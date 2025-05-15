

html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مشروع أنس ماجد الصبحي</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #34495e;
            --accent-color: #2980b9;
            --text-color: #333;
            --light-bg: #f9f9f9;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            color: var(--text-color);
            line-height: 1.6;
        }
        
        .header-container {
            background-color: var(--primary-color);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .university-header {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            padding: 10px;
            flex-wrap: wrap;
        }
        
        .university-logo {
            height: 80px;
            transition: transform 0.3s;
        }
        
        .university-logo:hover {
            transform: scale(1.05);
        }
        
        .site-title {
            margin: 0;
            font-size: 1.8rem;
            font-weight: 600;
            color: white;
        }
        
        .site-subtitle {
            margin: 5px 0 0;
            font-size: 1rem;
            font-weight: 300;
            opacity: 0.9;
        }
        
        nav {
            background-color: var(--secondary-color);
            padding: 12px 0;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 12px;
            padding: 8px 15px;
            border-radius: 25px;
            transition: all 0.3s;
            font-size: 0.95rem;
        }
        
        nav a:hover {
            background-color: var(--accent-color);
            transform: translateY(-2px);
        }
        
        .container {
            max-width: 850px;
            margin: 30px auto;
            padding: 25px;
            background-color: white;
            box-shadow: 0 0 15px rgba(0,0,0,0.08);
            border-radius: 8px;
        }
        
        .section {
            margin: 25px 0;
            padding: 20px;
            background-color: var(--light-bg);
            border-radius: 8px;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .section:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        h2 {
            color: var(--primary-color);
            margin-top: 0;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--accent-color);
        }
        
        h3 {
            color: var(--secondary-color);
            margin-top: 25px;
        }
        
        .contact-item {
            margin: 15px 0;
            display: flex;
            align-items: center;
            padding: 10px;
            border-radius: 6px;
            transition: background-color 0.2s;
        }
        
        .contact-item:hover {
            background-color: rgba(52, 152, 219, 0.1);
        }
        
        .contact-item i {
            margin-left: 10px;
            color: var(--accent-color);
            font-size: 1.2rem;
        }
        
        footer {
            background-color: var(--primary-color);
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
            font-size: 0.9rem;
        }
        
        .page {
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .active {
            display: block;
        }
        
        .welcome-message {
            text-align: center;
            padding: 30px 20px;
        }
        
        .welcome-message h2 {
            color: var(--primary-color);
            font-size: 2rem;
            margin-bottom: 20px;
        }
        
        .welcome-message p {
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto 25px;
        }
        
        .features-list {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            width: 200px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            transition: all 0.3s;
            text-align: center;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .feature-icon {
            font-size: 2rem;
            color: var(--accent-color);
            margin-bottom: 15px;
        }
        
        form {
            margin-top: 20px;
        }
        
        input, textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        input:focus, textarea:focus {
            border-color: var(--accent-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }
        
        button[type="submit"] {
            background-color: var(--accent-color);
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        button[type="submit"]:hover {
            background-color: #2475ab;
            transform: translateY(-2px);
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }
        
        @media (max-width: 768px) {
            .university-header {
                flex-direction: column;
                text-align: center;
            }
            
            nav a {
                margin: 0 5px;
                padding: 6px 10px;
                font-size: 0.85rem;
            }
            
            .container {
                margin: 15px;
                padding: 15px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <div class="header-container">
        <div class="university-header">
            <img src="https://www.taibahu.edu.sa/ar/About/Leadership/PublishingImages/TU-Logo-02.png" 
                 alt="شعار جامعة طيبة" 
                 class="university-logo">
            <div>
                <h1 class="site-title">مشروع أنس ماجد الصبحي</h1>
                <p class="site-subtitle">جامعة طيبة - الكلية التطبيقية</p>
            </div>
        </div>
    </div>
    
    <nav>
        <a href="#" onclick="showPage('home')"><i class="fas fa-home"></i> الرئيسية</a>
        <a href="#" onclick="showPage('page1')"><i class="fas fa-user-graduate"></i> معلومات الطالب</a>
        <a href="#" onclick="showPage('page2')"><i class="fas fa-project-diagram"></i> تعريف المشروع</a>
        <a href="#" onclick="showPage('page3')"><i class="fas fa-envelope"></i> اتصل بنا</a>
    </nav>
    
    <div class="container">
        <!-- الصفحة الرئيسية -->
        <div id="home" class="page active">
            <div class="welcome-message">
                <h2>مرحباً بكم في موقع مشروعي</h2>
                <p>يسعدني أن أقدم لكم من خلال هذا الموقع مشروعي الأكاديمي الذي يمثل ثمرة جهودي وتعلمي خلال مسيرتي الجامعية.</p>
                <p>يمكنكم استكشاف مختلف أقسام الموقع للتعرف علي وعلى مشروعي، كما يمكنكم التواصل معي مباشرة.</p>
                
                <div class="features-list">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-user-tie"></i>
                        </div>
                        <h3>معلومات شخصية</h3>
                        <p>تعرف على معلوماتي الأكاديمية والشخصية</p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-laptop-code"></i>
                        </div>
                        <h3>تفاصيل المشروع</h3>
                        <p>استكشف أهداف ومحتوى مشروعي</p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-comments"></i>
                        </div>
                        <h3>تواصل مباشر</h3>
                        <p>تواصل معني لطرح أي استفسارات</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- الصفحة الأولى -->
        <div id="page1" class="page">
            <div class="section student-info">
                <h2><i class="fas fa-id-card"></i> معلومات الطالب</h2>
                <div style="display: flex; align-items: center; gap: 20px; flex-wrap: wrap;">
                    <div style="flex: 1; min-width: 200px;">
                        <p><strong><i class="fas fa-user"></i> الاسم الكامل:</strong> أنس ماجد عيد الصبحي</p>
                        <p><strong><i class="fas fa-id-badge"></i> الرقم الجامعي:</strong> 4610959</p>
                        <p><strong><i class="fas fa-university"></i> الكلية:</strong> الكلية التطبيقية</p>
                        <p><strong><i class="fas fa-graduation-cap"></i> الجامعة:</strong> جامعة طيبة</p>
                    </div>
                    <div style="flex: 1; text-align: center; min-width: 200px;">
                        <img src="https://via.placeholder.com/200" alt="صورة الطالب" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; border: 3px solid var(--accent-color);">
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2><i class="fas fa-user-graduate"></i> نبذة عني</h2>
                <p>أنا طالب مجتهد في الكلية التطبيقية بجامعة طيبة، أسعى دائماً لاكتساب المعرفة وتطوير مهاراتي في مجال تخصصي.</p>
                <p>أهتم بتطوير نفسي أكاديمياً وعملياً، وأؤمن بأهمية العمل الجماعي والابتكار في تحقيق النجاح.</p>
            </div>
        </div>
        
        <!-- الصفحة الثانية -->
        <div id="page2" class="page">
            <div class="section project-description">
                <h2><i class="fas fa-project-diagram"></i> مشروع إنشاء ثلاث صفحات ويب</h2>
                <p>يسرني أن أقدم لكم مشروعي الذي يمثل خطوة مهمة في رحلتي التعليمية، حيث قمت بتطوير موقع ويب متكامل يتكون من ثلاث صفحات رئيسية مترابطة.</p>
                
                <h3><i class="fas fa-list-ol"></i> مكونات المشروع:</h3>
                <ol>
                    <li><strong>صفحة معلومات الطالب:</strong> تحتوي على معلوماتي الشخصية والأكاديمية</li>
                    <li><strong>صفحة المشروع:</strong> تعرض تفاصيل وأهداف المشروع الحالي</li>
                    <li><strong>صفحة اتصل بنا:</strong> تمكن الزوار من التواصل معي مباشرة</li>
                </ol>
                
                <h3><i class="fas fa-bullseye"></i> أهداف المشروع:</h3>
                <div style="display: flex; flex-wrap: wrap; gap: 15px; margin-top: 15px;">
                    <div style="background-color: rgba(52, 152, 219, 0.1); padding: 15px; border-radius: 8px; flex: 1; min-width: 200px;">
                        <h4><i class="fas fa-laptop-code"></i> تطوير المهارات</h4>
                        <p>تطبيق المعرفة النظرية في مجال تطوير الويب عملياً</p>
                    </div>
                    <div style="background-color: rgba(52, 152, 219, 0.1); padding: 15px; border-radius: 8px; flex: 1; min-width: 200px;">
                        <h4><i class="fas fa-users"></i> تجربة المستخدم</h4>
                        <p>تصميم واجهة مستخدم سهلة الاستخدام وجذابة</p>
                    </div>
                    <div style="background-color: rgba(52, 152, 219, 0.1); padding: 15px; border-radius: 8px; flex: 1; min-width: 200px;">
                        <h4><i class="fas fa-link"></i> الربط بين الصفحات</h4>
                        <p>إنشاء نظام متكامل للتنقل بين صفحات الموقع</p>
                    </div>
                </div>
            </div>
            
            <div class="section dedication">
                <h2><i class="fas fa-heart"></i> إهداء</h2>
                <p>أهدي هذا العمل إلى كل من ساندني في رحلتي التعليمية، وبالأخص إلى الدكتور الفاضل <strong>صالح المطيري</strong> الذي كان له الفضل الكبير في توجيهي وإثراء معرفتي.</p>
                <p>كما أتوجه بالشكر إلى عائلتي وأصدقائي الذين قدموا لي الدعم المستمر طوال هذه الرحلة.</p>
            </div>
        </div>
        
        <!-- الصفحة الثالثة -->
        <div id="page3" class="page">
            <div class="section contact-info">
                <h2><i class="fas fa-envelope"></i> اتصل بنا</h2>
                <p>يسعدني تلقي استفساراتكم وملاحظاتكم حول المشروع، يمكنكم التواصل معي عبر الوسائل التالية:</p>
                
                <div class="contact-item">
                    <i class="fas fa-mobile-alt"></i>
                    <span><strong>الجوال:</strong> 0532763923</span>
                </div>
                
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span><strong>البريد الإلكتروني:</strong> TU4610959@taibahu.edu.sa</span>
                </div>
                
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span><strong>الموقع:</strong> جامعة طيبة - المدينة المنورة</span>
                </div>
                
                <h3 style="margin-top: 30px;"><i class="fas fa-paper-plane"></i> أرسل رسالة مباشرة</h3>
                <form>
                    <div style="margin-bottom: 15px;">
                        <label for="name" style="display: block; margin-bottom: 5px;"><i class="fas fa-user"></i> الاسم:</label>
                        <input type="text" id="name" placeholder="ادخل اسمك الكريم">
                    </div>
                    
                    <div style="margin-bottom: 15px;">
                        <label for="email" style="display: block; margin-bottom: 5px;"><i class="fas fa-at"></i> البريد الإلكتروني:</label>
                        <input type="email" id="email" placeholder="ادخل بريدك الإلكتروني">
                    </div>
                    
                    <div style="margin-bottom: 20px;">
                        <label for="message" style="display: block; margin-bottom: 5px;"><i class="fas fa-comment"></i> الرسالة:</label>
                        <textarea id="message" rows="5" placeholder="اكتب رسالتك هنا..."></textarea>
                    </div>
                    
                    <button type="submit">
                        <i class="fas fa-paper-plane"></i> إرسال الرسالة
                    </button>
                </form>
            </div>
            
            <div class="section thanks">
                <h2><i class="fas fa-hands-helping"></i> كلمة شكر</h2>
                <p>أشكركم من أعماق قلبي لزيارتكم موقعي واهتمامكم بمشروعي. هذا الجهد يمثل لي خطوة مهمة في مسيرتي التعليمية والمهنية.</p>
                <p>أتطلع دائماً إلى تحسين عملي وتطوير مهاراتي، لذا فإن ملاحظاتكم واستفساراتكم تسعدني كثيراً وتساعدني على التطور.</p>
                <p>شكراً لوقتكم الكريم، وأتمنى أن تجدوا في هذا المشروع ما يفيدكم.</p>
            </div>
        </div>
    </div>
    
    <footer>
        <p>جميع الحقوق محفوظة &copy; <span id="year"></span> - أنس ماجد الصبحي</p>
        <div style="margin-top: 10px;">
            <a href="#" style="color: white; margin: 0 10px;"><i class="fab fa-twitter"></i></a>
            <a href="#" style="color: white; margin: 0 10px;"><i class="fab fa-linkedin"></i></a>
            <a href="#" style="color: white; margin: 0 10px;"><i class="fab fa-github"></i></a>
        </div>
    </footer>

    <script>
        // عرض الصفحات
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            document.getElementById(pageId).classList.add('active');
            
            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
        
        // تحديث سنة حقوق النشر
        document.getElementById('year').textContent = new Date().getFullYear();
        
        // تأثيرات عند تحميل الصفحة
        window.addEventListener('load', function() {
            setTimeout(function() {
                document.querySelector('.welcome-message').style.opacity = '1';
                document.querySelector('.welcome-message').style.transform = 'translateY(0)';
            }, 300);
        });
    </script>
</body>
</html>


