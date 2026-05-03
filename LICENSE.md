[Uploading index.html…]()
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    
    <!-- ========== Google Site Verification ========== -->
    <meta name="google-site-verification" content="google8226a3cc9f9296ee.html" />
    
    <title>ZK | متجر إلكتروني - ألوان متطابقة</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #FFF8F0 0%, #F5F5F5 100%);
            padding-bottom: 70px;
        }

        /* ========== ألوان الموقع المتطابقة مع الشعار ========== */
        :root {
            --primary: #FFA500;      /* اللون الأساسي - برتقالي ZK */
            --primary-dark: #FF8C00; /* برتقالي داكن */
            --primary-light: #FFB347; /* برتقالي فاتح */
            --dark: #1A1A1A;         /* أسود فاخر */
            --dark-gray: #2A2A2A;    /* رمادي غامق */
            --light: #FFF8F0;        /* بيج فاتح */
            --white: #FFFFFF;
            --gold-light: #FFD699;   /* ذهبي فاتح */
            --danger: #dc2626;
            --success: #10b981;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, var(--dark) 0%, var(--dark-gray) 100%);
            color: white;
            padding: 12px 20px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
            border-bottom: 3px solid var(--primary);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 10px;
            flex-wrap: wrap;
        }

        .logo-container {
            display: flex;
            flex-direction: column;
            cursor: pointer;
        }

        .logo-image {
            height: 50px;
            width: auto;
            max-width: 150px;
            object-fit: contain;
        }

        .logo-text {
            font-size: 28px;
            font-weight: bold;
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .logo-slogan {
            font-size: 10px;
            color: var(--gold-light);
            margin-top: 2px;
        }

        .logo-edit-btn {
            background: rgba(255, 165, 0, 0.2);
            border: none;
            color: var(--gold-light);
            cursor: pointer;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 11px;
            display: flex;
            align-items: center;
            gap: 4px;
            transition: all 0.3s;
        }

        .logo-edit-btn:hover {
            background: rgba(255, 165, 0, 0.4);
            color: var(--primary);
        }

        .search-bar {
            flex: 1;
            display: flex;
            max-width: 350px;
        }

        .search-bar input {
            width: 100%;
            padding: 8px 12px;
            border: none;
            border-radius: 8px 0 0 8px;
            outline: none;
            background: white;
        }

        .search-bar button {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            border: none;
            padding: 8px 15px;
            border-radius: 0 8px 8px 0;
            cursor: pointer;
            color: var(--dark);
            font-weight: bold;
        }

        .currency-selector {
            background: rgba(255, 165, 0, 0.2);
            padding: 5px 10px;
            border-radius: 30px;
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 12px;
        }

        .currency-selector select {
            background: transparent;
            border: none;
            color: var(--gold-light);
            font-weight: bold;
            cursor: pointer;
            outline: none;
        }

        .cart-icon {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            padding: 6px 12px;
            border-radius: 30px;
            cursor: pointer;
            font-weight: bold;
            color: var(--dark);
            transition: transform 0.3s;
        }

        .cart-icon:hover {
            transform: scale(1.05);
        }

        /* الأقسام */
        .categories-bar {
            background: linear-gradient(135deg, var(--dark) 0%, var(--dark-gray) 100%);
            padding: 10px 15px;
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            align-items: center;
            border-bottom: 1px solid rgba(255, 165, 0, 0.3);
            overflow-x: auto;
        }

        .category-item {
            color: var(--gold-light);
            cursor: pointer;
            padding: 5px 12px;
            border-radius: 30px;
            display: flex;
            align-items: center;
            gap: 5px;
            background: rgba(255, 165, 0, 0.1);
            font-size: 13px;
            white-space: nowrap;
            transition: all 0.3s;
        }

        .category-item:hover {
            background: rgba(255, 165, 0, 0.3);
        }

        .category-item.active {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--dark);
            font-weight: bold;
        }

        /* العروض الجذابة */
        .hero-offers {
            background: linear-gradient(135deg, var(--dark) 0%, #0f0c29 50%, var(--dark-gray) 100%);
            margin: 15px;
            border-radius: 24px;
            padding: 20px;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(255, 165, 0, 0.3);
        }

        .hero-offers::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,165,0,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .hero-offers h2 {
            color: var(--primary);
            text-shadow: 0 0 10px rgba(255,165,0,0.5);
        }

        .offers-slider {
            display: flex;
            gap: 15px;
            overflow-x: auto;
            padding: 10px 5px;
        }

        .offer-slide {
            min-width: 260px;
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            cursor: pointer;
            position: relative;
            transition: transform 0.3s;
            border-top: 3px solid var(--primary);
        }

        .offer-slide:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(255,165,0,0.3);
        }

        .offer-tag {
            position: absolute;
            top: 10px;
            right: 10px;
            background: var(--danger);
            color: white;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 12px;
        }

        .offer-image {
            background: linear-gradient(135deg, var(--light) 0%, #FFE0B5 100%);
            padding: 20px;
            text-align: center;
            font-size: 60px;
        }

        .offer-details {
            padding: 12px;
            text-align: center;
        }

        .offer-old-price {
            text-decoration: line-through;
            color: #999;
        }

        .offer-new-price {
            color: var(--danger);
            font-size: 20px;
            font-weight: bold;
        }

        /* المنتجات */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
            margin: 15px;
        }

        .product-card {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            cursor: pointer;
            border-top: 3px solid var(--primary);
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(255,165,0,0.2);
        }

        .product-image {
            background: linear-gradient(135deg, var(--light) 0%, #FFE0B5 100%);
            padding: 20px;
            text-align: center;
            font-size: 64px;
        }

        .product-info {
            padding: 15px;
            text-align: center;
        }

        .product-title {
            font-size: 16px;
            font-weight: bold;
            color: var(--dark);
        }

        .product-price {
            color: var(--primary-dark);
            font-size: 20px;
            font-weight: bold;
        }

        .add-to-cart-btn {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            border: none;
            padding: 10px;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            margin-top: 10px;
            transition: transform 0.2s;
        }

        .add-to-cart-btn:hover {
            transform: scale(1.02);
        }

        /* المودالات */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: var(--white);
            border-radius: 24px;
            max-width: 500px;
            width: 90%;
            max-height: 85vh;
            overflow-y: auto;
            padding: 20px;
            border-top: 4px solid var(--primary);
        }

        .close-modal {
            float: left;
            font-size: 24px;
            cursor: pointer;
            color: #999;
            transition: color 0.3s;
        }

        .close-modal:hover {
            color: var(--danger);
        }

        .form-group {
            margin-bottom: 15px;
            text-align: right;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: var(--dark);
        }

        .form-group input, .form-group textarea, .form-group select {
            width: 100%;
            padding: 10px;
            border-radius: 12px;
            border: 1px solid #FFD699;
            outline: none;
            transition: border 0.3s;
        }

        .form-group input:focus, .form-group textarea:focus, .form-group select:focus {
            border-color: var(--primary);
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            padding: 10px;
            border: none;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            transition: transform 0.2s;
        }

        .btn-primary:hover {
            transform: scale(1.02);
        }

        .btn-danger {
            background: var(--danger);
            color: white;
            border: none;
            padding: 5px 12px;
            border-radius: 20px;
            cursor: pointer;
        }

        .admin-panel {
            background: var(--white);
            padding: 20px;
            border-radius: 20px;
            margin: 15px;
            border-right: 4px solid var(--primary);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .admin-panel h3, .admin-panel h4 {
            color: var(--dark);
        }

        .admin-form {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 10px 0;
        }

        .admin-form input, .admin-form select, .admin-form textarea {
            padding: 8px;
            border-radius: 30px;
            border: 1px solid #FFD699;
            flex: 1;
        }

        .payment-item {
            background: var(--light);
            padding: 10px;
            border-radius: 12px;
            margin: 8px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .toggle-switch {
            position: relative;
            width: 50px;
            height: 24px;
        }

        .toggle-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }

        .toggle-slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            border-radius: 34px;
            transition: 0.3s;
        }

        .toggle-slider:before {
            position: absolute;
            content: "";
            height: 18px;
            width: 18px;
            left: 3px;
            bottom: 3px;
            background-color: white;
            border-radius: 50%;
            transition: 0.3s;
        }

        input:checked + .toggle-slider {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
        }

        input:checked + .toggle-slider:before {
            transform: translateX(26px);
        }

        /* الفوتر */
        .social-footer {
            background: linear-gradient(135deg, var(--dark) 0%, var(--dark-gray) 100%);
            margin-top: 20px;
            padding: 25px 20px;
            text-align: center;
            border-top: 3px solid var(--primary);
        }

        .social-title {
            color: var(--primary);
            font-size: 18px;
            margin-bottom: 15px;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }

        .social-icon {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
            text-decoration: none;
            transition: transform 0.2s;
        }

        .social-icon:hover {
            transform: translateY(-3px);
        }

        .social-icon span:first-child {
            font-size: 32px;
        }

        .social-icon span:last-child {
            color: var(--gold-light);
            font-size: 12px;
        }

        .contact-info {
            border-top: 1px solid rgba(255, 165, 0, 0.3);
            padding-top: 15px;
            color: var(--gold-light);
            font-size: 12px;
        }

        .bottom-tabs {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(135deg, var(--dark) 0%, var(--dark-gray) 100%);
            display: flex;
            justify-content: space-around;
            padding: 8px 15px;
            border-top: 1px solid var(--primary);
            z-index: 100;
        }

        .tab-btn {
            background: none;
            border: none;
            color: var(--gold-light);
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 3px;
            cursor: pointer;
            font-size: 11px;
            transition: color 0.3s;
        }

        .tab-btn:hover {
            color: var(--primary);
        }

        @media (max-width: 768px) {
            .header {
                flex-direction: column;
                align-items: stretch;
            }
            .search-bar {
                max-width: 100%;
            }
        }
    </style>
