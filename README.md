<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VIORA | فيورا - الأناقة والفخامة الرقمية</title>
    <!-- استدعاء خطوط مميزة من Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;800&family=Playfair+Display:ital,wght@0,600;1,400&display=swap" rel="stylesheet">
    <!-- FontAwesome للأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --bg-primary: #0a1118;
            --bg-secondary: #0f1c2e;
            --accent-gold: #d4af37;
            --accent-gold-light: #f3e5ab;
            --text-light: #f8f9fa;
            --text-dim: #a0aec0;
            --card-border: rgba(212, 175, 55, 0.2);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-light);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* خلفية توهج أنيقة */
        .glow-bg {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.08) 0%, rgba(10, 17, 24, 0) 70%);
            z-index: -1;
            pointer-events: none;
        }

        /* الهيدر وشعار الموقع */
        header {
            padding: 2rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--card-border);
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(10, 17, 24, 0.85);
        }

        .logo-container {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo-img {
            width: 45px;
            height: 45px;
            object-fit: contain;
        }

        .logo-text {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 700;
            letter-spacing: 2px;
            background: linear-gradient(135deg, #fff 0%, var(--accent-gold) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* القسم الرئيسي (Hero Section) */
        .hero {
            min-height: 85vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 4rem 1rem;
            position: relative;
        }

        .brand-badge {
            padding: 6px 18px;
            border: 1px solid var(--accent-gold);
            border-radius: 50px;
            color: var(--accent-gold);
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
            letter-spacing: 1px;
            background: rgba(212, 175, 55, 0.05);
        }

        .hero h1 {
            font-size: clamp(2.2rem, 5vw, 4rem);
            font-weight: 800;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero h1 span {
            color: var(--accent-gold);
            font-family: 'Playfair Display', serif;
        }

        .hero p {
            max-width: 650px;
            color: var(--text-dim);
            font-size: 1.15rem;
            margin-bottom: 2.5rem;
        }

        /* معرض المنتجات/الصور القابلة للتعديل */
        .showcase {
            width: 100%;
            max-width: 1000px;
            margin: 2rem auto 4rem auto;
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid var(--card-border);
            box-shadow: 0 20px 40px rgba(0,0,0,0.5);
        }

        .showcase-img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }

        .showcase:hover .showcase-img {
            transform: scale(1.02);
        }

        /* قسم منصات التواصل التفاعلية */
        .social-section {
            max-width: 900px;
            margin: 0 auto 5rem auto;
            padding: 0 1.5rem;
        }

        .section-title {
            text-align: center;
            font-size: 1.8rem;
            margin-bottom: 2rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 2px;
            background: var(--accent-gold);
            margin: 10px auto 0 auto;
        }

        .social-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        /* بطاقات مبتكرة للتواصل الاجتماعي */
        .social-card {
            background: var(--bg-secondary);
            border: 1px solid var(--card-border);
            padding: 2rem;
            border-radius: 16px;
            text-decoration: none;
            color: var(--text-light);
            display: flex;
            align-items: center;
            justify-content: space-between;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            overflow: hidden;
        }

        .social-card::before {
            content: '';
            position: absolute;
            top: 0;
            right: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(212, 175, 55, 0.1), transparent);
            transition: right 0.6s ease;
        }

        .social-card:hover::before {
            right: 100%;
        }

        .social-card:hover {
            transform: translateY(-8px);
            border-color: var(--accent-gold);
            box-shadow: 0 10px 25px rgba(212, 175, 55, 0.15);
        }

        .social-info {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .social-icon {
            font-size: 2rem;
            color: var(--accent-gold);
            width: 50px;
            height: 50px;
            background: rgba(212, 175, 55, 0.1);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .social-details h3 {
            font-size: 1.2rem;
            font-weight: 600;
        }

        .social-details p {
            font-size: 0.85rem;
            color: var(--text-dim);
        }

        .action-arrow {
            font-size: 1.2rem;
            color: var(--accent-gold);
            transition: transform 0.3s ease;
        }

        .social-card:hover .action-arrow {
            transform: translateX(-5px);
        }

        /* الفوتر */
        footer {
            text-align: center;
            padding: 2rem;
            border-top: 1px solid var(--card-border);
            color: var(--text-dim);
            font-size: 0.9rem;
        }

        /* تجاوب مع الشاشات الصغيرة */
        @media (max-width: 768px) {
            header {
                padding: 1.5rem 4%;
            }
            .hero h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>

    <div class="glow-bg"></div>

    <!-- الهيدر الرئيسي -->
    <header>
        <div class="logo-container">
            <!-- يمكنك تغيير صورة اللوجو هنا -->
            <img src="https://via.placeholder.com/100x100/0a1118/d4af37?text=V" alt="VIORA Logo" class="logo-img">
            <div class="logo-text">VIORA</div>
        </div>
    </header>

    <!-- قسم العرض الرئيسي -->
    <section class="hero">
        <div class="brand-badge">أناقة · عمق · أصالة</div>
        <h1>علامة <span>VIORA</span> التجاريّة</h1>
        <p>أكثر من مجرد منتج... براند يرافق ذوقك في مختلف المجالات. جودة تستحقها، وتنوع يليق بك.</p>

        <!-- صورة استعراض الهوية الرئيسية (يمكنك تبديل رابط الرابط بأي صورة من اختيارك) -->
        <div class="showcase">
            <img src="https://via.placeholder.com/1000x550/0f1c2e/d4af37?text=VIORA+Brand+Identity" alt="VIORA Showcase" class="showcase-img">
        </div>
    </section>

    <!-- قسم المنصات الاجتماعية بضغطة زر -->
    <section class="social-section">
        <h2 class="section-title">تواصل معنا مباشرًة</h2>
        <div class="social-grid">
            
            <!-- رابط الإنستغرام -->
            <a href="https://www.instagram.com/vioraomn?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==" target="_blank" class="social-card">
                <div class="social-info">
                    <div class="social-icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <div class="social-details">
                        <h3>إنستغرام</h3>
                        <p>@vioraomn</p>
                    </div>
                </div>
                <div class="action-arrow">
                    <i class="fas fa-arrow-left"></i>
                </div>
            </a>

            <!-- رابط اللينكدإن -->
            <a href="https://www.linkedin.com/company/viorabrand/?lipi=urn%3Ali%3Apage%3Ad_flagship3_search_srp_companies%3Bkj%2B28iaYSyaR88r2C3BzNw%3D%3D" target="_blank" class="social-card">
                <div class="social-info">
                    <div class="social-icon">
                        <i class="fab fa-linkedin-in"></i>
                    </div>
                    <div class="social-details">
                        <h3>لينكدإن</h3>
                        <p>VIORA Brand</p>
                    </div>
                </div>
                <div class="action-arrow">
                    <i class="fas fa-arrow-left"></i>
                </div>
            </a>

        </div>
    </section>

    <!-- الفوتر -->
    <footer>
        <p>جميع الحقوق محفوظة &copy; 2026 VIORA | تصميم الهوية الرقمية</p>
    </footer>

</body>
</html>
