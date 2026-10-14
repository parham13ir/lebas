<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بوتیک استایل | فروشگاه آنلاین پوشاک</title>
    <!-- فونت وزیرمتن -->
    <link href="https://cdn.jsdelivr.net/gh/rastikerdar/vazirmatn@v33.003/Vazirmatn-font-face.css" rel="stylesheet" type="text/css" />
    <style>
        * {
            box-sizing: border-box;
            transition: all 0.3s ease;
        }

        body {
            font-family: 'Vazirmatn', Tahoma, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #222;
        }

        /* هدر بوتیک */
        header {
            background: linear-gradient(135deg, #111, #333);
            color: #fff;
            text-align: center;
            padding: 50px 20px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }

        header h1 {
            margin: 0;
            font-size: 34px;
            letter-spacing: 1px;
        }

        header p {
            margin: 10px 0 0;
            color: #aaa;
            font-size: 16px;
        }

        /* منوی ناوبری */
        nav {
            background: #fff;
            text-align: center;
            padding: 15px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav a {
            color: #111;
            margin: 0 20px;
            text-decoration: none;
            font-weight: bold;
            font-size: 15px;
        }

        nav a:hover {
            color: #d32f2f;
            border-bottom: 2px solid #d32f2f;
            padding-bottom: 3px;
        }

        /* بخش اصلی */
        section {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
            text-align: center;
        }

        h2 {
            font-size: 28px;
            color: #111;
            margin-bottom: 10px;
        }

        /* کادر جستجو */
        #searchBox {
            width: 100%;
            max-width: 500px;
            padding: 14px 20px;
            margin: 25px auto 40px auto;
            border: 2px solid #eee;
            border-radius: 30px;
            font-size: 16px;
            outline: none;
            background: #fff;
            box-shadow: 0 4px 15px rgba(0,0,0,0.03);
            display: block;
            font-family: 'Vazirmatn';
        }

        #searchBox:focus {
            border-color: #111;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
        }

        /* شبکه محصولات (Grid) */
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 30px;
        }

        /* کارت محصول */
        .product-item {
            background: #fff;
            border-radius: 16px;
            overflow: hidden;
            border: 1px solid #eaeaea;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
            text-align: right;
            display: flex;
            flex-direction: column;
        }

        .product-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            border-color: #ddd;
        }

        /* بخش جایگزین عکس با طراحی گرافیکی شیک */
        .product-img-box {
            width: 100%;
            height: 240px;
            background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 75px;
            border-bottom: 1px solid #eee;
        }

        .product-content {
            padding: 20px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .product-item h3 {
            margin: 0 0 10px 0;
            font-size: 18px;
            color: #222;
        }

        .price {
            color: #d32f2f;
            font-weight: bold;
            font-size: 18px;
            margin-bottom: 15px;
        }

        .order-btn {
            width: 100%;
            padding: 12px;
            background: #111;
            color: #fff;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-family: 'Vazirmatn';
            font-weight: bold;
            font-size: 14px;
            margin-top: auto;
        }

        .order-btn:hover {
            background: #d32f2f;
        }

        /* فرم ثبت سفارش */
        .order-container {
            background: #fff;
            border-radius: 20px;
            max-width: 550px;
            margin: 60px auto;
            padding: 45px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.06);
            border: 1px solid #f0f0f0;
            text-align: right;
        }

        .order-container h2 {
            text-align: center;
            color: #111;
            margin-bottom: 25px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label { display: block; margin-bottom: 8px; font-weight: bold; color: #444; }

        input, select, textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 10px;
            font-family: 'Vazirmatn';
            font-size: 15px;
            background: #fafafa;
            box-sizing: border-box;
        }

        input:focus, select:focus, textarea:focus {
            border-color: #111;
            background: #fff;
            outline: none;
            box-shadow: 0 0 0 3px rgba(0,0,0,0.05);
        }

        textarea {
            resize: vertical;
            height: 90px;
        }

        .submit-btn {
            width: 100%;
            margin-top: 10px;
            padding: 14px;
            background: #111;
            color: #fff;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        .submit-btn:hover {
            background: #d32f2f;
        }

        #orderResult {
            display: none;
            margin-top: 20px;
            padding: 15px;
            border-radius: 10px;
            font-weight: bold;
            text-align: center;
            animation: fadeIn 0.5s ease;
        }

        .success-msg { background: #e8f5e9; color: #2e7d32; border: 1px solid #a5d6a7; }
        .error-msg { background: #ffebee; color: #c62828; border: 1px solid #ef9a9a; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        footer {
            text-align: center;
            padding: 30px;
            background: #111;
            color: #888;
            margin-top: 80px;
            font-size: 14px;
        }
    </style>
</head>
<body>

    <header>
        <h1>بوتیک استایل 🧥</h1>
        <p>جدیدترین و شیک‌ترین پوشاک روز دنیا با کیفیت عالی</p>
    </header>

    <nav>
        <a href="#">صفحه اصلی</a>
        <a href="#shop">محصولات</a>
        <a href="#order">ثبت سفارش</a>
    </nav>

    <section id="shop">
        <h2>کلکسیون پوشاک</h2>
        <p style="color: #666; margin-bottom: 10px;">محصول مورد نظر خود را جستجو کنید و سفارش دهید.</p>

        <input type="text" id="searchBox" placeholder="جستجوی هودی، کت، پیراهن، شلوار...">

        <div class="products">
            <div class="product-item">
                <div class="product-img-box">🧥</div>
                <div class="product-content">
                    <h3>کت چرم مردانه کلاسیک</h3>
                    <span class="price">۱,۴۵۰,۰۰۰ تومان</span>
                    <button class="order-btn" onclick="selectProduct('کت چرم مردانه کلاسیک')">انتخاب سفارش</button>
                </div>
            </div>

            <div class="product-item">
                <div class="product-img-box">👕</div>
                <div class="product-content">
                    <h3>هودی لش مشکی اسپرت</h3>
                    <span class="price">۶۸۰,۰۰۰ تومان</span>
                    <button class="order-btn" onclick="selectProduct('هودی لش مشکی اسپرت')">انتخاب سفارش</button>
                </div>
            </div>

            <div class="product-item">
                <div class="product-img-box">👔</div>
                <div class="product-content">
                    <h3>تیشرت لانگ نخی طرح‌دار</h3>
                    <span class="price">۳۵۰,۰۰۰ تومان</span>
                    <button class="order-btn" onclick="selectProduct('تیشرت لانگ نخی طرح‌دار')">انتخاب سفارش</button>
                </div>
            </div>

            <div class="product-item">
                <div class="product-img-box">👖</div>
                <div class="product-content">
                    <h3>شلوار جین زغالی جذب</h3>
                    <span class="price">۸۵۰,۰۰۰ تومان</span>
                    <button class="order-btn" onclick="selectProduct('شلوار جین زغالی جذب')">انتخاب سفارش</button>
                </div>
            </div>

            <div class="product-item">
                <div class="product-img-box">🧥</div>
                <div class="product-content">
                    <h3>بارانی بلند شیک زنانه</h3>
                    <span class="price">۱,۲۰۰,۰۰۰ تومان</span>
                    <button class="order-btn" onclick="selectProduct('بارانی بلند شیک زنانه')">انتخاب سفارش</button>
                </div>
            </div>

            <div class="product-item">
                <div class="product-img-box">👗</div>
                <div class="product-content">
                    <h3>پیراهن مجلسی مینیمال</h3>
                    <span class="price">۹۵۰,۰۰۰ تومان</span>
                    <button class="order-btn" onclick="selectProduct('پیراهن مجلسی مینیمال')">انتخاب سفارش</button>
                </div>
            </div>
        </div>
    </section>

    <!-- فرم ثبت سفارش -->
    <div id="order" style="padding-top: 20px;">
        <div class="order-container">
            <h2>فرم ثبت سفارش و ارسال پستی</h2>

            <form id="orderForm">
                <div class="form-group">
                    <label>نام و نام خانوادگی:</label>
                    <input type="text" id="customerName" placeholder="مثلاً: علی رضایی">
                </div>

                <div class="form-group">
                    <label>شماره تماس:</label>
                    <input type="tel" id="customerPhone" placeholder="مثلاً: 09123456789">
                </div>

                <div class="form-group">
                    <label>محصول انتخابی:</label>
                    <select id="productSelect">
                        <option value="">-- لطفاً یک محصول انتخاب کنید --</option>
                        <option>کت چرم مردانه کلاسیک</option>
                        <option>هودی لش مشکی اسپرت</option>
                        <option>تیشرت لانگ نخی طرح‌دار</option>
                        <option>شلوار جین زغالی جذب</option>
                        <option>بارانی بلند شیک زنانه</option>
                        <option>پیراهن مجلسی مینیمال</option>
                    </select>
                </div>

                <div class="form-group">
                    <label>سایز:</label>
                    <select id="sizeSelect">
                        <option>Small (S)</option>
                        <option>Medium (M)</option>
                        <option>Large (L)</option>
                        <option>XLarge (XL)</option>
                    </select>
                </div>

                <div class="form-group">
                    <label>تعداد:</label>
                    <input type="number" id="quantity" value="1" min="1">
                </div>

                <div class="form-group">
                    <label>آدرس دقیق پستی:</label>
                    <textarea id="customerAddress" placeholder="استان، شهر، خیابان، کوچه، پلاک، واحد"></textarea>
                </div>

                <div class="form-group">
                    <label>کد پستی (۱۰ رقمی):</label>
                    <input type="text" id="customerPostalCode" placeholder="مثلاً: 1234567890" maxlength="10">
                </div>

                <button type="submit" class="submit-btn">ثبت نهایی سفارش و ارسال 📦</button>
            </form>

            <div id="orderResult"></div>
        </div>
    </div>

    <footer>
        <p>تمامی حقوق محفوظ است | بوتیک استایل 🧥</p>
    </footer>

    <script>
        const searchBox = document.getElementById("searchBox");
        const items = document.getElementsByClassName("product-item");

        searchBox.addEventListener("keyup", function() {
            let filter = searchBox.value.toLowerCase().trim();
            for (let i = 0; i < items.length; i++) {
                let text = items[i].textContent.toLowerCase();
                if (text.includes(filter)) {
                    items[i].style.display = "flex";
                } else {
                    items[i].style.display = "none";
                }
            }
        });

        function selectProduct(name) {
            document.getElementById("productSelect").value = name;
            document.getElementById("order").scrollIntoView({ behavior: "smooth" });
        }

        const form = document.getElementById("orderForm");
        const resultBox = document.getElementById("orderResult");

        form.addEventListener("submit", function(event) {
            event.preventDefault();

            const name = document.getElementById("customerName").value.trim();
            const phone = document.getElementById("customerPhone").value.trim();
            const product = document.getElementById("productSelect").value;
            const size = document.getElementById("sizeSelect").value;
            const qty = document.getElementById("quantity").value;
            const address = document.getElementById("customerAddress").value.trim();
            const postalCode = document.getElementById("customerPostalCode").value.trim();

            resultBox.style.display = "block";

            if (name === "" || phone === "" || product === "" || address === "" || postalCode === "") {
                resultBox.className = "error-msg";
                resultBox.textContent = "⚠️ لطفاً تمامی فیلدها از جمله آدرس و کد پستی را به دقت پر کنید.";
                return;
            }

            resultBox.className = "success-msg";
            resultBox.innerHTML = `🎉 تبریک <b>${name}</b> عزیز!<br>سفارش ${qty} عدد <b>${product}</b> (سایز: ${size}) ثبت شد.<br>پستی به آدرس ثبت‌شده ارسال خواهد شد.`;
            
            form.reset();
        });
    </script>

</body>
</html>