</head>
<body>

<div class="header">
    <div class="logo-area">
        <div class="logo-container" id="logoContainer" onclick="openLogoModal()">
            <!-- سيتم عرض الشعار هنا ديناميكياً -->
        </div>
        <button class="logo-edit-btn" onclick="openLogoModal()">✏️ تعديل الشعار</button>
    </div>
    <div class="search-bar">
        <input type="text" id="searchInput" placeholder="ابحث عن منتج...">
        <button onclick="searchProducts()">🔍</button>
    </div>
    <div style="display: flex; align-items: center; gap: 8px;">
        <div class="currency-selector">
            💱 <select id="currencySelect" onchange="changeCurrency()">
                <option value="USD">🇺🇸 دولار</option>
                <option value="SAR">🇸🇦 ريال سعودي</option>
                <option value="YER">🇾🇪 ريال يمني</option>
            </select>
        </div>
        <div class="cart-icon" onclick="openCartModal()">🛒 <span id="cartCount">0</span></div>
    </div>
</div>

<div class="categories-bar" id="categoriesBar"></div>

<!-- العروض الجذابة -->
<div class="hero-offers" id="heroOffersSection">
    <div style="text-align:center; margin-bottom:15px;">
        <h2>🔥 عروض حصرية 🔥</h2>
        <p style="color: #FFD699;">خصومات تصل إلى 50% لفترة محدودة</p>
    </div>
    <div class="offers-slider" id="offersSlider"></div>
