<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>琀海王水產 | 平價超級市場</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
        }

        body {
            background-color: #f8fafc;
            color: #1e293b;
            line-height: 1.6;
        }

        /* 導覽列 */
        header {
            background: linear-gradient(135deg, #003366 0%, #0055b8 100%);
            color: white;
            padding: 1rem 1.5rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.15);
            gap: 0.8rem;
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 800;
            letter-spacing: 1px;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        nav {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        nav a {
            color: #e0f2fe;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.2s;
            white-space: nowrap;
        }

        nav a:hover {
            color: #ffffff;
            text-decoration: underline;
        }

        /* 首頁 Hero 區塊 */
        .hero {
            background: linear-gradient(180deg, #0055b8 0%, #003366 100%);
            color: white;
            padding: 3.5rem 1.5rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.2rem;
            margin-bottom: 0.8rem;
            font-weight: 800;
        }

        .hero p {
            font-size: 1.05rem;
            opacity: 0.95;
            max-width: 650px;
            margin: 0 auto 1.5rem;
            line-height: 1.8;
        }

        .badge {
            display: inline-block;
            background-color: rgba(255, 255, 255, 0.2);
            color: #ffffff;
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
            margin-bottom: 1rem;
            backdrop-filter: blur(4px);
        }

        /* 主區塊 Container */
        .container {
            max-width: 1000px;
            margin: 2.5rem auto;
            padding: 0 1.2rem;
        }

        .section-title {
            text-align: center;
            font-size: 1.6rem;
            margin-bottom: 1.8rem;
            color: #0f172a;
        }

        /* 當季嚴選商品格線 */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.2rem;
        }

        .card {
            background: white;
            border-radius: 14px;
            padding: 1.5rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
            text-align: center;
            transition: transform 0.2s;
        }

        .card:hover {
            transform: translateY(-3px);
        }

        .card-tag {
            background: #e0f2fe;
            color: #0369a1;
            font-size: 0.75rem;
            padding: 0.2rem 0.6rem;
            border-radius: 6px;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 0.6rem;
        }

        .card h3 {
            margin-bottom: 0.5rem;
            color: #0055b8;
            font-size: 1.2rem;
        }

        .card p {
            color: #64748b;
            font-size: 0.9rem;
        }

        /* 門市資訊區塊 */
        .info-section {
            background: white;
            border-radius: 14px;
            padding: 1.8rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
            margin-top: 2.5rem;
            border: 1px solid #e2e8f0;
        }

        .info-text h3 {
            font-size: 1.4rem;
            margin-bottom: 1.2rem;
            color: #0055b8;
            border-bottom: 2px solid #f1f5f9;
            padding-bottom: 0.5rem;
        }

        .info-detail {
            margin-bottom: 0.8rem;
            font-size: 0.95rem;
            color: #334155;
        }

        .btn-group {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
            margin-top: 1.5rem;
        }

        .btn {
            display: block;
            width: 100%;
            text-align: center;
            padding: 0.9rem;
            border-radius: 10px;
            text-decoration: none;
            font-weight: bold;
            transition: opacity 0.2s;
        }

        .btn-primary {
            background-color: #0055b8;
            color: white;
            box-shadow: 0 4px 8px rgba(0, 85, 184, 0.25);
        }

        .btn-fb {
            background-color: #1877f2;
            color: white;
            box-shadow: 0 4px 8px rgba(24, 119, 242, 0.25);
        }

        .btn-ig {
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            color: white;
            box-shadow: 0 4px 8px rgba(220, 39, 67, 0.25);
        }

        .btn:hover {
            opacity: 0.9;
        }

        /* 頁尾 */
        footer {
            text-align: center;
            padding: 2rem 1rem;
            background-color: #0f172a;
            color: #94a3b8;
            font-size: 0.85rem;
            margin-top: 3.5rem;
        }

        @media (max-width: 480px) {
            header {
                justify-content: center;
                text-align: center;
            }
            .logo {
                width: 100%;
                justify-content: center;
            }
            .hero h1 {
                font-size: 1.7rem;
            }
        }
    </style>
</head>
<body>

    <!-- 頂部導覽列 -->
    <header>
        <div class="logo">🐟 琀海王水產</div>
        <nav>
            <a href="#products">嚴選食材</a>
            <a href="#location">門市資訊</a>
        </nav>
    </header>

    <!-- 主視覺 Banner -->
    <section class="hero">
        <div class="badge">台中西屯平價超級市場</div>
        <h1>用心挑選每一份海味</h1>
        <p>鮮凍海鮮 ｜ 優質肉品 ｜ 燒烤食材 ｜ 嚴選台灣在地水產<br>從產地到餐桌，為您帶來最新鮮的食材！</p>
    </section>

    <div class="container">
        <!-- 主打商品展示 -->
        <section id="products">
            <h2 class="section-title">嚴選食材項目</h2>
            <div class="grid">
                <div class="card">
                    <span class="card-tag">嚴選水產</span>
                    <h3>鮮凍海鮮</h3>
                    <p>低溫急凍鎖住水分與鮮甜，各式當季鮮魚、干貝、蝦蟹應有盡有。</p>
                </div>
                <div class="card">
                    <span class="card-tag">在地品質</span>
                    <h3>台灣在地水產</h3>
                    <p>嚴選台灣在地新鮮海味，品質嚴格把關，吃得安心又美味。</p>
                </div>
                <div class="card">
                    <span class="card-tag">高品質肉品</span>
                    <h3>優質肉品</h3>
                    <p>精選火鍋片與精緻肉品，滿足全家大小的日常料理需求。</p>
                </div>
                <div class="card">
                    <span class="card-tag">聚會必備</span>
                    <h3>燒烤食材</h3>
                    <p>派對、露營、家庭聚會必備！多款特選燒烤食材隨心挑選。</p>
                </div>
            </div>
        </section>

        <!-- 門市資訊區塊 -->
        <section id="location" class="info-section">
            <div class="info-text">
                <h3>蒞臨門市選購</h3>
                <div class="info-detail">📍 <strong>門市地址：</strong>台中市西屯區青海路二段 211-1 號</div>
                <div class="info-detail">⏰ <strong>營業時間：</strong>上午 09:00 - 下午 09:00</div>
                <div class="info-detail">📞 <strong>服務電話：</strong>(04) 2452-8992</div>
                
                <div class="btn-group">
                    <a href="https://www.instagram.com/hanseafood168/" target="_blank" class="btn btn-ig">📸 追蹤 Instagram (hanseafood168)</a>
                    <a href="https://www.facebook.com/share/1Bi7MaykAd/?mibextid=wwXIfr" target="_blank" class="btn btn-fb">📘 前往 FB 粉絲專頁</a>
                    <a href="https://maps.app.goo.gl/SAxPaii8SZzihapP9" target="_blank" class="btn btn-primary">🗺️ 開啟 Google 地圖導航</a>
                </div>
            </div>
        </section>
    </div>

    <!-- 頁尾 -->
    <footer>
        <p>&copy; 2026 琀海王水產. All Rights Reserved.</p>
    </footer>

</body>
</html>
