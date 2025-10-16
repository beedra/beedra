
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seed Bombs - بذور الحياة</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #e8f5e9 100%);
            color: #2d3436;
        }

        .lang-switch {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
            display: flex;
            gap: 10px;
        }

        .lang-btn {
            padding: 10px 20px;
            background: #4CAF50;
            color: white;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .lang-btn:hover {
            background: #45a049;
            transform: translateY(-2px);
        }

        .lang-btn.active {
            background: #2e7d32;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .hero {
            text-align: center;
            padding: 80px 20px 60px;
        }

        h1 {
            font-size: 3.5rem;
            color: #2e7d32;
            margin-bottom: 20px;
            font-weight: 800;
        }

        .subtitle {
            font-size: 1.4rem;
            color: #558b2f;
            margin-bottom: 40px;
            font-weight: 300;
        }

        .product-section {
            background: white;
            border-radius: 30px;
            padding: 50px;
            margin: 40px 0;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
        }

        .product-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
            margin-bottom: 50px;
        }

        .product-image {
            width: 100%;
            height: 400px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 15px 35px rgba(76, 175, 80, 0.3);
            position: relative;
            overflow: hidden;
            background: #f5f5f5;
        }

        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 20px;
        }

        .product-info h2 {
            font-size: 2.5rem;
            color: #2e7d32;
            margin-bottom: 25px;
        }

        .price {
            font-size: 2.5rem;
            font-weight: 800;
            color: #4CAF50;
            margin: 25px 0;
            padding: 20px;
            background: linear-gradient(135deg, #f1f8e9, #e8f5e9);
            border-radius: 15px;
            border: 2px solid #4CAF50;
        }

        .product-info p {
            font-size: 1.15rem;
            line-height: 1.8;
            color: #555;
            margin-bottom: 20px;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin: 40px 0;
        }

        .feature-item {
            background: #f1f8e9;
            padding: 25px;
            border-radius: 15px;
            border-left: 4px solid #4CAF50;
            transition: all 0.3s ease;
        }

        .feature-item:hover {
            transform: translateX(10px);
            box-shadow: 0 5px 15px rgba(76, 175, 80, 0.2);
        }

        .feature-item h3 {
            color: #2e7d32;
            margin-bottom: 10px;
            font-size: 1.3rem;
        }

        .whatsapp-btn {
            display: inline-flex;
            align-items: center;
            gap: 15px;
            padding: 20px 40px;
            background: #25D366;
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.3rem;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(37, 211, 102, 0.3);
            margin-top: 30px;
        }

        .whatsapp-btn:hover {
            background: #20ba5a;
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 40px rgba(37, 211, 102, 0.5);
        }

        .whatsapp-icon {
            font-size: 2rem;
        }

        .cta-section {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, #4CAF50, #66bb6a);
            border-radius: 30px;
            margin: 40px 0;
            color: white;
        }

        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        [dir="rtl"] {
            direction: rtl;
            text-align: right;
        }

        [dir="rtl"] .product-grid {
            direction: rtl;
        }

        [dir="rtl"] .feature-item {
            border-left: none;
            border-right: 4px solid #4CAF50;
        }

        [dir="rtl"] .feature-item:hover {
            transform: translateX(-10px);
        }

        [dir="rtl"] h1, [dir="rtl"] h2, [dir="rtl"] h3 {
            font-family: 'Arial', sans-serif;
        }

        @media (max-width: 768px) {
            h1 { font-size: 2.2rem; }
            .product-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            .features {
                grid-template-columns: 1fr;
            }
            .product-section {
                padding: 30px 20px;
            }
            .lang-switch {
                top: 10px;
                right: 10px;
            }
            .product-image {
                height: 300px;
            }
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="lang-switch">
        <button class="lang-btn active" onclick="switchLang('fr')">Français</button>
        <button class="lang-btn" onclick="switchLang('ar')">العربية</button>
    </div>

    <div class="container">
        <!-- French Version -->
        <div id="content-fr">
            <div class="hero">
                <h1>🌱 Habba d'Amour by Beedra</h1>
                <p class="subtitle">Transformez chaque espace en jardin fleuri</p>
            </div>

            <div class="product-section">
                <div class="product-grid">
                    <div class="product-image">
                        <img src="https://scontent.ftng2-1.fna.fbcdn.net/v/t39.30808-6/565894302_122155829720849769_532804318022300059_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=127cfc&_nc_eui2=AeEXWdsnEZAM39ldtE0zjAlsS8oYuJ0UtjZLyhi4nRS2Nmk0lE62dZxF7rqiIxnbjVlIn2LZpPTNcueMhabRh1KR&_nc_ohc=mp6xKOKx3ksQ7kNvwGk6xyI&_nc_oc=Adnmy2sA7K6zaGL3GTSDkK-IgXPDiunyrAMP3NhMhHyVpRofv_zCJaH5q9lF1JNX9AM&_nc_zt=23&_nc_ht=scontent.ftng2-1.fna&_nc_gid=8ZrqGEfxTgsApLRaiLXJJg&oh=00_Aff4IppmMkd_GvCjJaWFNOWM5YoBAUcqb3Hy1xWJ1sdJBQ&oe=68F74074" alt="Habba d'Amour Seedballs">
                    </div>
                    <div class="product-info">
                        <h2>Des Graines qui Changent le Monde</h2>
                        <div class="price">399 DH</div>
                        <p>Nos Habba d'Amour sont de petites boules magiques composées d'argile naturelle, de compost riche et de graines sélectionnées. Conçues pour reverdir les espaces urbains oubliés, elles sont la solution parfaite pour ceux qui veulent contribuer à un environnement plus vert sans effort.</p>
                        <p>Simple à utiliser : lancez-les dans votre jardin, sur un terrain vague, ou n'importe quel espace qui a besoin de vie. La pluie fait le reste !</p>
                    </div>
                </div>

                <div class="features">
                    <div class="feature-item">
                        <h3>🌍 100% Écologique</h3>
                        <p>Ingrédients naturels, zéro plastique, biodégradable à 100%</p>
                    </div>
                    <div class="feature-item">
                        <h3>💚 Facile à Utiliser</h3>
                        <p>Lancez et laissez la nature faire son travail</p>
                    </div>
                    <div class="feature-item">
                        <h3>🌸 Fleurs Locales</h3>
                        <p>Graines adaptées au climat marocain</p>
                    </div>
                    <div class="feature-item">
                        <h3>🎁 Cadeau Parfait</h3>
                        <p>Idéal pour les amoureux de la nature</p>
                    </div>
                </div>
            </div>

            <div class="cta-section">
                <h2>Prêt à Verdir Votre Quartier ?</h2>
                <p style="font-size: 1.2rem; margin-bottom: 20px;">Contactez-nous sur WhatsApp pour commander vos Seed Bombs</p>
                <a href="https://wa.me/212661818302?text=Bonjour,%20je%20suis%20intéressé%20par%20Habba%20d'Amour" class="whatsapp-btn" target="_blank">
                    <span class="whatsapp-icon">📱</span>
                    Contacter sur WhatsApp
                </a>
            </div>
        </div>

        <!-- Arabic Version -->
        <div id="content-ar" class="hidden" dir="rtl">
            <div class="hero">
                <h1>🌱 حبة الحب by Beedra</h1>
                <p class="subtitle">حول كل مساحة إلى حديقة مزهرة</p>
            </div>

            <div class="product-section">
                <div class="product-grid">
                    <div class="product-info">
                        <h2>بذور تغير العالم</h2>
                        <div class="price">399 درهم</div>
                        <p>حبة الحب الخاصة بنا عبارة عن كرات سحرية صغيرة مصنوعة من الطين الطبيعي والسماد العضوي والبذور المنتقاة. مصممة لإعادة الخضرة للمساحات الحضرية المنسية، وهي الحل الأمثل لأولئك الذين يريدون المساهمة في بيئة أكثر خضرة دون جهد.</p>
                        <p>سهلة الاستخدام: ارمها في حديقتك، في أرض فارغة، أو أي مساحة تحتاج إلى حياة. المطر يقوم بالباقي!</p>
                    </div>
                    <div class="product-image">
                        <img src="https://scontent.ftng2-1.fna.fbcdn.net/v/t39.30808-6/565894302_122155829720849769_532804318022300059_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=127cfc&_nc_eui2=AeEXWdsnEZAM39ldtE0zjAlsS8oYuJ0UtjZLyhi4nRS2Nmk0lE62dZxF7rqiIxnbjVlIn2LZpPTNcueMhabRh1KR&_nc_ohc=mp6xKOKx3ksQ7kNvwGk6xyI&_nc_oc=Adnmy2sA7K6zaGL3GTSDkK-IgXPDiunyrAMP3NhMhHyVpRofv_zCJaH5q9lF1JNX9AM&_nc_zt=23&_nc_ht=scontent.ftng2-1.fna&_nc_gid=8ZrqGEfxTgsApLRaiLXJJg&oh=00_Aff4IppmMkd_GvCjJaWFNOWM5YoBAUcqb3Hy1xWJ1sdJBQ&oe=68F74074" alt="Habba d'Amour Seedballs">
                    </div>
                </div>

                <div class="features">
                    <div class="feature-item">
                        <h3>🌍 صديق للبيئة 100%</h3>
                        <p>مكونات طبيعية، بدون بلاستيك، قابل للتحلل بالكامل</p>
                    </div>
                    <div class="feature-item">
                        <h3>💚 سهل الاستخدام</h3>
                        <p>ارمي واترك الطبيعة تقوم بعملها</p>
                    </div>
                    <div class="feature-item">
                        <h3>🌸 زهور محلية</h3>
                        <p>بذور متكيفة مع المناخ المغربي</p>
                    </div>
                    <div class="feature-item">
                        <h3>🎁 هدية مثالية</h3>
                        <p>مثالية لعشاق الطبيعة</p>
                    </div>
                </div>
            </div>

            <div class="cta-section">
                <h2>هل أنت مستعد لتخضير حيك؟</h2>
                <p style="font-size: 1.2rem; margin-bottom: 20px;">اتصل بنا على واتساب لطلب قنابل البذور الخاصة بك</p>
                <a href="https://wa.me/212661818302?text=مرحبا،%20أنا%20مهتم%20بحبة%20الحب" class="whatsapp-btn" target="_blank">
                    <span class="whatsapp-icon">📱</span>
                    تواصل عبر واتساب
                </a>
            </div>
        </div>
    </div>

    <script>
        function switchLang(lang) {
            const frContent = document.getElementById('content-fr');
            const arContent = document.getElementById('content-ar');
            const buttons = document.querySelectorAll('.lang-btn');

            if (lang === 'fr') {
                frContent.classList.remove('hidden');
                arContent.classList.add('hidden');
                buttons[0].classList.add('active');
                buttons[1].classList.remove('active');
            } else {
                frContent.classList.add('hidden');
                arContent.classList.remove('hidden');
                buttons[0].classList.remove('active');
                buttons[1].classList.add('active');
            }
        }
    </script>
</body>
</html>