</div>

<!-- المنتجات -->
<div class="products-grid" id="productsGrid"></div>

<!-- لوحة التحكم -->
<div class="admin-panel">
    <h3>🛠️ لوحة تحكم ZK</h3>
    
    <h4>📦 إدارة المنتجات</h4>
    <div class="admin-form">
        <input type="text" id="prodTitle" placeholder="اسم المنتج">
        <input type="number" id="prodPrice" placeholder="السعر">
        <input type="text" id="prodIcon" placeholder="رمز المنتج">
        <select id="prodCategory"></select>
    </div>
    <div class="admin-form">
        <textarea id="prodDescription" rows="2" placeholder="وصف المنتج"></textarea>
    </div>
    <div class="admin-form">
        <input type="text" id="prodFeatures" placeholder="المميزات (مفصولة بفاصلة)">
    </div>
    <button class="btn-primary" onclick="addProduct()">➕ إضافة منتج</button>
    
    <hr style="margin: 15px 0;">
    
    <h4>🎁 إدارة العروض</h4>
    <div class="admin-form">
        <select id="offerProductSelect"></select>
        <input type="number" id="offerDiscount" placeholder="الخصم %">
        <input type="datetime-local" id="offerExpiry">
        <button onclick="addOffer()">➕ إضافة عرض</button>
    </div>
    
    <hr style="margin: 15px 0;">
    
    <h4>💳 إدارة طرق الدفع</h4>
    <div id="paymentMethodsListAdmin"></div>
    <div class="admin-form">
        <input type="text" id="newPaymentName" placeholder="اسم طريقة الدفع">
        <input type="text" id="newPaymentIcon" placeholder="رمز (📱)">
        <input type="text" id="newPaymentLink" placeholder="رابط الدفع">
        <button onclick="addPaymentMethod()">➕ إضافة</button>
    </div>
    
    <hr style="margin: 15px 0;">
    
    <h4>📞 إدارة طرق التواصل</h4>
    <div id="socialLinksListAdmin"></div>
    <div class="admin-form">
        <select id="socialType">
            <option value="whatsapp">واتساب</option>
            <option value="facebook">فيسبوك</option>
            <option value="instagram">إنستقرام</option>
            <option value="twitter">تويتر</option>
            <option value="email">بريد إلكتروني</option>
        </select>
        <input type="text" id="socialValue" placeholder="الرابط أو رقم الهاتف">
        <button onclick="addSocialLink()">➕ إضافة</button>
    </div>
    
    <hr style="margin: 15px 0;">
    
    <h4>📂 إضافة قسم</h4>
    <div class="admin-form">
        <input type="text" id="newCategoryName" placeholder="اسم القسم">
        <input type="text" id="newCategoryIcon" placeholder="رمز">
        <button onclick="addCategory()">➕ إضافة</button>
    </div>
    
    <button class="btn-danger" style="margin-top:15px;" onclick="resetToDefault()">🔄 استعادة الافتراضي</button>
</div>

<!-- مودال شرح المنتج -->
<div id="productModal" class="modal">
    <div class="modal-content">
        <span class="close-modal" onclick="closeProductModal()">&times;</span>
        <div id="productModalContent"></div>
        <button class="btn-primary" id="modalAddToCartBtn" style="margin-top:15px;" onclick="modalAddToCart()">➕ أضف للسلة</button>
    </div>
</div>

<!-- مودال الشعار -->
<div id="logoModal" class="modal">
    <div class="modal-content">
        <span class="close-modal" onclick="closeLogoModal()">&times;</span>
        <h3>🎨 تخصيص الشعار</h3>
        <div class="form-group">
            <label>نوع الشعار</label>
            <select id="logoType" onchange="toggleLogoType()">
                <option value="text">شعار نصي</option>
                <option value="image">شعار صوري</option>
            </select>
        </div>
        <div id="logoTextDiv">
            <div class="form-group">
                <label>نص الشعار</label>
                <input type="text" id="logoText" placeholder="ZK">
            </div>
        </div>
        <div id="logoImageDiv" style="display:none;">
            <div class="form-group">
                <label>صورة الشعار</label>
                <input type="file" id="logoImageFile" accept="image/*" onchange="previewLogoImage(this)">
                <div id="logoImagePreview" style="margin-top:10px;"></div>
            </div>
        </div>
        <div class="form-group">
            <label>الشعار السفلي (Slogan)</label>
            <input type="text" id="storeSlogan" placeholder="تسوق بسهولة">
        </div>
        <button class="btn-primary" onclick="saveLogoSettings()">💾 حفظ</button>
        <button class="btn-danger" style="margin-top:10px;" onclick="resetLogoSettings()">🔄 استعادة الافتراضي</button>
    </div>
