# راهنمای دیتاست‌های بنچ‌مارک استاندارد و پیاده‌سازی عملی VRP
## Standard Benchmarks, Datasets, and Hands-on Python Implementation Guide

---

## ۱. پایگاه داده جهانی CVRPLIB (مرجع رسمی مقایسه الگوریتم‌ها)

تمامی مقالات علمی بین‌المللی برای اثبات برتری الگوریتم‌های خود موظف هستند نتایج خود را روی دیتاست‌های استاندارد **CVRPLIB (Capacitated Vehicle Routing Problem Library)** گزارش کنند.

* **آدرس پایگاه داده:** `http://vrp.atd-lab.inf.puc-rio.br` یا `http://vrp.galgos.inf.puc-rio.br/index.php/en/`
* این کتابخانه شامل بهترین جواب‌های شناخته‌شده (BKS - Best Known Solution) در کل تاریخ برای هر مسئله است.

### مهم‌ترین مجموعه‌های CVRPLIB:

1. **مجموعه‌های اوگرا (Augerat et al. - 1995):**
   * معروف به **Set A**، **Set B** و **Set P**.
   * شامل مسائلی با ۱۶ تا ۸۰ مشتری. امروزه تمام این مسائل با روش‌های دقیق در چند ثانیه حل می‌شوند و برای تست اولیه الگوریتم‌ها ایده‌آل هستند.
2. **مجموعه کریستوفیدز (Christofides, Mingozzi, Toth - 1979):**
   * مسائل کلاسیک CMT شامل ۵۰ تا ۱۹۹ مشتری با چیدمان‌های تصادفی و خوشه‌ای.
3. **مجموعه گلدن (Golden et al. - 1998):**
   * مسائل با مقیاس بزرگتر (Large-scale) شامل ۲۰۰ تا ۴۸۳ مشتری.
4. **مجموعه اچوا (Uchoa et al. - 2014):**
   * این مجموعه **استاندارد طلایی کنونی جهان** است.
   * شامل ۱۰۰ نمونه مسئله جدید (از ۱۰۰ تا ۱۰۰۰ مشتری) که بر اساس واقعیت‌های عملیات لجستیک صنعتی شبیه‌سازی شده‌اند (مانند موقعیت دپو در مرکز یا گوشه، پراکندگی خوشه‌ای مشتریان، و توزیع‌های مختلف تقاضا).

---

## ۲. بنچ‌مارک‌های سلیمان برای مسائل با پنجره زمانی (Solomon VRPTW)

مجموعه داده‌های ماریوس سلیمان (۱۹۸۷) شامل ۵۶ مسئله با ۱۰۰ مشتری است که به شش دسته کلیدی تقسیم می‌شوند:

| نام دسته | ساختار پراکندگی مشتریان | افق زمان‌بندی و ظرفیت خودرو | کاربرد در دنیای واقعی |
| :--- | :--- | :--- | :--- |
| **C1** | خوشه‌ای (Clustered) | افق کوتاه / خودروهای با ظرفیت کم | فروشگاه‌های زنجیره‌ای در مراکز تجاری |
| **C2** | خوشه‌ای (Clustered) | افق بلند / خودروهای با ظرفیت بالا | انتقال بار بین انبارهای صنعتی متمرکز |
| **R1** | پراکنده تصادفی (Random) | افق کوتاه / خودروهای با ظرفیت کم | تحویل فوری غذا یا سوپرمارکت آنلاین |
| **R2** | پراکنده تصادفی (Random) | افق بلند / خودروهای با ظرفیت بالا | خدمات پستی و توزیع کالای روزانه |
| **RC1** | ترکیبی (Random-Clustered) | افق کوتاه / خودروهای با ظرفیت کم | توزیع مویرگی در شهرهای با بافت ناهمگن |
| **RC2** | ترکیبی (Random-Clustered) | افق بلند / خودروهای با ظرفیت بالا | پخش سراسری قطعات یدکی و اقلام تجاری |

### توسعه مقیاس بزرگ هومبرگر (Homberger & Gehring - 1999):
برای ارزیابی فراابتکاری‌ها در ابعاد غول‌پیکر، ۳۰۰ مسئله با ابعاد ۲۰۰، ۴۰۰، ۶۰۰، ۸۰۰ و ۱۰۰۰ مشتری بر اساس ساختار سلیمان طراحی شده است.

---

## ۳. استفاده از داده‌های واقعی نقشه شهری با Python و OpenStreetMap

در پروژه‌های صنعتی واقعی به جای استفاده از مسافت اقلیدسی ($\sqrt{\Delta x^2 + \Delta y^2}$)، باید از معابر واقعی، خیابان‌های یک‌طرفه و ترافیک استفاده کرد.

### ابزارهای استخراج داده نقشه در پایتون:
1. **کتابخانه OSMnx:** دانلود گراف کامل معابر شهری از OpenStreetMap با مشخصات جهت و سرعت مجاز:
   ```python
   import osmnx as ox
   # دانلود شبکه معابر خودرویی منطقه ۶ تهران
   G = ox.graph_from_place("District 6, Tehran, Iran", network_type="drive")
   ```
2. **سرویس OSRM (Open Source Routing Machine):**
   * سریع‌ترین موتور محاسبه ماتریس فاصله و زمان سفر در دنیا بر پایه C++ و الگوریتم‌های Contraction Hierarchies.
   * می‌توان سرور محلی OSRM را با نقشه ایران (`iran-latest.osm.pbf`) راه‌اندازی کرد و ماتریس فاصله هزاران نقطه را در کسری از ثانیه محاسبه نمود.

---

## ۴. نمونه کد عملی و کامل پیاده‌سازی CVRP با Google OR-Tools در پایتون

