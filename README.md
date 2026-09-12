talebi-saghir/
│
├── frontend/
│   ├── index.html
│   ├── register.html
│   ├── login.html
│   ├── dashboard.html
│   │
│   ├── css/
│   │   └── style.css
│   │
│   └── js/
│       ├── config.js
│       ├── api.js
│       ├── auth.js
│       └── dashboard.js
│
├── backend/
│   ├── Code.gs
│   └── README.md
│
└── README.md
frontend/js/config.js
التلميذ
   ↓
GitHub Pages
   ↓
التسجيل / الدخول
   ↓
Google Apps Script
   ↓
Google Sheets
   ↓
Google Drive
طالبي الصغيرطالبي الصغير
│
├── 4 أساسي
│   ├── رياضيات
│   ├── عربية
│   ├── Français
│   ├── English
│   └── إيقاظ علمي
│رياضيات
│بداية الاشتراك
       +
عدد الأشهر
       ↓
تاريخ الانتهاء
       ↓
ACTIVE / EXPIRED
├── الثلاثي الأول
│   ├── 📘 الدروسطالبي الصغير
│
├── 🏠 الرئيسية
│
├── 👤 حساب التلميذ
│   ├── الاسم واللقب
│   ├── المستوى
│   └── حالة الاشتراك
│
├── 📚 المحتوى
│   ├── 4 أساسي
│   ├── 5 أساسي
│   └── 6 أساسي
│
├── 📖 المواد
│   ├── رياضيات
│   ├── عربية
│   ├── Français
│   ├── English
│   └── إيقاظ علمي
│<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>طالبي الصغير | نحو الاستقلالية</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

body{
    font-family:Tahoma,Arial,sans-serif;
    background:#f4f7fc;
    color:#172033;
}

/* ================= HEADER ================= */

header{
    background:white;
    height:75px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 6%;
    box-shadow:0 2px 10px rgba(0,0,0,.06);
    position:sticky;
    top:0;
    z-index:100;
}

.logo{
    display:flex;
    align-items:center;
    gap:12px;
}

