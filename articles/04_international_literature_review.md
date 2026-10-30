# مرور مقالات شاخص و ادبیات پژوهشی بین‌المللی VRP
## International Literature Review: Seminal Papers, Milestones, and Breakthroughs

---

## ۱. مقدمه (Introduction)

در طول بیش از شش دهه از معرفی نخستین مقاله VRP در سال ۱۹۵۹، هزاران مقاله علمی در برترین ژورنال‌های تحقیق در عملیات مانند *Transportation Science*، *Operations Research*، *European Journal of Operational Research (EJOR)*، *Computers & Operations Research (COR)* و کنفرانس‌های هوش مصنوعی منتشر شده است. 

در این سند، مقالات تاریخ‌ساز و تحول‌آفرین بین‌المللی که مبنای تئوری و کاربردی این حوزه را شکل داده‌اند به ترتیب دوره‌های زمانی دسته‌بندی و تشریح شده‌اند.

---

## ۲. دوره پیدایش و پایه‌گذاری (۱۹۵۹ تا ۱۹۸۰)

### ۲.۱. دانتزیگ و رامسر (Dantzig & Ramser - 1959)
* **عنوان:** *The Truck Dispatching Problem*
* **ژورنال:** *Management Science*, Vol. 6, No. 1, pp. 80–91.
* **دستاورد:** نخستین صورت‌بندی ریاضی مسئله مسیریابی ناوگان سوخت با تقاضای پمپ‌بنزین‌ها و محدودیت ظرفیت تانکر. آنها روشی مبتنی بر تقریب برای دسته‌بندی ایستگاه‌ها ارائه دادند.

### ۲.۲. کلارک و رایت (Clarke & Wright - 1964)
* **عنوان:** *Scheduling of Vehicles from a Central Depot to a Number of Delivery Points*
* **ژورنال:** *Operations Research*, Vol. 12, No. 4, pp. 568–581.
* **دستاورد:** معرفی مفهوم انقلابی **پس‌انداز (Savings Concept)**. این مقاله پایه‌گذار الگوریتم‌های ساختاری حریصانه در توزیع کالا شد و همچنان به عنوان یکی از پراستنادترین مقالات تاریخ این علم شناخته می‌شود.

### ۲.۳. ژیلت و میلر (Gillett & Miller - 1974)
* **عنوان:** *A Heuristic Algorithm for the Vehicle-Dispatch Problem*
* **ژورنال:** *Operations Research*, Vol. 22, No. 2, pp. 340–349.
* **دستاورد:** معرفی الگوریتم **Sweep (جاروبی)** که رویکرد دوقطبی «ابتدا خوشه‌بندی، سپس مسیریابی» (Cluster-first, Route-second) را پایه‌ریزی کرد.

---

## ۳. دوره تثبیت قیود زمانی و بنچ‌مارک‌های استاندارد (۱۹۸۰ تا ۲۰۰۰)

### ۳.۱. ماریوس سلیمان (Marius M. Solomon - 1987)
* **عنوان:** *Algorithms for the Vehicle Routing and Scheduling Problems with Time Window Constraints*
* **ژورنال:** *Operations Research*, Vol. 35, No. 2, pp. 254–265.
* **دستاورد برجسته:**
  1. فرمول‌بندی مسئله VRPTW و ارائه الگوریتم‌های درج پی در پی (Insertion Heuristics نظیر $I_1$).
  2. طراحی **مجموعه داده‌های محک استاندارد سلیمان (Solomon Benchmarks)** شامل ۵۶ مسئله ۱۰۰ مشتری در ۶ دسته ساختاری:
     * **C1, C2:** مشتریان خوشه‌ای (Clustered).
     * **R1, R2:** مشتریان با توزیع تصادفی جغرافیایی (Random).
     * **RC1, RC2:** ترکیب خوشه‌ای و تصادفی.
     *(دسته‌های نوع ۱ دارای افق زمانی کوتاه و ظرفیت کم وسیله هستند؛ دسته‌های نوع ۲ افق زمانی بازتر و ظرفیت بزرگتری دارند).* این بنچ‌مارک تا به امروز معیار رسمی مقایسه تمام الگوریتم‌های دنیاست.

### ۳.۲. گیلبرت لاپورت (Gilbert Laporte - 1992)
* **عنوان:** *The Vehicle Routing Problem: An overview of exact and approximate algorithms*
* **ژورنال:** *European Journal of Operational Research (EJOR)*, Vol. 59, No. 3, pp. 345–358.
* **دستاورد:** جمع‌بندی جامع شاخه و کران، نامساوی‌های معتبر و اولین دسته‌بندی سیستماتیک روش‌های حل دقیق در برابر تقریبی.

---

## ۴. عصر طلایی فراابتکاری‌ها و پیشرفت روش‌های دقیق (۲۰۰۰ تا ۲۰۱۵)

### ۴.۱. پائولو توت و دانیله ویگو (Toth & Vigo - 2002 / 2014)
* **کتاب مرجع:** *The Vehicle Routing Problem* (SIAM Monographs on Discrete Mathematics and Applications).
* **دستاورد:** این کتاب به عنوان «انجیل VRP» شناخته می‌شود که توسط برجسته‌ترین دانشمندان این حوزه تالیف شده و تمامی فرمول‌بندی‌ها، برش‌ها، لم‌ها و کاربردهای صنعتی تا آن زمان را مدون کرد.

