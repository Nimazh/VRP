# مقاله بین‌المللی ۲: الگوریتم پس‌انداز کلارک و رایت (۱۹۶۴)

---

## 📌 مشخصات شناسنامه‌ای مقاله (Bibliographic Citation)

* **عنوان کامل مقاله:** Scheduling of Vehicles from a Central Depot to a Number of Delivery Points
* **نویسندگان:** 
  1. **Geoffrey Clarke** (مشاور ارشد تحقیق در عملیات، بریتانیا)
  2. **John W. Wright** (محقق علوم مدیریت، بریتانیا)
* **نام ژورنال معتبر:** *Operations Research* (موسسه INFORMS آمریکا)
* **سال و دوره انتشار:** Volume 12, Issue 4, August 1964, Pages 568–581
* **شناسه بین‌المللی دیجیتال (DOI):** `10.1287/opre.12.4.568`
* **میزان استناد:** بیش از ۵,۰۰۰ استناد رسمی در ادبیات بهینه‌سازی و علوم کامپیوتر

---

## 📝 چکیده و خلاصه مقاله (Abstract)

> *"An algorithm is presented for scheduling the routes of a fleet of delivery vehicles of varying capacities from a central depot to a number of delivery points with known demands. The algorithm aims to minimize total mileage traveled and vehicles required by iteratively linking delivery points based on the potential distance savings achieved."*

این مقاله انقلابی‌ترین الگوریتم ساختاری ابتکاری (Constructive Heuristic) تاریخ VRP را معرفی کرد که هنوز هم در ماژول‌های تولید جواب اولیه نرم‌افزارهای تجاری بزرگ جهان به کار می‌رود.

---

## 📐 فرمول ریاضی پس‌انداز (The Savings Formula)

ایده کلیدی کلارک و رایت به این صورت است:
اگر فرض کنیم در بدترین حالت، به هر مشتری $i$ یک کامیون اختصاص داده شود که از دپو ($0$) به $i$ رفته و بازگردد، مسافت طی‌شده $2 c_{0i}$ خواهد بود.
اگر دو مشتری $i$ و $j$ در یک تور ادغام شوند ($0 \to i \to j \to 0$):
* هزینه رفت و برگشت مجزا: $2 c_{0i} + 2 c_{0j}$
* هزینه مسیر ادغام‌شده: $c_{0i} + c_{ij} + c_{j0}$
* **میزان صرفه‌جویی یا پس‌انداز حاصل از اتصال $i$ به $j$ برابر است با:**
  $$s_{ij} = c_{0i} + c_{0j} - c_{ij}$$

الگوریتم در دو نسخه موازی (Parallel) و متوالی (Sequential) توسعه داده شد و تا تکمیل ظرفیت خودرو، مشتریان با بالاترین $s_{ij}$ را در یک مسیر پیوند می‌دهد.