</div>

<!-- مودال السلة -->
<div id="cartModal" class="modal">
    <div class="modal-content">
        <span class="close-modal" onclick="closeCartModal()">&times;</span>
        <h3>🛒 سلة التسوق</h3>
        <div id="cartItemsList"></div>
        <div id="cartTotal" style="font-size:18px; font-weight:bold; text-align:center; padding:15px;"></div>
        <div style="display:flex; gap:10px;">
            <button class="btn-danger" style="flex:1;" onclick="clearCart()">🗑️ تفريغ</button>
            <button class="btn-primary" style="flex:1;" onclick="checkout()">💰 إتمام الشراء</button>
        </div>
    </div>
</div>

<!-- مودال الدفع -->
<div id="paymentModal" class="modal">
    <div class="modal-content">
        <span class="close-modal" onclick="closePaymentModal()">&times;</span>
        <h3>💳 اختر طريقة الدفع</h3>
        <div id="paymentMethodsList"></div>
        <button class="btn-primary" onclick="confirmPayment()" style="margin-top:15px;">✅ تأكيد الدفع</button>
    </div>
</div>

<!-- الفوتر مع طرق التواصل -->
<div class="social-footer">
    <div class="social-title">📢 تواصل معنا</div>
    <div class="social-icons" id="socialIconsFooter"></div>
    <div class="contact-info">
        <p>© 2026 ZK | جميع الحقوق محفوظة</p>
        <p style="font-size:11px; margin-top:5px;">تسوق بسهولة، كل ما تحتاجه بين يديك</p>
    </div>
</div>

<div class="bottom-tabs">
    <button class="tab-btn active" onclick="location.reload()"><span>🏠</span><span>الرئيسية</span></button>
    <button class="tab-btn" onclick="openCartModal()"><span>🛒</span><span>السلة</span></button>
</div>