### ۴.۲. روپکه و پیسینگر (Ropke & Pisinger - 2006)
* **عنوان:** *An Adaptive Large Neighborhood Search Heuristic for the Pickup and Delivery Problem with Time Windows*
* **ژورنال:** *Transportation Science*, Vol. 40, No. 4, pp. 455–472.
* **دستاورد:** معرفی چارچوب **ALNS (جستجوی همسایگی بزرگ انطباقی)**. این متدولوژی با مکانیزم Destroy & Repair و یادگیری خودکار اوزان، مرزهای توانایی حل مسائل با ده‌ها قید همزمان (مانند تحویل، دریافت و پنجره زمانی) را جابجا کرد.

### ۴.۳. تیبو ویدال و همکاران (Vidal, Crainic, Gendreau, Prins - 2012)
* **عنوان:** *A hybrid genetic algorithm with adaptive diversity management for a large class of vehicle routing problems*
* **ژورنال:** *Operations Research*, Vol. 60, No. 3, pp. 611–624.
* **دستاورد:** اختراع معماری **HGS (Hybrid Genetic Search)**. این الگوریتم با ترکیب الگوریتم بهینه تقسیم مسیر (Split Algorithm) و مدیریت هوشمند تنوع جمعیت، توانست رکورد صدها مسئله باز را شکسته و تا امروز دقیق‌ترین فراابتکاری جهان برای CVRP و گونه‌های آن باشد.

---

## ۵. دوره شکوفایی نرم‌افزارهای حل دقیق و هوش مصنوعی (۲۰۱۵ تا ۲۰۲۶)

### ۵.۱. پکیج VRPSolver و پسوا و همکاران (Pessoa et al. - 2020)
* **عنوان:** *A Generic Exact Solver for Vehicle Routing Problems based on a Branch-Cut-and-Price Framework*
* **ژورنال:** *Mathematical Programming Computation*, Vol. 12, pp. 647–689.
* **دستاورد:** ایجاد یک سالور دقیق همه‌منظوره که توانست مسائل حل‌نشده با ابعاد ۲۰۰ تا ۳۰۰ گره در بنچ‌مارک‌های CVRP، VRPTW، MDVRP و VRPSPD را پس از دهه‌ها به اثبات بهینگی مطلق برساند.

### ۵.۲. یادگیری عمیق و کول و همکاران (Kool, van Hoof, Welling - 2018)
* **عنوان:** *Attention, Learn to Solve Routing Problems!*
* **کنفرانس:** *International Conference on Learning Representations (ICLR 2019)*.
* **دستاورد:** تحول عظیم در حل VRP به کمک شبکه‌های عصبی گراف و ترنسفورمر. مدل یاد می‌گیرد بدون نیاز به نوشتن دستی هیوریستیک، با مشاهده نمونه‌های زیاد، نقشه مسیرها را در کسری از ثانیه با دقتی نزدیک به ۹۷-۹۸٪ فراابتکاری‌ها تولید کند.

### ۵.۳. مور و اسپرانتزا (Mor & Speranza - 2022)
* **عنوان:** *Vehicle routing problems over 60 years: Extensions and taxonomy*
* **ژورنال:** *Computers & Operations Research*, Vol. 141, 105689.
* **دستاورد:** جامع‌ترین مرور سیستماتیک ۶۰ سال تاریخچه VRP با تمرکز بر ترندهای معاصر نظیر لجستیک اشتراکی (Crowd-shipping)، استفاده از پهپادها (Drones / UAVs)، وسایل نقلیه خودران (Autonomous Delivery) و توزیع سبز بدون آلودگی.

---

## ۶. جدول خلاصه ارجاعات مقالات کلیدی بین‌المللی

| سال | نویسندگان اصلی | عنوان کلیدی | نوآوری اصلی | حوزه کاربرد |
| :--- | :--- | :--- | :--- | :--- |
| **1959** | Dantzig & Ramser | *Truck Dispatching Problem* | اولین فرمول‌بندی ریاضی VRP | پخش سوخت و بنزین |
| **1964** | Clarke & Wright | *Savings Method* | الگوریتم پس‌انداز ساختاری | توزیع تجاری کالا |
| **1987** | Solomon | *VRPTW Benchmarks & Heuristics* | ایجاد پایگاه داده استاندارد جهانی | پنجره‌های زمانی تحویل |
| **2006** | Ropke & Pisinger | *Adaptive Large Neighborhood Search* | چارچوب ALNS با عملگرهای متعدد | مسائل پیچیده چندقیدی |
| **2012** | Vidal et al. | *Hybrid Genetic Search (HGS)* | جستجوی ژنتیک ترکیبی با Split | رکورد کیفیتی بنچ‌مارک‌ها |
| **2018** | Kool et al. | *Attention Model for Routing* | ترنسفورمر و یادگیری تقویتی | حل بلادرنگ و سریع |
| **2020** | Pessoa et al. | *VRPSolver / Branch-Cut-Price* | قوی‌ترین سالور دقیق عمومی | حل قطعی ریاضیاتی |
| **2022** | Mor & Speranza | *60 Years of VRP Review* | طبقه‌بندی جامع روندهای نوظهور | پهپادها، خودروهای برقی |