.logo-icon{
    width:48px;
    height:48px;
    border-radius:14px;
    background:linear-gradient(135deg,#315bd6,#7548d8);
    color:white;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:27px;
    font-weight:bold;
}

.logo-text{
    font-size:20px;
    font-weight:bold;
}

.logo-text small{
    display:block;
    font-size:10px;
    color:#777;
    margin-top:2px;
}

nav{
    display:flex;
    gap:20px;
    align-items:center;
}

nav a{
    text-decoration:none;
    color:#333;
    font-size:14px;
}

.btn{
    border:none;
    background:#315bd6;
    color:white;
    padding:11px 20px;
    border-radius:12px;
    cursor:pointer;
    font-weight:bold;
    text-decoration:none;
    display:inline-block;
}

.btn:hover{
    background:#2448b8;
}

/* ================= HERO ================= */

.hero{
    max-width:1200px;
    margin:auto;
    min-height:520px;
    padding:70px 6%;
    display:grid;
    grid-template-columns:1.2fr .8fr;
    gap:50px;
    align-items:center;
}

.hero h1{
    font-size:48px;
    line-height:1.4;
    margin:15px 0;
}

.hero h1 span{
    color:#315bd6;
}

.hero p{
    color:#667085;
    font-size:18px;
    line-height:2;
}

.hero-buttons{
    margin-top:30px;
    display:flex;
    gap:12px;
}

.btn-light{
    background:#eaf0ff;
    color:#315bd6;
}

.hero-card{
    background:white;
    border-radius:30px;
    padding:45px;
    text-align:center;
    box-shadow:0 20px 60px rgba(35,55,120,.12);
}

.hero-card .book{
    font-size:80px;
    margin-bottom:20px;
}

.hero-card h2{
    margin-bottom:10px;
}

.hero-card p{
    font-size:14px;
}

/* ================= SECTIONS ================= */

section{
    max-width:1200px;
    margin:auto;
    padding:60px 6%;
}

.section-title{
    margin-bottom:30px;
}

.section-title span{
    color:#315bd6;
    font-weight:bold;
}

.section-title h2{
    margin-top:5px;
    font-size:30px;
}

/* ================= LEVELS ================= */

.levels{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.level{
    background:white;
    padding:30px;
    border-radius:22px;
    border:1px solid #e5e8f0;
    cursor:pointer;
    transition:.2s;
}

.level:hover{
    transform:translateY(-5px);
    box-shadow:0 15px 35px rgba(40,60,120,.1);
}

.level-number{
    font-size:50px;
    font-weight:bold;
    color:#315bd6;
}

.level h3{
    margin:10px 0;
}

.level p{
    color:#777;
}

/* ================= SUBJECTS ================= */

.subjects{
    display:grid;
    grid-template-columns:repeat(5,1fr);
    gap:15px;
}

.subject{
    background:white;
    border:1px solid #e5e8f0;
    border-radius:20px;
    padding:25px 15px;
    text-align:center;
    cursor:pointer;
    transition:.2s;
}

.subject:hover{
    transform:translateY(-4px);
    border-color:#315bd6;
}

.subject-icon{
    font-size:40px;
    margin-bottom:12px;
}

.subject h3{
    font-size:16px;
}

/* ================= TERMS ================= */

.terms{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.term{
    background:#eef2ff;
    border:1px solid #dce3ff;
    padding:25px;
    border-radius:20px;
    cursor:pointer;
}

.term h3{
    color:#315bd6;
    margin-bottom:8px;
}

.term p{
    color:#666;
    font-size:13px;
}

/* ================= LIBRARY ================= */

.library{
    background:white;
    border-radius:25px;
    padding:35px;
    border:1px solid #e5e8f0;
}

.files{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
    margin-top:20px;
}

.file{
    padding:20px;
    border:1px solid #e5e8f0;
    border-radius:15px;
}

.file-icon{
    font-size:30px;
}

.file h4{
    margin:10px 0;
}

.file a{
    color:#315bd6;
    font-weight:bold;
    text-decoration:none;
}

/* ================= REGISTER ================= */

.register{
    background:linear-gradient(135deg,#315bd6,#7048d8);
    color:white;
    border-radius:30px;
    text-align:center;
}

.register h2{
    font-size:32px;
    margin-bottom:12px;
}

.register p{
    margin-bottom:25px;
}

/* ================= FOOTER ================= */

footer{
    background:#172033;
    color:white;
    text-align:center;
    padding:35px;
    margin-top:50px;
}

footer small{
    display:block;
    margin-top:8px;
    color:#aeb5c5;
}

/* ================= MOBILE ================= */

@media(max-width:850px){

    nav a:not(.btn){
        display:none;
    }

    .hero{
        grid-template-columns:1fr;
        text-align:center;
    }

    .hero h1{
        font-size:35px;
    }

    .hero-buttons{
        justify-content:center;
    }

    .levels{
        grid-template-columns:1fr;
    }

    .subjects{
        grid-template-columns:repeat(2,1fr);
    }

    .terms{
        grid-template-columns:1fr;
    }

    .files{
        grid-template-columns:1fr;
    }
}
</style>
</head>

<body>

<!-- ================= HEADER ================= -->

<header>

    <div class="logo">

        <div class="logo-icon">
            ط
        </div>

        <div class="logo-text">
            طالبي الصغير
            <small>نحو الاستقلالية</small>
        </div>

    </div>

    <nav>

        <a href="#levels">
            المستويات
        </a>

        <a href="#subjects">
            المواد
        </a>

        <a href="#library">
            المكتبة
        </a>

        <a href="login.html">
            تسجيل الدخول
        </a>

        <a class="btn" href="register.html">
            إنشاء حساب
        </a>

    </nav>

</header>


<!-- ================= HERO ================= -->

<div class="hero">

    <div>

        <span style="color:#315bd6;font-weight:bold;">
            منصة تعليمية عن بعد
        </span>

        <h1>
            مرحبًا بك في
            <span>طالبي الصغير</span>
        </h1>

        <p>
            منصة تعليمية تساعد التلميذ على التعلم،
            التدريب، المراجعة، ثم الوصول إلى الاستقلالية.
        </p>

        <div class="hero-buttons">

            <a href="register.html" class="btn">
                ابدأ الآن
            </a>

            <a href="#levels" class="btn btn-light">
                اكتشف المنصة
            </a>

        </div>

    </div>


    <div class="hero-card">

        <div class="book">
            📚
        </div>

        <h2>
            كل ما يحتاجه التلميذ
        </h2>

        <p>
            دروس • تمارين • إصلاح • كتب
        </p>

        <p>
            الرابعة • الخامسة • السادسة أساسي
        </p>

    </div>

</div>


<!-- ================= LEVELS ================= -->

<section id="levels">

    <div class="section-title">

        <span>
            اختر المستوى
        </span>

        <h2>
            السنوات الدراسية
        </h2>

    </div>


    <div class="levels">

        <div class="level"
             onclick="chooseLevel(4)">

            <div class="level-number">
                4
            </div>

            <h3>
                السنة الرابعة أساسي
            </h3>

            <p>
                جميع المواد والثلاثيات
            </p>

        </div>


        <div class="level"
             onclick="chooseLevel(5)">

            <div class="level-number">
                5
            </div>

            <h3>
                السنة الخامسة أساسي
            </h3>

            <p>
                جميع المواد والثلاثيات
            </p>

        </div>


        <div class="level"
             onclick="chooseLevel(6)">

            <div class="level-number">
                6
            </div>

            <h3>
                السنة السادسة أساسي
            </h3>

            <p>
                جميع المواد والثلاثيات
            </p>

        </div>

    </div>

</section>


<!-- ================= SUBJECTS ================= -->

<section id="subjects">

    <div class="section-title">

        <span>
            المواد
        </span>

        <h2>
            ماذا يتعلم التلميذ؟
        </h2>

    </div>


    <div class="subjects">

        <div class="subject">
            <div class="subject-icon">➕</div>
            <h3>الرياضيات</h3>
        </div>

        <div class="subject">
            <div class="subject-icon">📖</div>
            <h3>العربية</h3>
        </div>

        <div class="subject">
            <div class="subject-icon">🇫🇷</div>
            <h3>الفرنسية</h3>
        </div>

        <div class="subject">
            <div class="subject-icon">🇬🇧</div>
            <h3>الإنجليزية</h3>
        </div>

        <div class="subject">
            <div class="subject-icon">🔬</div>
            <h3>الإيقاظ العلمي</h3>
        </div>

    </div>

</section>


<!-- ================= TERMS ================= -->

<section>

    <div class="section-title">

        <span>
            البرنامج
        </span>

        <h2>
            الثلاثيات
        </h2>

    </div>


    <div class="terms">

        <div class="term">
            <h3>الثلاثي الأول</h3>
            <p>
                دروس وتمارين وإصلاحات وكتب
            </p>
        </div>

        <div class="term">
            <h3>الثلاثي الثاني</h3>
            <p>
                دروس وتمارين وإصلاحات وكتب
            </p>
        </div>

        <div class="term">
            <h3>الثلاثي الثالث</h3>
            <p>
                دروس وتمارين وإصلاحات وكتب
            </p>
        </div>

    </div>

</section>


<!-- ================= LIBRARY ================= -->

<section id="library">

    <div class="section-title">

        <span>
            المكتبة
        </span>

        <h2>
            مكتبة طالبي الصغير
        </h2>

    </div>


    <div class="library">

        <h3>
            🔒 المكتبة متاحة للمشتركين
        </h3>

        <p style="color:#777;margin-top:10px;">
            بعد تفعيل الاشتراك يستطيع التلميذ الوصول
            إلى الكتب والوثائق الخاصة بالمستوى.
        </p>


        <div class="files">

            <div class="file">

                <div class="file-icon">
                    📕
                </div>

                <h4>
                    كتب الرياضيات
                </h4>

                <a href="login.html">
                    تسجيل الدخول
                </a>

            </div>


            <div class="file">

                <div class="file-icon">
                    📘
                </div>

                <h4>
                    كتب العربية
                </h4>

                <a href="login.html">
                    تسجيل الدخول
                </a>

            </div>


            <div class="file">

                <div class="file-icon">
                    📗
                </div>

                <h4>
                    كتب الفرنسية
                </h4>

                <a href="login.html">
                    تسجيل الدخول
                </a>

            </div>

        </div>

    </div>

</section>


<!-- ================= REGISTER ================= -->

<section>

    <div class="register">

        <h2>
            هل أنت مستعد للتعلم؟
        </h2>

        <p>
            أنشئ حسابك وابدأ رحلتك نحو الاستقلالية.
        </p>

        <a href="register.html"
           class="btn"
           style="background:white;color:#315bd6;">
            إنشاء حساب
        </a>

    </div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

    <strong>
        طالبي الصغير
    </strong>

    <small>
        نحو الاستقلالية
    </small>

    <small>
        تحت إشراف الأستاذ أيمن دبوسي
    </small>

    <small>
        © 2026 جميع الحقوق محفوظة
    </small>

</footer>


<script>

function chooseLevel(level){

    localStorage.setItem(
        "selectedLevel",
        level
    );

    window.location.href =
        "dashboard.html?level=" + level;

}

</script>

</body>
</html>
├── 🗓️ الثلاثيات
│   ├── الثلاثي الأول
│   ├── الثلاثي الثاني
│   └── الثلاثي الثالث
│
├── 🔒 مكتبة المشتركين
│
└── ⚙️ الإدارة
    ├── التلاميذ
    ├── الاشتراكات
    ├── الملفات
    ├── الكتب
    └── الإحصائيات
│   ├── 📝 التمارين
│   ├── ✅ الإصلاح
│   └── 📚 الكتب 🔒
│
├── الثلاثي الثاني
│   ├── 📘 الدروس
│   ├── 📝 التمارين
│   ├── ✅ الإصلاح
│   └── 📚 الكتب 🔒التلميذ يسجل
       ↓
الإدارة تستقبل التسجيل
       ↓
تفعيل الاشتراك
       ↓
الحساب يصبح ACTIVE
       ↓
المكتبة تفتح تلقائيًا
│التلميذ يسجل
       ↓
الإدارة تستقبل التسجيل
       ↓
تفعيل الاشتراك
       ↓
الحساب يصبح ACTIVE
       ↓
المكتبة تفتح تلقائيًا
└── الثلاثي الثالث
    ├── 📘 الدروس
    ├── 📝 التمارين
    ├── ✅ الإصلاح
    └── 📚 الكتب 🔒
├── 5 أساسي
│   └── نفس المواد
│
└── 6 أساسي
    └── نفس المواد
│
├── التلميذ
│   ├── تسجيل
│   ├── تسجيل الدخول
│   └── لوحة التلميذ
│
└── الإدارة
    ├── التلاميذ
    ├── الاشتراكات
    ├── الوثائق
    ├── الكتب
    └── الإحصائيات
   ↓
الدروس + التمارين + الإصلاح + مكتبة الكتب