در ادامه یک اسکریپت کامل و تست‌شده برای حل مسئله مسیریابی وسایل نقلیه با محدودیت ظرفیت (CVRP) با استفاده از موتور بهینه‌سازی صنعتی **Google OR-Tools** ارائه شده است:

```python
"""
پیاده‌سازی مسئله مسیریابی وسایل نقلیه با قید ظرفیت (CVRP)
با استفاده از Google OR-Tools
"""
from ortools.constraint_solver import routing_enums_pb2
from ortools.constraint_solver import pywrapcp

def create_data_model():
    """ایجاد داده‌های ورودی مسئله (ماتریس مسافت، تقاضاها و ظرفیت ناوگان)"""
    data = {}
    # ماتریس مسافت اقلیدسی یا واقعی بین گره‌ها (گره 0 نشان‌دهنده دپو است)
    data["distance_matrix"] = [
        [0, 548, 776, 696, 582, 478, 194, 798, 409, 657],
        [548, 0, 684, 308, 194, 502, 388, 354, 582, 319],
        [776, 684, 0, 992, 878, 502, 800, 936, 409, 999],
        [696, 308, 992, 0, 114, 650, 536, 342, 729, 217],
        [582, 194, 878, 114, 0, 536, 422, 228, 615, 125],
        [478, 502, 502, 650, 536, 0, 319, 673, 273, 655],
        [194, 388, 800, 536, 422, 319, 0, 673, 456, 490],
        [798, 354, 936, 342, 228, 673, 673, 0, 708, 182],
        [409, 582, 409, 729, 615, 273, 456, 708, 0, 730],
        [657, 319, 999, 217, 125, 655, 490, 182, 730, 0],
    ]
    # تقاضای هر مشتری (تقاضای دپو 0 است)
    data["demands"] = [0, 1, 1, 2, 4, 2, 4, 8, 8, 1]
    # تعداد وسایل نقلیه موجود در دپو
    data["num_vehicles"] = 4
    # ظرفیت هر وسیله نقلیه
    data["vehicle_capacities"] = [15, 15, 15, 15]
    # شاخص دپو (مبدا و مقصد ناوگان)
    data["depot"] = 0
    return data

def print_solution(data, manager, routing, solution):
    """نمایش گرافیکی و متنی مسیرهای بهینه استخراج شده"""
    print(f"مقدار بهینه تابع هدف (مجموع مسافت کل): {solution.ObjectiveValue()} واحد\n")
    total_distance = 0
    total_load = 0
    for vehicle_id in range(data["num_vehicles"]):
        index = routing.Start(vehicle_id)
        plan_output = f"مسیر خودروی شماره {vehicle_id + 1}:\n  "
        route_distance = 0
        route_load = 0
        while not routing.IsEnd(index):
            node_index = manager.IndexToNode(index)
            route_load += data["demands"][node_index]
            plan_output += f"گره {node_index} (بار: {route_load}) -> "
            previous_index = index
            index = solution.Value(routing.NextVar(index))
            route_distance += routing.GetArcCostForVehicle(previous_index, index, vehicle_id)
        
        node_index = manager.IndexToNode(index)
        plan_output += f"گره {node_index} (پایان در دپو)\n"
        plan_output += f"  مسافت طی‌شده: {route_distance} واحد | مجموع بار حمل‌شده: {route_load}/{data['vehicle_capacities'][vehicle_id]}\n"
        print(plan_output)
        total_distance += route_distance
        total_load += route_load
    print(f"مجموع کل مسافت پیموده شده توسط ناوگان: {total_distance} واحد")
    print(f"مجموع کل بارهای توزیع شده: {total_load} واحد")

def main():
    # ۱. آماده‌سازی داده‌ها
    data = create_data_model()

    # ۲. ایجاد مدیر شاخص‌های مسیریابی
    manager = pywrapcp.RoutingIndexManager(
        len(data["distance_matrix"]), data["num_vehicles"], data["depot"]
    )

    # ۳. ایجاد مدل اصلی مسیریابی
    routing = pywrapcp.RoutingModel(manager)

    # ۴. تعریف تابع هزینه مسافت
    def distance_callback(from_index, to_index):
        from_node = manager.IndexToNode(from_index)
        to_node = manager.IndexToNode(to_index)
        return data["distance_matrix"][from_node][to_node]

    transit_callback_index = routing.RegisterTransitCallback(distance_callback)
    routing.SetArcCostEvaluatorOfAllVehicles(transit_callback_index)

    # ۵. تعریف قید ظرفیت بارگیری ناوگان
    def demand_callback(from_index):
        from_node = manager.IndexToNode(from_index)
        return data["demands"][from_node]

    demand_callback_index = routing.RegisterUnaryTransitCallback(demand_callback)
    routing.AddDimensionWithVehicleCapacity(
        demand_callback_index,
        0,  # بدون ظرفیت مازاد
        data["vehicle_capacities"],  # ظرفیت خودروها
        True,  # شروع از صفر
        "Capacity",
    )

    # ۶. تنظیم پارامترهای جستجوی بهینه‌سازی و استراتژی فراابتکاری
    search_parameters = pywrapcp.DefaultRoutingSearchParameters()
    search_parameters.first_solution_strategy = (
        routing_enums_pb2.FirstSolutionStrategy.PATH_CHEAPEST_ARC
    )
    search_parameters.local_search_metaheuristic = (
        routing_enums_pb2.LocalSearchMetaheuristic.GUIDED_LOCAL_SEARCH
    )
    search_parameters.time_limit.FromSeconds(2)

    # ۷. حل مسئله
    solution = routing.SolveWithParameters(search_parameters)

    # ۸. چاپ نتایج
    if solution:
        print_solution(data, manager, routing, solution)
    else:
        print("هیچ جوابی یافت نشد!")

if __name__ == "__main__":
    main()
```
