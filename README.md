# my-project
test report
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الصفحة الرسمية لكلية ايلول</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            direction: rtl;
        }
        header {
            background-color: #274575;
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        nav {
            background-color: #003366;
            color: white;
            padding: 15px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-size: 1.2em;
            transition: color 0.3s;
        }
        nav a:hover {
            color: #ffd700;
        }
        .container {
            padding: 20px;
            max-width: 1200px;
            margin: auto;
        }
        .ads {
            margin: 20px 0;
            text-align: center;
        }
        .ads img {
            width: 100%;
            max-width: 550px;
            height: auto;
            display: block;
            margin: 10px auto;
            transition: transform 0.3s;
        }
        .ads img:hover {
            transform: scale(1.05);
        }
        .form-section, .departments, .price-inquiry {
            margin: 20px 0;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        .form-section:hover, .departments:hover, .price-inquiry:hover {
            transform: scale(1.02);
        }
        .form-section input, .form-section select, .form-section button {
            display: block;
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            font-size: 1em;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .form-section button {
            background-color: #274575;
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .form-section button:hover {
            background-color: #003366;
        }
        .departments h2, .price-inquiry h2 {
            text-align: center;
            color: #274575;
        }
        .departments ul {
            list-style-type: none;
            padding: 0;
        }
        .departments li {
            padding: 10px;
            margin: 10px 0;
            background-color: #f9f9f9;
            border: 1px solid #ddd;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .departments li:hover {
            background-color: #f1f1f1;
        }
        .department-details {
            display: none;
            margin-top: 10px;
            padding: 10px;
            background-color: #f4f4f4;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .price-details {
            display: none;
            margin-top: 10px;
            padding: 10px;
            background-color: #f4f4f4;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #003366;
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>كلية ايلول للعلوم الطبية والتقنية</h1>
    </header>
    <nav>
        <a href="#ads">الإعلانات</a>
        <a href="#departments">الاستعلام عن التخصصات</a>
        <a href="#price-inquiry">الاستعلام عن الأسعار</a>
        <a href="#registration">التسجيل</a>
    </nav>
    <div class="container">
        <section id="ads" class="ads">
            <h2>الإعلانات</h2>
            <img src="inf1.jpg" alt="إعلان 1">
            <img src="inf2.jpg" alt="إعلان 2">
        </section>
        <section id="departments" class="departments">
            <h2>الاستعلام عن التخصصات</h2>
            <ul>
                <li onclick="toggleDetails('ba')">
                    <strong>صيدله</strong>
                    <div id="ba" class="department-details">
                        يدرس تركيب الأدوية، علم الأدوية، وآلية عمل العقاقير.
                    </div>
                </li>
                <li onclick="toggleDetails('md')">
                    <strong>مساعد طبيب</strong>
                    <div id="md" class="department-details">
                        يجهز الطلاب للعمل كمساعدين للأطباء في التشخيص والعلاج.
                    </div>
                </li>
                <li onclick="toggleDetails('do')">
                    <strong>فني عمليات</strong>
                    <div id="do" class="department-details">
                        يدرب الطلاب على تقنيات الجراحة والإجراءات الطبية في غرف العمليات.
                    </div>
                </li>
                <li onclick="toggleDetails('dow')">
                    <strong>قباله</strong>
                    <div id="dow" class="department-details">
                        يركز على رعاية الأمهات أثناء الحمل والولادة وبعدها.
                    </div>
                </li>
                <li onclick="toggleDetails('cs')">
                    <strong>تقنية معلومات</strong>
                    <div id="cs" class="department-details">
                        يختص ببرمجة التطبيقات، الأمن السيبراني، وإدارة الشبكات.
                    </div>
                </li>
                <li onclick="toggleDetails('eng')">
                    <strong>جرافكس وملتميديا</strong>
                    <div id="eng" class="department-details">
                        يركز على تصميم الوسائط الرقمية، الإعلانات، والتصميم ثلاثي الأبعاد.
                    </div>
                </li>
            </ul>
        </section>
        <section id="price-inquiry" class="price-inquiry">
            <h2>الاستعلام عن الأسعار</h2>
            <form onsubmit="event.preventDefault(); displayPrice();">
                <label for="price-major">اختر التخصص:</label>
                <select id="price-major" name="price-major" required>
                    <option value="farma">الصيدله</option>
                    <option value="midical">مساعد طبيب</option>
                    <option value="doctor">فني عمليات</option>
                    <option value="doctor w">قبالة</option>
                    <option value="computer_science">تقنية معلومات</option>
                    <option value="engineering">جرافكس وملتميديا</option>
                </select>
                <button type="submit">استعلام</button>
            </form>
            <div id="price-details" class="price-details"></div>
        </section>
        <section id="registration" class="form-section">
            <h2>التسجيل</h2>
            <form action="#">
                <label for="name">الاسم:</label>
                <input type="text" id="name" name="name" required>
                <label for="number">رقم الهاتف:</label>
                <input type="number" id="number" name="number" required>
                <label for="major">التخصص:</label>
                <select id="major" name="major" required>
                    <option value="farma">الصيدله</option>
                    <option value="midical">مساعد طبيب</option>
                    <option value="doctor">فني عمليات</option>
                    <option value="doctor w">قبالة</option>
                    <option value="computer_science">تقنية معلومات</option>
                    <option value="engineering">جرافكس وملتميديا</option>
                </select>
                <button type="submit">تسجيل</button>
            </form>
        </section>
        <section id="contact">
            <h2>اتصل بنا</h2>
            <p>للتواصل مع الكلية، يرجى الاتصال على الأرقام التالية:</p>
            <p><strong>302520 - 771007199 - 771004055 - 771009313</strong></p>
        </section>
    </div>
    <footer>
        <p>&copy; 2025 كلية إيلول - جميع الحقوق محفوظة</p>
    </footer>
    <script>
        function toggleDetails(dept) {
            var details = document.getElementById(dept);
            if (details.style.display === "none" || details.style.display === "") {
                details.style.display = "block";
            } else {
                details.style.display = "none";
            }
        }
        
        function displayPrice() {
            var major = document.getElementById("price-major").value;
            var priceDetails = document.getElementById("price-details");
            var price;

            switch (major) {
                case "farma":
                case "midical":
                case "doctor":
                case "doctor w":
                    price = "١٨٠ ألف ريال يمني";
                    break;
                case "computer_science":
                case "engineering":
                    price = "١٥٠ ألف ريال يمني";
                    break;
                default:
                    price = "اختر تخصص صحيح";
            }

            priceDetails.innerHTML = "<strong>السعر:</strong> " + price;
            priceDetails.style.display = "block";
        }
    </script>
</body>
</html>
