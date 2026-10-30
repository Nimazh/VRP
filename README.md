# پایگاه جامع دانش و مرجع پژوهشی مسئله مسیریابی وسایل نقلیه (VRP)
## Vehicle Routing Problem (VRP) - Knowledge Base, Literature & Real-World Case Studies

---

## 📌 درباره این پروژه

این مخزن دانشی به منظور پوشش جامع، علمی، مستند و کاربردی **مسئله مسیریابی وسایل نقلیه (Vehicle Routing Problem)** گردآوری شده است. در این مجموعه:
1. مقالات بنیادین و تاریخی **ژورنال‌های تراز اول جهان** (مانند Management Science, Operations Research, Transportation Science) با شناسه DOI و فرمول‌بندی‌ها، به همراه **فایل‌های کامل PDF اصل مقالات بین‌المللی** قرار گرفته‌اند.
2. مقالات **علمی-پژوهشی معتبر وزارت علوم در دانشگاه‌های برتر ایران** (نظیر دانشگاه تهران، پژوهشکده حمل و نقل، نشریات مدیریت نوآوری و...) به همراه **فایل‌های کامل PDF دانلودشده اصل مقالات فارسی** در پوشه اختصاصی ذخیره شده‌اند.
3. مطالعات موردی واقعی پیاده‌سازی شده در صنایع بزرگ دنیا (UPS ORION، آمازون، والمارت) و ایران (دیجی‌کالا، پخش البرز و دارو، لبنیات کاله و میهن، شهرداری تهران) به همراه بنچ‌مارک‌های CVRPLIB و کد اجرایی پایتون مستندسازی شده‌اند.

---

## 📂 ساختار پوشه‌ها و نقشه راه اسناد

```
d:\prj\VRP\
│
├── README.md                                # همین راهنمای اصلی
├── STUDY_ROADMAP.md                         # 🗺️ نقشه راه جامع مطالعاتی (۶ فاز گام‌به‌گام از صفر تا مرز دانش)
│
├── articles/                                # بخش مقالات، تئوری‌ها و ادبیات پژوهشی
│   ├── 01_vrp_complete_guide_and_taxonomy.md   # تعریف پایه، تاریخچه و گونه‌شناسی جامع VRP
│   ├── 02_mathematical_models_and_formulations.md # فرمول‌بندی‌های دقیق ریاضی (۲ و ۳ اندیسه، افراز مجموعه)
│   ├── 03_algorithms_and_solution_methods.md     # روش‌های حل دقیق، فراابتکاری‌ها و یادگیری تقویتی عمیق
│   ├── 04_international_literature_review.md     # مرور کلی و سنتز مقالات بین‌المللی
│   ├── 05_domestic_iranian_literature_review.md  # تحلیل کلان رویکردهای پژوهشی اساتید ایران
│   │
│   ├── international_papers/                # 🌐 مقالات شناسنامه‌دار معتبر بین‌المللی
│   │   ├── README_international_papers.md       # فهرست مقالات معتبر بین‌المللی
│   │   ├── 01_dantzig_ramser_1959.md            # مقاله دانتزیگ و رامسر (Management Science 1959)
│   │   ├── 02_clarke_wright_1964.md             # مقاله الگوریتم پس‌انداز کلارک و رایت (Operations Research 1964)
│   │   ├── 03_solomon_1987.md                   # مقاله سلیمان و بنچ‌مارک‌های VRPTW (Operations Research 1987)
│   │   ├── 04_ropke_pisinger_2006.md            # مقاله الگوریتم ALNS (Transportation Science 2006)
│   │   ├── 05_vidal_hgs_2012.md                 # مقاله الگوریتم ژنتیک ترکیبی HGS (Operations Research 2012)
│   │   ├── 06_kool_attention_drl_2018.md        # مقاله یادگیری عمیق و Attention (کنفرانس ICLR 2019)
│   │   └── pdfs/                                # 📥 فایل‌های کامل PDF دانلودشده مقالات بین‌المللی
│   │       ├── 05_vidal_hgs_cvrp_2022.pdf       # اصل مقاله ژنتیک ترکیبی HGS تیبو ویدال
│   │       ├── 06_kool_attention_drl_2019.pdf   # اصل مقاله ترنسفورمر و یادگیری عمیق کول و ولینگ
│   │       └── 07_pessoa_vrpsolver_exact_2020.pdf # اصل مقاله سالور دقیق VRPSolver
│   │
│   └── domestic_iranian_papers/             # 🇮🇷 مقالات علمی-پژوهشی فارسی و دانشگاهی ایران
│       ├── README_domestic_papers.md            # فهرست مقالات معتبر دانشگاهی ایران
│       ├── 01_tavakkoli_uncertainty_differential_evolution.md # مقاله دکتر توکلی‌مقدم در شرایط عدم قطعیت و ترافیک
│       ├── 02_disaster_relief_mdvrp_earthquake.md # مقاله ساعی، توکلی‌مقدم، علینقیان در امدادرسانی بحران و زلزله
│       ├── 03_location_routing_survey_tehran_univ.md # مقاله مروری LRP در نشریه مهندسی صنایع دانشگاه تهران
│       ├── 04_pharmaceutical_coldchain_vrptw.md # مقاله بهینه‌سازی توزیع دارو با زنجیره سرد و پنجره زمانی
│       ├── 05_mashhad_urban_waste_network_sid.md # مقاله مسیریابی روی شبکه واقعی معابر مشهد با کلونی مورچگان
│       ├── 06_dairy_vrpspd_fuzzy_iran.md        # مقاله تحویل و دریافت همزمان لبنیات با رویکرد فازی
│       └── pdfs/                                # 📥 فایل‌های کامل PDF دانلودشده مقالات دانشگاهی ایران
│           ├── 01_tavakkoli_uncertainty_differential_evolution.pdf # اصل مقاله دکتر توکلی‌مقدم (نشریه IMOS)
│           ├── 02_disaster_relief_mdvrp_earthquake.pdf           # اصل مقاله ساعی و توکلی‌مقدم (پژوهشنامه حمل و نقل)
│           ├── 03_ut_industrial_management_vrp_101109.pdf        # اصل مقاله مسیریابی دانشگاه تهران (۱)
│           ├── 03_ut_industrial_management_vrp_22994.pdf         # اصل مقاله مسیریابی دانشگاه تهران (۲)
│           └── 03_ut_industrial_management_vrp_64592.pdf         # اصل مقاله مسیریابی دانشگاه تهران (۳)
│
└── case_studies/                            # بخش مطالعات موردی واقعی و صنعتی
    ├── 01_international_industrial_cases.md     # کیس‌های غول‌های جهانی (UPS ORION, Amazon, Walmart, ...)
    ├── 02_iranian_industrial_cases.md           # کیس‌های صنایع ایران (دیجی‌کالا، پخش دارو، لبنیات، شهرداری)
    └── 03_benchmarks_and_datasets_guide.md      # بنچ‌مارک‌های CVRPLIB، سلیمان و کد پایتون با Google OR-Tools
```
