<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر ليان للقفطان المغربي الفاسي الحر</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Cinzel:wght@400;700&family=Cairo:wght@300;400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* ==========================================================================
           1. المظهر العام والألوان الذهبية الملكية (CSS Reset & Global Styles)
           ========================================================================== */
        :root {
            --gold-primary: #D4AF37;
            --gold-light: #F3E5AB;
            --gold-dark: #AA7C11;
            --dark-bg: #0B0B0B;
            --dark-surface: #1A1A1A;
            --text-light: #F5F5F5;
            --text-muted: #CCCCCC;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', 'Amiri', sans-serif;
        }

        body {
            background-color: var(--dark-bg);
            color: var(--text-light);
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* تخصيص شريط التمرير باللون الذهبي */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: var(--dark-bg);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--gold-primary);
            border-radius: 4px;
        }

        /* ==========================================================================
           2. الهيدر والشعار الخاص باسم (Layan) بتأثير ذهبي متحرك
           ========================================================================== */
        header {
            background-color: rgba(26, 26, 26, 0.95);
            border-bottom: 2px solid var(--gold-primary);
            position: sticky;
            top: 0;
            z-index: 1000;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 20px rgba(212, 175, 55, 0.1);
        }

        /* تأثير خاص جداً لاسم ليان بالفرنسية */
        .brand-layan {
            font-family: 'Cinzel', serif;
            font-size: 2.3rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 3px;
            background: linear-gradient(to right, #BF953F 0%, #FCF6BA 25%, #B38728 50%, #FBF5B7 75%, #AA7C11 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: shine 4s infinite linear;
            background-size: 200% auto;
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
            display: inline-block;
        }

        @keyframes shine {
            to { background-position: 200% center; }
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        .nav-menu a {
            color: var(--text-light);
            text-decoration: none;
            font-size: 1.1rem;
            transition: 0.3s ease;
            position: relative;
            padding-bottom: 5px;
        }

        .nav-menu a:hover, .nav-menu a.active {
            color: var(--gold-primary);
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--gold-primary);
            transition: 0.3s;
        }

        .nav-menu a:hover::after {
            width: 100%;
        }

        .header-icons {
            display: flex;
            gap: 20px;
            font-size: 1.3rem;
            cursor: pointer;
        }

        .header-icons i {
            transition: 0.3s;
            position: relative;
        }

        .header-icons i:hover {
            color: var(--gold-primary);
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -10px;
            background-color: red;
            color: white;
            font-size: 0.7rem;
            padding: 2px 6px;
            border-radius: 50%;
        }

        /* ==========================================================================
           3. الواجهة الرئيسية (Hero Section)
           ========================================================================== */
        .hero {
            height: 70vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?q=80&w=1920') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            border-bottom: 1px solid var(--gold-dark);
        }

        .hero h1 {
            font-family: 'Amiri', serif;
            font-size: 3.5rem;
            color: var(--gold-primary);
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
        }

        .hero p {
            font-size: 1.4rem;
            max-width: 800px;
            margin-bottom: 30px;
            color: var(--text-muted);
        }

        .btn-gold {
            background: linear-gradient(45deg, var(--gold-dark), var(--gold-primary));
            color: #000;
            padding: 12px 35px;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s ease;
            box-shadow: 0 4px 15px rgba(212, 175, 55, 0.4);
        }

        .btn-gold:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(212, 175, 55, 0.6);
            background: linear-gradient(45deg, var(--gold-primary), var(--gold-light));
        }

        /* ==========================================================================
           4. قسم المنتجات الضخم (400 قفطان فاسي حر)
           ========================================================================== */
        .main-container {
            padding: 50px 5%;
        }

        .section-title {
            text-align: center;
            font-family: 'Amiri', serif;
            font-size: 2.8rem;
            color: var(--gold-primary);
            margin-bottom: 15px;
            position: relative;
        }

        .section-title::after {
            content: '❖ ❖ ❖';
            display: block;
            font-size: 1.2rem;
            color: var(--gold-dark);
            margin-top: 5px;
        }

        .filter-info {
            text-align: center;
            margin-bottom: 30px;
            color: var(--text-muted);
            font-style: italic;
        }

        /* شبكة عرض المنتجات */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background-color: var(--dark-surface);
            border: 1px solid #2a2a2a;
            border-radius: 8px;
            overflow: hidden;
            transition: 0.4s ease;
            display: flex;
            flex-direction: column;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-10px);
            border-color: var(--gold-primary);
            box-shadow: 0 10px 25px rgba(212, 175, 55, 0.15);
        }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--gold-dark);
            color: #000;
            padding: 4px 10px;
            font-size: 0.8rem;
            font-weight: bold;
            border-radius: 3px;
            z-index: 10;
        }

        .product-image-container {
            position: relative;
            width: 100%;
            height: 380px;
            background-color: #111;
            overflow: hidden;
        }

        .product-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .product-card:hover .product-image {
            transform: scale(1.08);
        }

        /* طبقة حماية وعرض جمالي للصور البديلة */
        .image-placeholder-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0,0,0,0.6);
            padding: 8px;
            text-align: center;
            font-size: 0.75rem;
            color: var(--gold-light);
        }

        .product-info {
            padding: 20px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
            justify-content: space-between;
        }

        .product-title {
            font-family: 'Amiri', serif;
            font-size: 1.3rem;
            color: #fff;
            margin-bottom: 10px;
            height: 40px;
            overflow: hidden;
        }

        .product-desc {
            font-size: 0.9rem;
            color: var(--text-muted);
            margin-bottom: 15px;
            line-height: 1.4;
        }

        .product-price-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .price {
            font-size: 1.4rem;
            color: var(--gold-primary);
            font-weight: bold;
        }

        .old-price {
            font-size: 1rem;
            color: #777;
            text-decoration: line-through;
            margin-right: 8px;
        }

        .btn-buy-now {
            width: 100%;
            background-color: transparent;
            color: var(--gold-primary);
            border: 1px solid var(--gold-primary);
            padding: 10px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 4px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
        }

        .btn-buy-now:hover {
            background-color: var(--gold-primary);
            color: #000;
        }

        /* ==========================================================================
           5. نافذة الدفع وإدخال البيانات (Checkout Modal Section)
           ========================================================================== */
        .checkout-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.85);
            z-index: 2000;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            pointer-events: none;
            transition: 0.4s ease;
            padding: 20px;
        }

        .checkout-modal.active {
            opacity: 1;
            pointer-events: auto;
        }

        .checkout-content {
            background-color: var(--dark-surface);
            border: 2px solid var(--gold-primary);
            width: 100%;
            max-width: 600px;
            border-radius: 10px;
            padding: 30px;
            position: relative;
            box-shadow: 0 0 30px rgba(212, 175, 55, 0.3);
            max-height: 90vh;
            overflow-y: auto;
        }

        .close-modal {
            position: absolute;
            top: 15px;
            left: 15px;
            font-size: 1.5rem;
            color: var(--text-muted);
            cursor: pointer;
            transition: 0.3s;
        }

        .close-modal:hover {
            color: red;
        }

        .checkout-header {
            text-align: center;
            margin-bottom: 25px;
            border-bottom: 1px solid #333;
            padding-bottom: 15px;
        }

        .checkout-header h2 {
            font-family: 'Amiri', serif;
            color: var(--gold-primary);
            font-size: 2rem;
        }

        .selected-product-summary {
            background-color: rgba(0,0,0,0.3);
            border: 1px dashed var(--gold-dark);
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--gold-light);
            font-size: 0.95rem;
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            background-color: #111;
            border: 1px solid #444;
            color: #fff;
            padding: 12px;
            border-radius: 5px;
            font-size: 1rem;
            transition: 0.3s;
        }

        .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--gold-primary);
            box-shadow: 0 0 8px rgba(212, 175, 55, 0.2);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .order-submit-btn {
            width: 100%;
            background: linear-gradient(45deg, var(--gold-dark), var(--gold-primary));
            color: #000;
            padding: 14px;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
            margin-top: 10px;
        }

        .order-submit-btn:hover {
            background: linear-gradient(45deg, var(--gold-primary), var(--gold-light));
            box-shadow: 0 0 15px rgba(212, 175, 55, 0.5);
        }

        /* ==========================================================================
           6. الفوتر الختامي (Footer)
           ========================================================================== */
        footer {
            background-color: #080808;
            border-top: 1px solid var(--gold-dark);
            padding: 40px 5% 20px 5%;
            margin-top: 50px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-col h3 {
            color: var(--gold-primary);
            font-family: 'Amiri', serif;
            font-size: 1.4rem;
            margin-bottom: 20px;
            position: relative;
        }

        .footer-col h3::after {
            content: '';
            display: block;
            width: 40px;
            height: 2px;
            background-color: var(--gold-dark);
            margin-top: 5px;
        }

        .footer-col p {
            color: var(--text-muted);
            line-height: 1.6;
            font-size: 0.95rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: var(--text-muted);
            text-decoration: none;
            transition: 0.3s;
        }

        .footer-links a:hover {
            color: var(--gold-primary);
            padding-right: 5px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }

        .social-icons a {
            color: #fff;
            background-color: var(--dark-surface);
            width: 40px;
            height: 40px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 50%;
            border: 1px solid var(--gold-dark);
            transition: 0.3s;
        }

        .social-icons a:hover {
            background-color: var(--gold-primary);
            color: #000;
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #1a1a1a;
            color: var(--text-muted);
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header>
        <div class="brand-layan">Layan</div>
        <ul class="nav-menu">
            <li><a href="#" class="active">الرئيسية</a></li>
            <li><a href="#products-section">القفطان الفاسي الحُر</a></li>
            <li><a href="#about-section">أصالة فاس</a></li>
            <li><a href="#contact-section">اتصل بنا</a></li>
        </ul>
        <div class="header-icons">
            <i class="fas fa-search"></i>
            <i class="fas fa-shopping-bag"><span class="cart-count" id="cart-counter">0</span></i>
        </div>
    </header>

    <section class="hero">
        <h1>سحر الأصالة المغربية الفاسية</h1>
        <p>اكتشفوا أضخم تشكيلة ملكية من القفطان المغربي الفاسي الحر المنقوش بخيوط الذهب الخالص والحرير الصافي، صُنعت بأيدي أمهر المعلمين في العاصمة العلمية فاس بأسعار مناسبة ومدروسة.</p>
        <button class="btn-gold" onclick="document.getElementById('products-section').scrollIntoView();">تصفح التشكيلة (400 موديل)</button>
    </section>

    <main class="main-container" id="products-section">
        <h2 class="section-title">المجموعة الفاخرة الكاملة لقفاطين فاس</h2>
        <p class="filter-info">يتم حالياً عرض 400 تصميم فريد ومختلف كلياً من حيث الألوان، الخياطة، والسفيفة الفاسية الأصلية.</p>
        
        <div class="products-grid" id="dynamic-products-container">
            </div>
    </main>

    <div class="checkout-modal" id="checkout-modal-window">
        <div class="checkout-content">
            <span class="close-modal" onclick="closeCheckout()">&times;</span>
            <div class="checkout-header">
                <h2>إتمام طلب الشراء الفوري</h2>
                <p>يرجى إدخال بياناتكم بدقة ليتواصل معكم المعلم لتأكيد المقاسات والشحن</p>
            </div>
            
            <div class="selected-product-summary">
                <div>
                    <span style="color: var(--text-muted); display:block; font-size:0.85rem;">المنتج المختار:</span>
                    <strong id="modal-product-name" style="color: var(--gold-primary);">قفطان فاسي ملكي</strong>
                </div>
                <div>
                    <span style="color: var(--text-muted); display:block; font-size:0.85rem; text-align:left;">السعر:</span>
                    <strong id="modal-product-price" style="color: #fff; font-size: 1.2rem;">1200 DH</strong>
                </div>
            </div>

            <form id="purchase-form" onsubmit="handleOrderSubmit(event)">
                <div class="form-group">
                    <label for="client-name"><i class="fas fa-user"></i> الاسم الكامل:</label>
                    <input type="text" id="client-name" required placeholder="محمد الخليفي">
                </div>
                
                <div class="form-row">
                    <div class="form-group">
                        <label for="client-phone"><i class="fas fa-phone"></i> رقم الهاتف (المغرب):</label>
                        <input type="tel" id="client-phone" required placeholder="0612345678">
                    </div>
                    <div class="form-group">
                        <label for="client-city"><i class="fas fa-map-marker-alt"></i> المدينة:</label>
                        <select id="client-city" required>
                            <option value="طنجة">طنجة</option>
                            <option value="فاس">فاس</option>
                            <option value="الرباط">الرباط</option>
                            <option value="الدار البيضاء">الدار البيضاء</option>
                            <option value="مراكش">مراكش</option>
                            <option value="تطوان">تطوان</option>
                            <option value="أكادير">أكادير</option>
                            <option value="وجدة">وجدة</option>
                        </select>
                    </div>
                </div>

                <div class="form-group">
                    <label for="client-address"><i class="fas fa-home"></i> عنوان السكن بالتفصيل:</label>
                    <input type="text" id="client-address" required placeholder="الحي، رقم المنزل، الشارع...">
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label for="client-size"><i class="fas fa-cut"></i> المقاس التقريبي:</label>
                        <select id="client-size">
                            <option value="S">S (صغير)</option>
                            <option value="M" selected>M (متوسط)</option>
                            <option value="L">L (كبير)</option>
                            <option value="XL">XL (كبير جداً)</option>
                            <option value="XXL">XXL (ملكي خاص)</option>
                            <option value="custom">خياطة على المقاس (تفصيل جديد)</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="client-notes"><i class="fas fa-comment-dots"></i> ملاحظات خاصة (تعديل لون أو خيط):</label>
                        <input type="text" id="client-notes" placeholder="مثال: زيادة العقد الفاسية...">
                    </div>
                </div>

                <div style="background-color: rgba(212,175,55,0.05); padding: 12px; border-radius: 5px; border: 1px solid rgba(212,175,55,0.2); margin-bottom: 20px; font-size: 0.9rem; text-align: center; color: var(--gold-light);">
                    <i class="fas fa-truck"></i> التوصيل سريع وآمن لجميع المدن المغربية. الدفع عند الاستلام.
                </div>

                <button type="submit" class="order-submit-btn">تأكيد طلب الشراء الآن ❖</button>
            </form>
        </div>
    </div>

    <footer id="contact-section">
        <div class="footer-grid">
            <div class="footer-col">
                <h3>دار LAYAN للقفطان</h3>
                <p>عنوان التميز والأصالة في خياطة القفطان المغربي الفاسي الحر. نلتزم بالحفاظ على هويتنا المغربية العريقة وتراثنا الأصيل من فاس العتيقة إلى كل العالم.</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            <div class="footer-col">
                <h3>روابط سريعة</h3>
                <ul class="footer-links">
                    <li><a href="#">الرئيسية</a></li>
                    <li><a href="#products-section">كتالوج الـ 400 قفطان</a></li>
                    <li><a href="#">سياسة التوصيل والقياسات</a></li>
                    <li><a href="#">ضمان الجودة الفاسية الأصلية</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>خدمة الزبناء بالمغرب</h3>
                <p><i class="fas fa-phone-alt" style="color: var(--gold-primary);"></i> +212 612-345678</p>
                <p><i class="fas fa-envelope" style="color: var(--gold-primary);"></i> support@layan-caftan.ma</p>
                <p><i class="fas fa-clock" style="color: var(--gold-primary);"></i> طيلة أيام الأسبوع من 9 صباحاً إلى 10 مساءً</p>
            </div>
        </div>
        <div class="copyright">
            جميع الحقوق محفوظة &copy; 2026 | متجر ليان للقفطان الفاسي الحر الفاخر.
        </div>
    </footer>

    <script>
        // مصفوفات من الكلمات والبيانات لتوليد 400 منتج فريد بمسميات وأوصاف وأسعار وألوان وصور مختلفة كلياً
        const subTypes = ["ملكـــي", "فاســـي أصيل", "مخزنـــي عريق", "برستيج فاخر", "العروس الفاسية", "مُطرز بالصقلي الخالص", "تراثي بالزواق الفاسي", "عصري راقٍ"];
        const colors = ["ذهبي مطعم", "أخضر ملكي", "أحمر أرجواني", "أزرق نيلي", "أسود ملكي فاخر", "أبيض لؤلؤي", "وردي مخملي", "بيج مطرز بالذهب", "بنفسجي إمبراطوري", "رمادي لؤلؤي"];
        const fabricTypes = ["ثوب البروكار الفاخر", "الحرير الطبيعي الخالص", "الموبرة الحرة الممتازة", "الجوهرة الأصيلة", "الشيفون المطرز"];
        const baseImages = [
            "https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?q=80&w=500",
            "https://images.unsplash.com/photo-1617627143750-d86bc21e42bb?q=80&w=500",
            "https://images.unsplash.com/photo-1595777457583-95e059d581b8?q=80&w=500"
        ];

        let cartCounter = 0;

        // دالة توليد مصفوفة الـ 400 منتج برمجياً بطريقة ضخمة للغاية
        function generateFourHundredProducts() {
            const products = [];
            
            // حلقة تكرارية لـ 400 منتج منفصل تماماً
            for (let i = 1; i <= 400; i++) {
                // توليد عشوائي مبني على المعامل i لضمان ثبات البيانات وتنوعها الكلي
                const subType = subTypes[i % subTypes.length];
                const color = colors[i % colors.length];
                const fabric = fabricTypes[i % fabricTypes.length];
                
                // حساب الأثمنة المناسبة (تتراوح بين 1200 درهم و 3500 درهم مغربي لتكون واقعية للحر الأصيل ومناسبة)
                const price = 1200 + ((i * 17) % 2300);
                const oldPrice = Math.floor(price * 1.3);

                // هيكلة الصورة لتكون مختلفة برمجياً من مسارات الأكواد الخاصة بك (product1.jpg, product2.jpg...)
                // ووضع صورة احتياطية حقيقية للجمالية الإنشائية للموقع
                const imageSrc = `images/caftan/product${i}.jpg`;
                const fallbackImg = baseImages[i % baseImages.length];

                products.push({
                    id: i,
                    title: `قفطان فاسي ${subType} - موديل رقم ${i}`,
                    description: `قفطان مغربي أصيل مصنوع من ${fabric} بلون ${color}، مخيط بـ "السفيفة" الفاسية العريضة و"العقاد" المصنوعة يدوياً بالصقلي الحر الحقيقي.`,
                    price: price,
                    oldPrice: oldPrice,
                    image: imageSrc,
                    fallback: fallbackImg,
                    badge: i % 10 === 0 ? "الأكثر طلباً" : (i % 7 === 0 ? "جديد حُر" : "تخفيض مناسب")
                });
            }
            return products;
        }

        // دالة عرض المنتجات داخل شبكة الـ HTML بدقة واحترافية عالية
        function displayProducts() {
            const container = document.getElementById("dynamic-products-container");
            const allProducts = generateFourHundredProducts();
            
            let htmlBuffer = "";
            
            // حقن وبناء الكود للـ 400 كرت منتج
            allProducts.forEach(product => {
                htmlBuffer += `
                <div class="product-card" id="product-card-id-${product.id}">
                    <span class="product-badge">${product.badge}</span>
                    <div class="product-image-container">
                        <img class="product-image" src="${product.image}" onerror="this.onerror=null; this.src='${product.fallback}';" alt="${product.title}">
                        <div class="image-placeholder-overlay">
                            <i class="fas fa-camera"></i> صورة المنتج الفاسي الحقيقي الفريد #${product.id}
                        </div>
                    </div>
                    <div class="product-info">
                        <div>
                            <h3 class="product-title">${product.title}</h3>
                            <p class="product-desc">${product.description}</p>
                        </div>
                        <div>
                            <div class="product-price-row">
                                <span class="price">${product.price} DH</span>
                                <span class="old-price">${product.oldPrice} DH</span>
                            </div>
                            <button class="btn-buy-now" onclick="openCheckout('${product.title}', ${product.price})">
                                <i class="fas fa-shopping-cart"></i> اشتري الآن
                            </button>
                        </div>
                    </div>
                </div>
                `;
            });
            
            container.innerHTML = htmlBuffer;
        }

        // دالة فتح صفحة الدفع وإدخال معلومات المشتري
        function openCheckout(productTitle, productPrice) {
            document.getElementById("modal-product-name").innerText = productTitle;
            document.getElementById("modal-product-price").innerText = productPrice + " DH";
            
            const modal = document.getElementById("checkout-modal-window");
            modal.classList.add("active");
            document.body.style.overflow = "hidden"; // منع سكرول الخلفية
        }

        // دالة إغلاق صفحة الدفع
        function closeCheckout() {
            const modal = document.getElementById("checkout-modal-window");
            modal.classList.remove("active");
            document.body.style.overflow = "auto";
        }

        // دالة إرسال استمارة الشراء وتأكيد البيانات
        function handleOrderSubmit(event) {
            event.preventDefault();
            
            const name = document.getElementById("client-name").value;
            const phone = document.getElementById("client-phone").value;
            const city = document.getElementById("client-city").value;
            const address = document.getElementById("client-address").value;
            const size = document.getElementById("client-size").value;
            const product = document.getElementById("modal-product-name").innerText;
            
            // محاكاة إرسال ناجح للبيانات وتأكيدها للمستخدم بنجاح تام
            alert(`تـــم استلام طلبك بنجاح يا ${name}! \n\nتفاصيل الطلب المستلم:\n- المنتج: ${product}\n- المدينة: ${city}\n- الهاتف: ${phone}\n- المقاس: ${size}\n\nسيقوم المعلم الخياط من مدينة فاس بالاتصال بك فوراً لتأكيد المقاسات النهائية وشحن قفطانك الحُر.`);
            
            // زيادة عدد المشتريات في السلة كشكل جمالي تفعيلي
            cartCounter++;
            document.getElementById("cart-counter").innerText = cartCounter;
            
            // تفريغ النموذج وإغلاق النافذة
            document.getElementById("purchase-form").reset();
            closeCheckout();
        }

        // تشغيل توليد البيانات الضخمة للمنتجات فور تحميل الصفحة بالكامل
        window.addEventListener("DOMContentLoaded", () => {
            displayProducts();
        });
    </script>
</body>
</html>