<script>
    // ========== إعدادات العملات ==========
    let exchangeRates = JSON.parse(localStorage.getItem('zk_rates')) || { USD: 1, SAR: 3.75, YER: 1500 };
    let currentCurrency = localStorage.getItem('zk_currency') || 'YER';
    
    function formatPrice(usdPrice, currency) {
        const converted = usdPrice * exchangeRates[currency];
        const symbols = { USD: '$', SAR: 'ر.س', YER: 'ر.ي' };
        if (currency === 'YER') return converted.toLocaleString() + ' ' + symbols[currency];
        return symbols[currency] + ' ' + converted.toFixed(2);
    }
    
    function changeCurrency() {
        currentCurrency = document.getElementById('currencySelect').value;
        localStorage.setItem('zk_currency', currentCurrency);
        renderProducts();
        renderOffersSlider();
        if (document.getElementById('cartModal').style.display === 'flex') openCartModal();
    }
    
    // ========== بيانات الشعار ==========
    let logoData = JSON.parse(localStorage.getItem('zk_logo')) || {
        type: 'text',
        text: 'ZK',
        image: null,
        slogan: 'تسوق بسهولة'
    };
    
    function renderLogo() {
        const container = document.getElementById('logoContainer');
        if (logoData.type === 'image' && logoData.image) {
            container.innerHTML = `<img src="${logoData.image}" class="logo-image"><div class="logo-slogan">${logoData.slogan}</div>`;
        } else {
            container.innerHTML = `<div><div class="logo-text">${logoData.text}</div><div class="logo-slogan">${logoData.slogan}</div></div>`;
        }
    }
    
    function openLogoModal() {
        document.getElementById('logoType').value = logoData.type;
        document.getElementById('logoText').value = logoData.text;
        document.getElementById('storeSlogan').value = logoData.slogan;
        toggleLogoType();
        document.getElementById('logoModal').style.display = 'flex';
    }
    
    function closeLogoModal() { document.getElementById('logoModal').style.display = 'none'; }
    
    function toggleLogoType() {
        const type = document.getElementById('logoType').value;
        document.getElementById('logoTextDiv').style.display = type === 'text' ? 'block' : 'none';
        document.getElementById('logoImageDiv').style.display = type === 'image' ? 'block' : 'none';
    }
    
    function previewLogoImage(input) {
        if (input.files && input.files[0]) {
            const reader = new FileReader();
            reader.onload = e => document.getElementById('logoImagePreview').innerHTML = `<img src="${e.target.result}" style="max-width:150px;">`;
            reader.readAsDataURL(input.files[0]);
        }
    }
    
    function saveLogoSettings() {
        const type = document.getElementById('logoType').value;
        const text = document.getElementById('logoText').value.trim();
        const slogan = document.getElementById('storeSlogan').value.trim();
        const file = document.getElementById('logoImageFile').files[0];
        
        logoData.type = type;
        if (text) logoData.text = text;
        if (slogan) logoData.slogan = slogan;
        
        if (type === 'image' && file) {
            const reader = new FileReader();
            reader.onload = e => {
                logoData.image = e.target.result;
                localStorage.setItem('zk_logo', JSON.stringify(logoData));
                renderLogo();
                closeLogoModal();
                showToast('✅ تم حفظ الشعار');
            };
            reader.readAsDataURL(file);
        } else {
            logoData.image = null;
            localStorage.setItem('zk_logo', JSON.stringify(logoData));
            renderLogo();
            closeLogoModal();
            showToast('✅ تم حفظ الشعار');
        }
    }
    
    function resetLogoSettings() {
        logoData = { type: 'text', text: 'ZK', image: null, slogan: 'تسوق بسهولة' };
        localStorage.setItem('zk_logo', JSON.stringify(logoData));
        renderLogo();
        closeLogoModal();
        showToast('🔄 تم استعادة الشعار الافتراضي');
    }
    
    // ========== بيانات طرق الدفع ==========
    let paymentMethods = JSON.parse(localStorage.getItem('zk_paymentMethods')) || [
        { id: 1, name: "STC Pay", icon: "📱", link: "https://stcpay.com.sa", enabled: true },
        { id: 2, name: "Apple Pay", icon: "🍎", link: "https://apple.com/apple-pay", enabled: true },
        { id: 3, name: "Google Pay", icon: "🤖", link: "https://pay.google.com", enabled: true },
        { id: 4, name: "تمارا", icon: "🟣", link: "https://tamara.com", enabled: true },
        { id: 5, name: "تابي", icon: "🔵", link: "https://tabby.ai", enabled: true },
        { id: 6, name: "تحويل بنكي", icon: "🏦", link: "", enabled: true }
    ];
    
    function renderPaymentMethodsAdmin() {
        const container = document.getElementById('paymentMethodsListAdmin');
        container.innerHTML = paymentMethods.map(m => `
            <div class="payment-item">
                <div><span style="font-size:24px;">${m.icon}</span> <strong>${m.name}</strong></div>
                <div style="display:flex; gap:10px; align-items:center;">
                    <label class="toggle-switch">
                        <input type="checkbox" ${m.enabled ? 'checked' : ''} onchange="togglePaymentMethod(${m.id}, this.checked)">
                        <span class="toggle-slider"></span>
                    </label>
                    <button class="btn-danger" onclick="deletePaymentMethod(${m.id})">🗑️</button>
                </div>
            </div>
        `).join('');
    }
    
    function renderPaymentMethodsList() {
        const container = document.getElementById('paymentMethodsList');
        const enabled = paymentMethods.filter(m => m.enabled);
        container.innerHTML = enabled.map(m => `
            <div onclick="selectPaymentMethod(${m.id})" style="background:#FFF8F0; border:2px solid #FFD699; border-radius:60px; padding:12px 20px; margin:10px 0; display:flex; align-items:center; gap:15px; cursor:pointer;" id="payment-${m.id}">
                <span style="font-size:28px;">${m.icon}</span>
                <div><strong>${m.name}</strong></div>
                <span style="flex:1;"></span>
                <span>➡️</span>
            </div>
        `).join('');
    }
    
    function addPaymentMethod() {
        let name = document.getElementById('newPaymentName')?.value.trim();
        let icon = document.getElementById('newPaymentIcon')?.value.trim();
        let link = document.getElementById('newPaymentLink')?.value.trim();
        if (!name) return alert("أدخل اسم طريقة الدفع");
        if (!icon) icon = "💳";
        const newId = Math.max(...paymentMethods.map(m => m.id), 0) + 1;
        paymentMethods.push({ id: newId, name, icon, link, enabled: true });
        localStorage.setItem('zk_paymentMethods', JSON.stringify(paymentMethods));
        renderPaymentMethodsAdmin();
        renderPaymentMethodsList();
        document.getElementById('newPaymentName').value = '';
        document.getElementById('newPaymentIcon').value = '';
        document.getElementById('newPaymentLink').value = '';
        showToast(`✅ تم إضافة ${name}`);
    }
    
    function togglePaymentMethod(id, enabled) {
        const method = paymentMethods.find(m => m.id === id);
        if (method) method.enabled = enabled;
        localStorage.setItem('zk_paymentMethods', JSON.stringify(paymentMethods));
        renderPaymentMethodsAdmin();
        renderPaymentMethodsList();
    }
    
    function deletePaymentMethod(id) {
        if (confirm('حذف طريقة الدفع؟')) {
            paymentMethods = paymentMethods.filter(m => m.id !== id);
            localStorage.setItem('zk_paymentMethods', JSON.stringify(paymentMethods));
            renderPaymentMethodsAdmin();
            renderPaymentMethodsList();
            showToast('✅ تم الحذف');
        }
    }
    
    // ========== بيانات طرق التواصل ==========
    let socialLinks = JSON.parse(localStorage.getItem('zk_socialLinks')) || [
        { type: "whatsapp", name: "واتساب", icon: "📱", value: "966512345678" },
        { type: "facebook", name: "فيسبوك", icon: "📘", value: "ZKStore" },
        { type: "instagram", name: "إنستقرام", icon: "📸", value: "zk_store" }
    ];
    
    function renderSocialLinks() {
        const container = document.getElementById('socialIconsFooter');
        container.innerHTML = socialLinks.map(s => {
            let link = '';
            if (s.type === 'whatsapp') link = `https://wa.me/${s.value}`;
            else if (s.type === 'facebook') link = `https://facebook.com/${s.value}`;
            else if (s.type === 'instagram') link = `https://instagram.com/${s.value}`;
            else if (s.type === 'twitter') link = `https://twitter.com/${s.value}`;
            else if (s.type === 'email') link = `mailto:${s.value}`;
            return `<a href="${link}" target="_blank" class="social-icon"><span>${s.icon}</span><span>${s.name}</span></a>`;
        }).join('');
        
        const containerAdmin = document.getElementById('socialLinksListAdmin');
        containerAdmin.innerHTML = socialLinks.map((s, idx) => `
            <div class="payment-item">
                <div><span style="font-size:24px;">${s.icon}</span> <strong>${s.name}</strong><br><small>${s.value}</small></div>
                <button class="btn-danger" onclick="deleteSocialLink(${idx})">🗑️ حذف</button>
            </div>
        `).join('');
    }
    
    function addSocialLink() {
        const type = document.getElementById('socialType').value;
        const value = document.getElementById('socialValue').value.trim();
        if (!value) return alert("أدخل الرابط أو رقم الهاتف");
        const names = { whatsapp: "واتساب", facebook: "فيسبوك", instagram: "إنستقرام", twitter: "تويتر", email: "بريد إلكتروني" };
        const icons = { whatsapp: "📱", facebook: "📘", instagram: "📸", twitter: "🐦", email: "📧" };
        socialLinks.push({ type, name: names[type], icon: icons[type], value });
        localStorage.setItem('zk_socialLinks', JSON.stringify(socialLinks));
        renderSocialLinks();
        document.getElementById('socialValue').value = '';
        showToast(`✅ تم إضافة ${names[type]}`);
    }
    
    function deleteSocialLink(index) {
        socialLinks.splice(index, 1);
        localStorage.setItem('zk_socialLinks', JSON.stringify(socialLinks));
        renderSocialLinks();
        showToast('✅ تم الحذف');
    }
    
    // ========== البيانات الأساسية ==========
    let cart = JSON.parse(localStorage.getItem('zk_cart')) || [];
    let categories = JSON.parse(localStorage.getItem('zk_categories')) || [
        { id: 1, name: "الكل", icon: "✨" },
        { id: 2, name: "الكترونيات", icon: "📱" },
        { id: 3, name: "موضة", icon: "👗" },
        { id: 4, name: "منزل", icon: "🏠" }
    ];
    let offers = JSON.parse(localStorage.getItem('zk_offers')) || [];
    
    let products = JSON.parse(localStorage.getItem('zk_products'));
    if (!products || products.length === 0) {
        products = [
            { id: 1, title: "هاتف ZK Ultra", price: 599, icon: "📱", category: "الكترونيات", description: "هاتف ذكي متطور", features: ["شاشة AMOLED", "بطارية 5000mAh"] },
            { id: 2, title: "سماعات لاسلكية", price: 79, icon: "🎧", category: "الكترونيات", description: "سماعات عالية الجودة", features: ["بلوتوث 5.2", "عزل ضوضاء"] },
            { id: 3, title: "تيشيرت قطني", price: 29, icon: "👕", category: "موضة", description: "تيشيرت مريح", features: ["قطن 100%"] },
            { id: 4, title: "ساعة رياضية", price: 149, icon: "⌚", category: "الكترونيات", description: "ساعة ذكية", features: ["GPS", "مقاومة للماء"] }
        ];
        saveProducts();
    }
    
    let currentCategory = "الكل";
    let nextId = Math.max(...products.map(p => p.id), 0) + 1;
    let selectedPaymentId = null;
    let currentProductId = null;
    
    function saveProducts() { localStorage.setItem('zk_products', JSON.stringify(products)); }
    function saveCart() { localStorage.setItem('zk_cart', JSON.stringify(cart)); updateCartCount(); }
    function saveCategories() { localStorage.setItem('zk_categories', JSON.stringify(categories)); }
    function saveOffers() { localStorage.setItem('zk_offers', JSON.stringify(offers)); }
    function updateCartCount() { document.getElementById('cartCount').innerText = cart.length; }
    
    function showToast(msg) {
        const toast = document.createElement('div');
        toast.innerHTML = msg;
        toast.style.position = 'fixed';
        toast.style.bottom = '100px';
        toast.style.left = '20px';
        toast.style.right = '20px';
        toast.style.background = '#1A1A1A';
        toast.style.color = 'white';
        toast.style.padding = '12px';
        toast.style.borderRadius = '30px';
        toast.style.textAlign = 'center';
        toast.style.zIndex = '1000';
        toast.style.border = '1px solid #FFA500';
        document.body.appendChild(toast);
        setTimeout(() => toast.remove(), 2500);
    }
    
    // عرض المنتجات
    function renderProducts() {
        const grid = document.getElementById('productsGrid');
        let items = products.filter(p => currentCategory === "الكل" ? true : p.category === currentCategory);
        if (items.length === 0) { grid.innerHTML = "<p style='text-align:center; padding:40px;'>لا توجد منتجات</p>"; return; }
        grid.innerHTML = items.map(p => {
            const offer = offers.find(o => o.productId === p.id && new Date(o.expiry) > new Date());
            const finalPrice = offer ? p.price * (1 - offer.discount / 100) : p.price;
            return `
                <div class="product-card" onclick="showProductDetails(${p.id})">
                    <div class="product-image">${p.icon}</div>
                    <div class="product-info">
                        <div class="product-title">${p.title}</div>
                        ${offer ? `<div style="text-decoration:line-through; color:#999; font-size:12px;">${formatPrice(p.price, currentCurrency)}</div>` : ''}
                        <div class="product-price">${formatPrice(finalPrice, currentCurrency)}</div>
                        <button class="add-to-cart-btn" onclick="event.stopPropagation(); addToCart(${p.id})">➕ أضف للسلة</button>
                    </div>
                </div>
            `;
        }).join('');
    }
    
    function showProductDetails(id) {
        const p = products.find(p => p.id === id);
        if (!p) return;
        currentProductId = id;
        const offer = offers.find(o => o.productId === id && new Date(o.expiry) > new Date());
        const finalPrice = offer ? p.price * (1 - offer.discount / 100) : p.price;
        const featuresHtml = p.features ? p.features.map(f => `<li>✓ ${f}</li>`).join('') : '<li>✓ لا توجد مميزات</li>';
        document.getElementById('productModalContent').innerHTML = `
            <div style="text-align:center; padding:10px;">
                <div style="font-size:80px;">${p.icon}</div>
                <h2>${p.title}</h2>
                <div style="font-size:24px; color:#FF8C00;">${formatPrice(finalPrice, currentCurrency)}</div>
                ${offer ? `<div style="color:#dc2626;">🔥 خصم ${offer.discount}%</div>` : ''}
                <div style="margin-top:15px; text-align:right;">
                    <h4>📝 الوصف</h4>
                    <p>${p.description || 'لا يوجد وصف'}</p>
                    <h4 style="margin-top:10px;">✨ المميزات</h4>
                    <ul style="list-style:none;">${featuresHtml}</ul>
                </div>
            </div>
        `;
        document.getElementById('productModal').style.display = 'flex';
    }
    
    function closeProductModal() { document.getElementById('productModal').style.display = 'none'; }
    function modalAddToCart() { if (currentProductId) { addToCart(currentProductId); closeProductModal(); } }
    
    function addToCart(id) {
        const p = products.find(p => p.id === id);
        const offer = offers.find(o => o.productId === id && new Date(o.expiry) > new Date());
        const finalPrice = offer ? p.price * (1 - offer.discount / 100) : p.price;
        cart.push({ id: Date.now(), title: p.title, price: finalPrice, icon: p.icon });
        saveCart();
        showToast(`✅ تم إضافة ${p.title}`);
    }
    
    function removeFromCart(index) {
        cart.splice(index, 1);
        saveCart();
        openCartModal();
        showToast(`🔄 تم إرجاع المنتج`);
    }
    
    function clearCart() {
        if (cart.length === 0) return;
        if (confirm('تفريغ السلة؟')) { cart = []; saveCart(); openCartModal(); showToast('🗑️ تم تفريغ السلة'); }
    }
    
    function openCartModal() {
        const modal = document.getElementById('cartModal');
        const cartList = document.getElementById('cartItemsList');
        const cartTotal = document.getElementById('cartTotal');
        if (cart.length === 0) {
            cartList.innerHTML = '<div style="text-align:center; padding:20px;">السلة فارغة</div>';
            cartTotal.innerHTML = '';
        } else {
            cartList.innerHTML = cart.map((item, idx) => `
                <div style="display:flex; justify-content:space-between; align-items:center; padding:12px; border-bottom:1px solid #eee;">
                    <div style="font-size:32px;">${item.icon}</div>
                    <div style="flex:1; padding:0 10px;"><strong>${item.title}</strong><br>${formatPrice(item.price, currentCurrency)}</div>
                    <button class="btn-danger" onclick="removeFromCart(${idx})">إرجاع</button>
                </div>
            `).join('');
            const total = cart.reduce((s, i) => s + i.price, 0);
            cartTotal.innerHTML = `المجموع: ${formatPrice(total, currentCurrency)}`;
        }
        modal.style.display = 'flex';
    }
    
    function closeCartModal() { document.getElementById('cartModal').style.display = 'none'; }
    
    function checkout() { if (cart.length === 0) { showToast('السلة فارغة'); return; } closeCartModal(); openPaymentModal(); }
    
    function openPaymentModal() {
        selectedPaymentId = null;
        renderPaymentMethodsList();
        document.getElementById('paymentModal').style.display = 'flex';
    }
    
    function selectPaymentMethod(id) { selectedPaymentId = id; }
    function closePaymentModal() { document.getElementById('paymentModal').style.display = 'none'; }
    
    function confirmPayment() {
        if (!selectedPaymentId) { showToast('❌ اختر طريقة الدفع'); return; }
        const method = paymentMethods.find(m => m.id === selectedPaymentId);
        const total = cart.reduce((s, i) => s + i.price, 0);
        showToast(`✅ تم الدفع عبر ${method.name} بقيمة ${formatPrice(total, currentCurrency)}`);
        cart = []; saveCart(); closePaymentModal();
    }
    
    // العروض
    function renderOffersSlider() {
        const container = document.getElementById('offersSlider');
        const valid = offers.filter(o => new Date(o.expiry) > new Date());
        if (valid.length === 0) { container.innerHTML = '<div style="color:white;">لا توجد عروض حالياً</div>'; return; }
        container.innerHTML = valid.map(o => {
            const p = products.find(p => p.id === o.productId);
            if (!p) return '';
            const newPrice = p.price * (1 - o.discount / 100);
            return `
                <div class="offer-slide" onclick="showProductDetails(${p.id})">
                    <div class="offer-tag">-${o.discount}%</div>
                    <div class="offer-image">${p.icon}</div>
                    <div class="offer-details">
                        <div class="offer-title">${p.title}</div>
                        <span class="offer-old-price">${formatPrice(p.price, currentCurrency)}</span>
                        <span class="offer-new-price">${formatPrice(newPrice, currentCurrency)}</span>
                        <button class="add-to-cart-btn" onclick="event.stopPropagation(); addToCart(${p.id})">🛒 شراء</button>
                    </div>
                </div>
            `;
        }).join('');
    }
    
    // الأقسام
    function renderCategoriesBar() {
        const bar = document.getElementById('categoriesBar');
        bar.innerHTML = categories.map(c => `<div class="category-item ${currentCategory === c.name ? 'active' : ''}" onclick="filterByCategory('${c.name}')"><span>${c.icon}</span><span>${c.name}</span></div>`).join('');
        bar.innerHTML += `<div class="category-item" onclick="document.getElementById('newCategoryName').focus()">➕ قسم</div>`;
    }
    
    function addCategory() {
        let name = document.getElementById('newCategoryName')?.value.trim();
        let icon = document.getElementById('newCategoryIcon')?.value.trim();
        if (!name) return alert("أدخل اسم القسم");
        if (!icon) icon = "📁";
        if (categories.some(c => c.name === name)) return alert("القسم موجود");
        categories.push({ id: categories.length + 1, name, icon });
        saveCategories();
        document.getElementById('newCategoryName').value = '';
        document.getElementById('newCategoryIcon').value = '';
        renderCategoriesBar();
        updateCategorySelect();
        showToast(`✅ تم إضافة قسم ${name}`);
    }
    
    function updateCategorySelect() {
        const sel = document.getElementById('prodCategory');
        if (sel) sel.innerHTML = categories.filter(c => c.name !== "الكل").map(c => `<option value="${c.name}">${c.icon} ${c.name}</option>`).join('');
    }
    
    function filterByCategory(cat) { currentCategory = cat; renderCategoriesBar(); renderProducts(); }
    
    function searchProducts() {
        const term = document.getElementById('searchInput')?.value.toLowerCase();
        const grid = document.getElementById('productsGrid');
        if (!term) { renderProducts(); return; }
        const filtered = products.filter(p => p.title.toLowerCase().includes(term));
        if (filtered.length === 0) { grid.innerHTML = "<p style='text-align:center; padding:40px;'>لا توجد نتائج</p>"; return; }
        grid.innerHTML = filtered.map(p => `<div class="product-card" onclick="showProductDetails(${p.id})"><div class="product-image">${p.icon}</div><div class="product-info"><div class="product-title">${p.title}</div><div class="product-price">${formatPrice(p.price, currentCurrency)}</div><button class="add-to-cart-btn" onclick="event.stopPropagation(); addToCart(${p.id})">➕ أضف للسلة</button></div></div>`).join('');
    }
    
    function addProduct() {
        let title = document.getElementById('prodTitle')?.value.trim();
        let price = parseFloat(document.getElementById('prodPrice')?.value);
        let icon = document.getElementById('prodIcon')?.value.trim();
        let category = document.getElementById('prodCategory')?.value;
        let description = document.getElementById('prodDescription')?.value.trim();
        let featuresStr = document.getElementById('prodFeatures')?.value.trim();
        if (!title || isNaN(price) || !icon) return alert("املأ الحقول");
        products.push({ id: nextId++, title, price, icon, category: category || "الكل", description: description || "", features: featuresStr ? featuresStr.split(',').map(f => f.trim()) : [] });
        saveProducts();
        filterByCategory(currentCategory);
        updateOfferSelect();
        showToast(`✅ تم إضافة ${title}`);
    }
    
    function addOffer() {
        const pid = parseInt(document.getElementById('offerProductSelect')?.value);
        const disc = parseInt(document.getElementById('offerDiscount')?.value);
        const exp = document.getElementById('offerExpiry')?.value;
        if (!pid || !disc || !exp) return alert("املأ الحقول");
        if (disc < 1 || disc > 90) return alert("الخصم بين 1 و 90");
        const existing = offers.find(o => o.productId === pid);
        if (existing) { existing.discount = disc; existing.expiry = exp; }
        else offers.push({ productId: pid, discount: disc, expiry: exp });
        saveOffers();
        renderOffersSlider();
        renderProducts();
        updateOfferSelect();
        showToast("✅ تم إضافة العرض");
    }
    
    function updateOfferSelect() {
        const sel = document.getElementById('offerProductSelect');
        if (sel) sel.innerHTML = products.map(p => `<option value="${p.id}">${p.title} - $${p.price}</option>`).join('');
    }
    
    function resetToDefault() { if(confirm("استعادة الإعدادات الافتراضية؟")){ localStorage.clear(); location.reload(); } }
    
    // التهيئة
    document.getElementById('currencySelect').value = currentCurrency;
    renderLogo();
    renderCategoriesBar();
    updateCategorySelect();
    updateOfferSelect();
    renderOffersSlider();
    renderProducts();
    updateCartCount();
    renderPaymentMethodsAdmin();
    renderSocialLinks();
</script>
</body>
</html>
