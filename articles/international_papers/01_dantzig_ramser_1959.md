# مقاله بین‌المللی ۱: تولد مسئله مسیریابی وسایل نقلیه (دانتزیگ و رامسر ۱۹۵۹)

---

## 📌 مشخصات شناسنامه‌ای مقاله (Bibliographic Citation)

* **عنوان کامل مقاله:** The Truck Dispatching Problem
* **نویسندگان:** 
  1. **George B. Dantzig** (دانشگاه برکلی، پدر برنامه‌ریزی خطی و مخترع الگوریتم سیمپلکس)
  2. **John H. Ramser** (شرکت نفتی M. W. Kellogg)
* **نام ژورنال معتبر:** *Management Science* (موسسه INFORMS آمریکا)
* **سال و دوره انتشار:** Volume 6, Issue 1, October 1959, Pages 80–91
* **شناسه بین‌المللی دیجیتال (DOI):** `10.1287/mnsc.6.1.80`
* **لینک پایگاه ژورنال:** `https://pubsonline.informs.org/doi/10.1287/mnsc.6.1.80`

---

## 📝 چکیده رسمی و تاریخی مقاله (Abstract)

> *"The paper is concerned with the optimum routing of a fleet of gasoline delivery trucks between a bulk terminal and a large number of service stations supplied by the terminal. The distance between any two locations is given, and each demand is specified. The problem is to assign each customer to a truck and determine the route for each truck so that all demands are satisfied and the total distance traveled is a minimum."*

این مقاله نخستین سند مکتوب در تاریخ بشریت است که مسئله VRP را به عنوان یک کلاس مجزا از بهینه‌سازی ترکیبیاتی و فراتر از مسئله فروشنده دوره‌گرد (TSP) مطرح کرد. نویسندگان نشان دادند که چگونه می‌توان اعزام تانکرهای سوخت را از یک پایانه نفتی مادر به مجموعه‌ای از پمپ‌بنزین‌ها به صورت علمی زمان‌بندی و مسیریابی نمود.

---

## 📐 نوآوری ریاضیاتی دانتزیگ و رامسر

دانتزیگ و رامسر مسئله را ابتدا به صورت یک مسئله برنامه‌ریزی صفر و یک خطی تعمیم دادند و برای حل آن، یک روش تقریب چندمرحله‌ای بر اساس دسته‌بندی دوتایی گره‌ها ارائه کردند:
* هر زوج از مشتریان $(i, j)$ در صورتی ادغام می‌شدند که تقاضای کل آنها $q_i + q_j \le C$ باشد.
* این گره‌های ادغام‌شده مانند یک سوپرگره در نظر گرفته شده و تا رسیدن به سقف ظرفیت تانکر تجمیع می‌شدند.
* این ایده بعدها الهام‌بخش الگوریتم انقلابی کلارک و رایت شد.
