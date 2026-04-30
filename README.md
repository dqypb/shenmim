<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>纪念长征胜利 90 周年（1936-2026）</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-red: #C41E3A;
            --dark-red: #8B0000;
            --light-red: #E84A5F;
            --gold: #D4AF37;
            --light-gold: #F4D03F;
            --bg-cream: #F5F1E8;
            --text-dark: #2C1810;
            --text-gray: #5C4A3D;
        }

        body {
            font-family: "Microsoft YaHei", "PingFang SC", "Helvetica Neue", Arial, sans-serif;
            background: var(--bg-cream);
            color: var(--text-dark);
            line-height: 1.8;
            overflow-x: hidden;
        }

        /* 导航栏 */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: linear-gradient(135deg, var(--dark-red), var(--primary-red));
            padding: 15px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.3);
        }

            .navbar .logo {
                color: var(--gold);
                font-size: 24px;
                font-weight: bold;
                display: flex;
                align-items: center;
                gap: 10px;
            }

            .navbar .logo-star {
                font-size: 30px;
            }

            .navbar ul {
                display: flex;
                list-style: none;
                gap: 30px;
            }

                .navbar ul li a {
                    color: white;
                    text-decoration: none;
                    font-size: 15px;
                    transition: color 0.3s;
                    position: relative;
                }

                    .navbar ul li a:hover {
                        color: var(--gold);
                    }

                    .navbar ul li a::after {
                        content: '';
                        position: absolute;
                        bottom: -5px;
                        left: 0;
                        width: 0;
                        height: 2px;
                        background: var(--gold);
                        transition: width 0.3s;
                    }

                    .navbar ul li a:hover::after {
                        width: 100%;
                    }

        /* 英雄区 */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, rgba(139,0,0,0.9), rgba(196,30,58,0.8)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><pattern id="mountain" patternUnits="userSpaceOnUse" width="200" height="100"><polygon points="0,100 50,30 100,100" fill="%238B0000" opacity="0.3"/><polygon points="100,100 150,20 200,100" fill="%23C41E3A" opacity="0.3"/></pattern></defs><rect width="1000" height="1000" fill="url(%23mountain)"/></svg>');
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

            .hero::before {
                content: '';
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: radial-gradient(ellipse at center, transparent 0%, rgba(0,0,0,0.5) 100%);
            }

        .hero-content {
            position: relative;
            z-index: 1;
            animation: fadeInUp 1.5s ease;
        }

        .hero h1 {
            font-size: 72px;
            color: var(--gold);
            text-shadow: 3px 3px 6px rgba(0,0,0,0.5);
            margin-bottom: 20px;
            letter-spacing: 10px;
        }

        .hero .subtitle {
            font-size: 28px;
            color: white;
            margin-bottom: 30px;
            letter-spacing: 5px;
        }

        .hero .years {
            font-size: 48px;
            color: var(--gold);
            font-weight: bold;
            margin-bottom: 40px;
        }

        .hero .scroll-hint {
            position: absolute;
            bottom: 50px;
            left: 50%;
            transform: translateX(-50%);
            color: white;
            font-size: 14px;
            animation: bounce 2s infinite;
        }

            .hero .scroll-hint::after {
                content: '↓';
                display: block;
                font-size: 30px;
                margin-top: 10px;
            }

        /* 动画 */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateX(-50%) translateY(0);
            }

            40% {
                transform: translateX(-50%) translateY(-20px);
            }

            60% {
                transform: translateX(-50%) translateY(-10px);
            }
        }

        /* 通用区块样式 */
        section {
            padding: 100px 50px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

            .section-title h2 {
                font-size: 42px;
                color: var(--dark-red);
                margin-bottom: 15px;
                position: relative;
                display: inline-block;
            }

                .section-title h2::after {
                    content: '';
                    position: absolute;
                    bottom: -10px;
                    left: 50%;
                    transform: translateX(-50%);
                    width: 80px;
                    height: 4px;
                    background: linear-gradient(90deg, var(--gold), var(--primary-red), var(--gold));
                }

            .section-title p {
                font-size: 18px;
                color: var(--text-gray);
                margin-top: 25px;
            }

        /* 历史背景 */
        .history {
            background: white;
        }

        .history-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .history-text h3 {
            font-size: 28px;
            color: var(--primary-red);
            margin-bottom: 25px;
        }

        .history-text p {
            font-size: 17px;
            color: var(--text-gray);
            margin-bottom: 20px;
            text-indent: 2em;
        }

        .history-image {
            background: linear-gradient(135deg, var(--primary-red), var(--dark-red));
            border-radius: 10px;
            padding: 40px;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 10px 40px rgba(196,30,58,0.3);
        }

            .history-image .star-emblem {
                font-size: 150px;
                color: var(--gold);
                text-shadow: 0 0 30px rgba(212,175,55,0.5);
            }

        /* 时间轴 */
        .timeline-section {
            background: linear-gradient(180deg, var(--bg-cream), #EDE6D8);
        }

        .timeline {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }

            .timeline::before {
                content: '';
                position: absolute;
                left: 50%;
                transform: translateX(-50%);
                width: 4px;
                height: 100%;
                background: linear-gradient(180deg, var(--gold), var(--primary-red), var(--dark-red));
            }

        .timeline-item {
            display: flex;
            justify-content: flex-end;
            padding: 20px 0;
            position: relative;
            width: 50%;
        }

            .timeline-item:nth-child(odd) {
                align-self: flex-start;
                padding-right: 50px;
            }

            .timeline-item:nth-child(even) {
                align-self: flex-end;
                justify-content: flex-start;
                padding-left: 50px;
                margin-left: 50%;
            }

            .timeline-item::before {
                content: '';
                position: absolute;
                top: 30px;
                width: 20px;
                height: 20px;
                background: var(--gold);
                border: 4px solid var(--dark-red);
                border-radius: 50%;
                z-index: 1;
            }

            .timeline-item:nth-child(odd)::before {
                right: -10px;
            }

            .timeline-item:nth-child(even)::before {
                left: -10px;
            }

        .timeline-content {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            max-width: 400px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

            .timeline-content:hover {
                transform: translateY(-5px);
                box-shadow: 0 10px 30px rgba(196,30,58,0.2);
            }

            .timeline-content .year {
                font-size: 24px;
                font-weight: bold;
                color: var(--primary-red);
                margin-bottom: 10px;
            }

            .timeline-content h4 {
                font-size: 20px;
                color: var(--dark-red);
                margin-bottom: 10px;
            }

            .timeline-content p {
                font-size: 15px;
                color: var(--text-gray);
            }

        /* 重要战役 */
        .battles {
            background: white;
        }

        .battles-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .battle-card {
            background: linear-gradient(135deg, #FFF8F0, #FFF0E6);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            border: 2px solid transparent;
        }

            .battle-card:hover {
                transform: translateY(-10px);
                box-shadow: 0 15px 40px rgba(196,30,58,0.2);
                border-color: var(--gold);
            }

            .battle-card .card-header {
                background: linear-gradient(135deg, var(--primary-red), var(--dark-red));
                padding: 20px;
                text-align: center;
            }

                .battle-card .card-header h4 {
                    color: var(--gold);
                    font-size: 22px;
                }

            .battle-card .card-body {
                padding: 25px;
            }

                .battle-card .card-body p {
                    color: var(--text-gray);
                    font-size: 15px;
                    margin-bottom: 15px;
                }

            .battle-card .card-stats {
                display: flex;
                justify-content: space-around;
                padding-top: 15px;
                border-top: 1px solid rgba(196,30,58,0.2);
            }

                .battle-card .card-stats .stat {
                    text-align: center;
                }

                .battle-card .card-stats .stat-value {
                    font-size: 20px;
                    font-weight: bold;
                    color: var(--primary-red);
                }

                .battle-card .card-stats .stat-label {
                    font-size: 13px;
                    color: var(--text-gray);
                }

        /* 长征精神 */
        .spirit {
            background: linear-gradient(135deg, var(--dark-red), var(--primary-red));
            color: white;
        }

            .spirit .section-title h2 {
                color: var(--gold);
            }

            .spirit .section-title p {
                color: rgba(255,255,255,0.8);
            }

        .spirit-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 25px;
        }

        .spirit-item {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px 20px;
            text-align: center;
            transition: transform 0.3s, background 0.3s;
            border: 2px solid rgba(212,175,55,0.3);
        }

            .spirit-item:hover {
                transform: translateY(-10px);
                background: rgba(255,255,255,0.2);
                border-color: var(--gold);
            }

            .spirit-item .icon {
                font-size: 50px;
                margin-bottom: 15px;
            }

            .spirit-item h4 {
                font-size: 18px;
                color: var(--gold);
                margin-bottom: 12px;
            }

            .spirit-item p {
                font-size: 14px;
                color: rgba(255,255,255,0.9);
                line-height: 1.6;
            }

        /* 数据统计 */
        .stats-section {
            background: var(--bg-cream);
        }

        .stats-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
        }

        .stat-card {
            background: white;
            border-radius: 15px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            transition: transform 0.3s;
            position: relative;
            overflow: hidden;
        }

            .stat-card::before {
                content: '';
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                height: 5px;
                background: linear-gradient(90deg, var(--gold), var(--primary-red));
            }

            .stat-card:hover {
                transform: translateY(-10px);
            }

            .stat-card .stat-number {
                font-size: 48px;
                font-weight: bold;
                color: var(--primary-red);
                margin-bottom: 10px;
            }

            .stat-card .stat-unit {
                font-size: 20px;
                color: var(--dark-red);
                margin-bottom: 15px;
            }

            .stat-card .stat-label {
                font-size: 16px;
                color: var(--text-gray);
            }

        /* 互动区 */
        .interactive {
            background: white;
        }

        .quiz-container {
            max-width: 800px;
            margin: 0 auto;
            background: linear-gradient(135deg, #FFF8F0, #FFF0E6);
            border-radius: 20px;
            padding: 50px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
        }

        .quiz-question {
            font-size: 22px;
            color: var(--dark-red);
            margin-bottom: 30px;
            text-align: center;
        }

        .quiz-options {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 30px;
        }

        .quiz-option {
            padding: 20px 30px;
            background: white;
            border: 2px solid var(--primary-red);
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 16px;
            color: var(--text-dark);
        }

            .quiz-option:hover {
                background: var(--primary-red);
                color: white;
            }

            .quiz-option.correct {
                background: #28a745;
                border-color: #28a745;
                color: white;
            }

            .quiz-option.wrong {
                background: #dc3545;
                border-color: #dc3545;
                color: white;
            }

        .quiz-result {
            text-align: center;
            font-size: 24px;
            color: var(--primary-red);
            margin-top: 20px;
        }

        .quiz-next {
            display: block;
            margin: 30px auto 0;
            padding: 15px 50px;
            background: linear-gradient(135deg, var(--primary-red), var(--dark-red));
            color: white;
            border: none;
            border-radius: 30px;
            font-size: 18px;
            cursor: pointer;
            transition: transform 0.3s;
        }

            .quiz-next:hover {
                transform: scale(1.05);
            }

        /* 留言区 */
        .message-board {
            max-width: 800px;
            margin: 60px auto 0;
        }

            .message-board h3 {
                text-align: center;
                font-size: 28px;
                color: var(--dark-red);
                margin-bottom: 30px;
            }

        .message-form {
            display: grid;
            gap: 20px;
        }

            .message-form input,
            .message-form textarea {
                padding: 15px 20px;
                border: 2px solid rgba(196,30,58,0.3);
                border-radius: 10px;
                font-size: 16px;
                font-family: inherit;
                transition: border-color 0.3s;
            }

                .message-form input:focus,
                .message-form textarea:focus {
                    outline: none;
                    border-color: var(--primary-red);
                }

            .message-form textarea {
                min-height: 120px;
                resize: vertical;
            }

            .message-form button {
                padding: 15px 50px;
                background: linear-gradient(135deg, var(--primary-red), var(--dark-red));
                color: white;
                border: none;
                border-radius: 30px;
                font-size: 18px;
                cursor: pointer;
                transition: transform 0.3s;
            }

                .message-form button:hover {
                    transform: scale(1.05);
                }

        /* 页脚 */
        footer {
            background: linear-gradient(135deg, var(--dark-red), #5a0000);
            color: white;
            padding: 60px 50px 30px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 50px;
            margin-bottom: 40px;
        }

        .footer-section h4 {
            color: var(--gold);
            font-size: 20px;
            margin-bottom: 20px;
        }

        .footer-section p,
        .footer-section a {
            color: rgba(255,255,255,0.8);
            font-size: 15px;
            line-height: 2;
            text-decoration: none;
        }

            .footer-section a:hover {
                color: var(--gold);
            }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.2);
        }

            .footer-bottom p {
                color: rgba(255,255,255,0.6);
                font-size: 14px;
            }

        /* 响应式 */
        @media (max-width: 768px) {
            .navbar {
                padding: 15px 20px;
            }

                .navbar ul {
                    display: none;
                }

            .hero h1 {
                font-size: 36px;
            }

            .hero .subtitle {
                font-size: 18px;
            }

            .hero .years {
                font-size: 28px;
            }

            section {
                padding: 60px 20px;
            }

            .section-title h2 {
                font-size: 28px;
            }

            .history-content {
                grid-template-columns: 1fr;
            }

            .timeline::before {
                left: 20px;
            }

            .timeline-item {
                width: 100%;
                padding-left: 50px !important;
                padding-right: 0 !important;
                margin-left: 0 !important;
            }

                .timeline-item::before {
                    left: 10px !important;
                    right: auto !important;
                }

            .spirit-grid {
                grid-template-columns: 1fr;
            }

            .stats-container {
                grid-template-columns: 1fr 1fr;
            }

            .quiz-options {
                grid-template-columns: 1fr;
            }

            .footer-content {
                grid-template-columns: 1fr;
            }
        }

        /* 滚动动画 */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s, transform 0.6s;
        }

            .fade-in.visible {
                opacity: 1;
                transform: translateY(0);
            }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav class="navbar">
        <div class="logo">
            <span class="logo-star">★</span>
            <span>纪念长征胜利 90 周年</span>
        </div>
        <ul>
            <li><a href="#history">历史背景</a></li>
            <li><a href="#timeline">光辉历程</a></li>
            <li><a href="#battles">重要战役</a></li>
            <li><a href="#spirit">长征精神</a></li>
            <li><a href="#stats">数据统计</a></li>
            <li><a href="#interactive">互动学习</a></li>
        </ul>
    </nav>

    <!-- 英雄区 -->
    <section class="hero">
        <div class="hero-content">
            <h1>纪念长征胜利 90 周年</h1>
            <p class="subtitle">弘扬长征精神 · 走好新时代长征路</p>
            <p class="years">1936 - 2026</p>
        </div>
        <div class="scroll-hint">向下浏览</div>
    </section>

    <!-- 历史背景 -->
    <section id="history" class="history">
        <div class="section-title fade-in">
            <h2>历史背景</h2>
            <p>人类历史上的伟大壮举</p>
        </div>
        <div class="history-content">
            <div class="history-text fade-in">
                <h3>什么是长征？</h3>
                <p>长征是 1934 年 10 月至 1936 年 10 月期间，中国共产党领导的中国工农红军进行的战略转移。由于第五次反"围剿"失败，中央红军被迫实行战略性转移，从中央苏区出发，历经艰难险阻，最终到达陕北。</p>
                <p>长征途经江西、福建、广东、湖南、广西、贵州、云南、四川、西康、甘肃、陕西等 11 个省，行程约二万五千里，跨越近百条江河，翻越 40 余座高山险峰，其中海拔 4000 米以上的雪山就有 20 余座。</p>
                <p>1936 年 10 月，红一、二、四方面军在甘肃会宁胜利会师，标志着长征的胜利结束。长征的胜利，保存了党和红军的基干力量，使中国革命转危为安，为抗日战争和中国革命的胜利奠定了基础。</p>
            </div>
            <div class="history-image fade-in">
                <div class="star-emblem">★</div>
            </div>
        </div>
    </section>

    <!-- 时间轴 -->
    <section id="timeline" class="timeline-section">
        <div class="section-title fade-in">
            <h2>光辉历程</h2>
            <p>1934-1936 年关键历史节点</p>
        </div>
        <div class="timeline">
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1934 年 10 月</div>
                    <h4>长征开始</h4>
                    <p>中央红军从江西瑞金、于都和福建长汀、宁化等地出发，开始战略性转移。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1934 年 11 月</div>
                    <h4>湘江战役</h4>
                    <p>红军突破国民党军第四道封锁线，付出惨重代价，从 8.6 万人锐减至 3 万余人。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1935 年 1 月</div>
                    <h4>遵义会议</h4>
                    <p>确立毛泽东同志在党和红军中的领导地位，成为党的历史上生死攸关的转折点。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1935 年 1-3 月</div>
                    <h4>四渡赤水</h4>
                    <p>毛泽东指挥红军灵活机动地穿插于敌人重兵之间，创造战争奇迹。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1935 年 5 月</div>
                    <h4>飞夺泸定桥</h4>
                    <p>22 名勇士冒着枪林弹雨攀踏铁索，夺取泸定桥，打开北上通道。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1935 年 6 月</div>
                    <h4>翻越夹金山</h4>
                    <p>红军翻越第一座大雪山，克服高寒缺氧等极端困难。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1935 年 8 月</div>
                    <h4>过草地</h4>
                    <p>红军穿越松潘草地，经历饥饿、寒冷、沼泽等严峻考验。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1935 年 10 月</div>
                    <h4>到达吴起镇</h4>
                    <p>中央红军到达陕北吴起镇，与陕北红军胜利会师。</p>
                </div>
            </div>
            <div class="timeline-item fade-in">
                <div class="timeline-content">
                    <div class="year">1936 年 10 月</div>
                    <h4>会宁会师</h4>
                    <p>红一、二、四方面军在甘肃会宁胜利会师，长征胜利结束。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 重要战役 -->
    <section id="battles" class="battles">
        <div class="section-title fade-in">
            <h2>重要战役</h2>
            <p>决定长征走向的关键战斗</p>
        </div>
        <div class="battles-grid">
            <div class="battle-card fade-in">
                <div class="card-header">
                    <h4>湘江战役</h4>
                </div>
                <div class="card-body">
                    <p>1934 年 11 月，红军在广西湘江地区与国民党军展开激战，突破第四道封锁线。此役是长征中最惨烈的一战。</p>
                    <div class="card-stats">
                        <div class="stat">
                            <div class="stat-value">7 昼夜</div>
                            <div class="stat-label">战斗时长</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">5 万+</div>
                            <div class="stat-label">伤亡人数</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="battle-card fade-in">
                <div class="card-header">
                    <h4>遵义战役</h4>
                </div>
                <div class="card-body">
                    <p>1935 年 2 月，红军在遵义地区歼灭和击溃国民党军 2 个师又 8 个团，取得长征以来最大胜利。</p>
                    <div class="card-stats">
                        <div class="stat">
                            <div class="stat-value">5 天</div>
                            <div class="stat-label">战斗时长</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">3000+</div>
                            <div class="stat-label">歼敌人数</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="battle-card fade-in">
                <div class="card-header">
                    <h4>四渡赤水</h4>
                </div>
                <div class="card-body">
                    <p>1935 年 1 月至 3 月，毛泽东指挥红军在赤水河两岸灵活机动，穿插于敌人重兵之间，创造战争奇迹。</p>
                    <div class="card-stats">
                        <div class="stat">
                            <div class="stat-value">3 个月</div>
                            <div class="stat-label">战役时长</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">4 次</div>
                            <div class="stat-label">渡河次数</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="battle-card fade-in">
                <div class="card-header">
                    <h4>飞夺泸定桥</h4>
                </div>
                <div class="card-body">
                    <p>1935 年 5 月 29 日，红四团 22 名勇士冒着枪林弹雨攀踏 13 根铁索，夺取泸定桥，为红军打开北上通道。</p>
                    <div class="card-stats">
                        <div class="stat">
                            <div class="stat-value">22 人</div>
                            <div class="stat-label">突击队员</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">100 米</div>
                            <div class="stat-label">桥面长度</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="battle-card fade-in">
                <div class="card-header">
                    <h4>腊子口战役</h4>
                </div>
                <div class="card-body">
                    <p>1935 年 9 月，红军突破天险腊子口，打开进入甘肃的通道，为长征胜利奠定基础。</p>
                    <div class="card-stats">
                        <div class="stat">
                            <div class="stat-value">2 天</div>
                            <div class="stat-label">战斗时长</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">天险</div>
                            <div class="stat-label">地形特点</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="battle-card fade-in">
                <div class="card-header">
                    <h4>山城堡战役</h4>
                </div>
                <div class="card-body">
                    <p>1936 年 11 月，红军三大主力会师后取得的首次重大胜利，标志着长征的完全胜利。</p>
                    <div class="card-stats">
                        <div class="stat">
                            <div class="stat-value">1 天</div>
                            <div class="stat-label">战斗时长</div>
                        </div>
                        <div class="stat">
                            <div class="stat-value">1 个旅</div>
                            <div class="stat-label">歼敌规模</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 长征精神 -->
    <section id="spirit" class="spirit">
        <div class="section-title fade-in">
            <h2>长征精神</h2>
            <p>中国共产党人的精神丰碑</p>
        </div>
        <div class="spirit-grid">
            <div class="spirit-item fade-in">
                <!--<div class="icon">🎯</div>-->
                <h4>坚定信念</h4>
                <p>把全国人民和中华民族的根本利益看得高于一切，坚定革命的理想和信念</p>
            </div>
            <div class="spirit-item fade-in">
                <!--<div class="icon">💪</div>-->
                <h4>不怕牺牲</h4>
                <p>为了救国救民，不怕任何艰难险阻，不惜付出一切牺牲的精神</p>
            </div>
            <div class="spirit-item fade-in">
                <!--<div class="icon">🔍</div>-->
                <h4>实事求是</h4>
                <p>坚持独立自主、实事求是，一切从实际出发的精神</p>
            </div>
            <div class="spirit-item fade-in">
                <!--<div class="icon">🤝</div>-->
                <h4>顾全大局</h4>
                <p>顾全大局、严守纪律、紧密团结的精神</p>
            </div>
            <div class="spirit-item fade-in">
                <!--<div class="icon">❤️</div>-->
                <h4>依靠人民</h4>
                <p>紧紧依靠人民群众，同人民群众生死相依、患难与共、艰苦奋斗的精神</p>
            </div>
        </div>
    </section>

    <!-- 数据统计 -->
    <section id="stats" class="stats-section">
        <div class="section-title fade-in">
            <h2>长征数据</h2>
            <p>用数字铭记伟大壮举</p>
        </div>
        <div class="stats-container">
            <div class="stat-card fade-in">
                <div class="stat-number">25000</div>
                <div class="stat-unit">里</div>
                <div class="stat-label">总行程</div>
            </div>
            <div class="stat-card fade-in">
                <div class="stat-number">721</div>
                <div class="stat-unit">天</div>
                <div class="stat-label">历时时长</div>
            </div>
            <div class="stat-card fade-in">
                <div class="stat-number">11</div>
                <div class="stat-unit">省</div>
                <div class="stat-label">途经省份</div>
            </div>
            <div class="stat-card fade-in">
                <div class="stat-number">40+</div>
                <div class="stat-unit">座</div>
                <div class="stat-label">翻越高山</div>
            </div>
        </div>
    </section>

    <!-- 互动区 -->
    <section id="interactive" class="interactive">
        <div class="section-title fade-in">
            <h2>互动学习</h2>
            <p>测试你的长征知识</p>
        </div>
        <div class="quiz-container fade-in">
            <div id="quiz">
                <div class="quiz-question" id="question"></div>
                <div class="quiz-options" id="options"></div>
                <div class="quiz-result" id="result"></div>
                <button class="quiz-next" id="nextBtn" style="display:none;">下一题</button>
            </div>
        </div>
        <div class="message-board fade-in">
            <h3>留言寄语</h3>
            <form class="message-form" id="messageForm">
                <input type="text" placeholder="您的姓名" required>
                <textarea placeholder="写下您对长征精神的感悟或对未来的寄语..." required></textarea>
                <button type="submit">提交留言</button>
            </form>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h4>关于</h4>
                <p>本站为纪念长征胜利 90 周年而建，旨在弘扬长征精神，传承红色基因，激励新时代青年走好属于自己的长征路。</p>
            </div>
            
            <div class="footer-section">
                <h4>联系我</h4>
                <p>如有建议或意见，欢迎联系我</p>
                <p>
                    学号：20251034363
                </p>
            </div>
        </div>
        <div class="footer-bottom">
            <p>2026 纪念长征胜利 90 周年 | 弘扬长征精神 · 走好新时代长征路</p>
        </div>
    </footer>

    <script>
        // 滚动动画
        function checkFadeIn() {
        const elements = document.querySelectorAll('.fade-in');
        elements.forEach(el => {
        const rect = el.getBoundingClientRect();
        if (rect.top < window.innerHeight - 100) {
        el.classList.add('visible');
        }
        });
        }

        window.addEventListener('scroll', checkFadeIn);
        window.addEventListener('load', checkFadeIn);

        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
        });
        });

        // 问答系统
        const quizData = [
        {
        question: "长征开始于哪一年？",
        options: ["1933 年", "1934 年", "1935 年", "1936 年"],
        answer: 1
        },
        {
        question: "长征的总行程约为多少里？",
        options: ["一万五千里", "二万里", "二万五千里", "三万里"],
        answer: 2
        },
        {
        question: "遵义会议确立了谁在党和红军中的领导地位？",
        options: ["周恩来", "朱德", "毛泽东", "张闻天"],
        answer: 2
        },
        {
        question: "飞夺泸定桥发生在哪一年？",
        options: ["1934 年", "1935 年", "1936 年", "1937 年"],
        answer: 1
        },
        {
        question: "红军三大主力会师的地点是？",
        options: ["吴起镇", "延安", "会宁", "保安"],
        answer: 2
        },
        {
        question: "长征途经了多少个省份？",
        options: ["9 个", "10 个", "11 个", "12 个"],
        answer: 2
        }
        ];

        let currentQuestion = 0;
        let score = 0;

        function loadQuestion() {
        const q = quizData[currentQuestion];
        document.getElementById('question').textContent = `问题 ${currentQuestion + 1}/${quizData.length}：${q.question}`;

        const optionsDiv = document.getElementById('options');
        optionsDiv.innerHTML = '';

        q.options.forEach((opt, index) => {
        const btn = document.createElement('div');
        btn.className = 'quiz-option';
        btn.textContent = opt;
        btn.onclick = () => checkAnswer(index, btn);
        optionsDiv.appendChild(btn);
        });

        document.getElementById('result').textContent = '';
        document.getElementById('nextBtn').style.display = 'none';
        }

        function checkAnswer(selectedIndex, btnElement) {
        const options = document.querySelectorAll('.quiz-option');
        options.forEach(opt => opt.style.pointerEvents = 'none');

        const correct = quizData[currentQuestion].answer;

        if (selectedIndex === correct) {
        btnElement.classList.add('correct');
        document.getElementById('result').textContent = '✓ 回答正确！';
        score++;
        } else {
        btnElement.classList.add('wrong');
        options[correct].classList.add('correct');
        document.getElementById('result').textContent = '✗ 回答错误';
        }

        if (currentQuestion < quizData.length - 1) {
        document.getElementById('nextBtn').style.display = 'block';
        } else {
        document.getElementById('result').textContent += ` | 最终得分：${score}/${quizData.length}`;
        document.getElementById('nextBtn').textContent = '重新测试';
        document.getElementById('nextBtn').style.display = 'block';
        document.getElementById('nextBtn').onclick = resetQuiz;
        }
        }

        document.getElementById('nextBtn').onclick = () => {
        currentQuestion++;
        loadQuestion();
        };

        function resetQuiz() {
        currentQuestion = 0;
        score = 0;
        document.getElementById('nextBtn').textContent = '下一题';
        document.getElementById('nextBtn').onclick = () => {
        currentQuestion++;
        loadQuestion();
        };
        loadQuestion();
        }

        // 初始化问答
        loadQuestion();

        // 留言表单
        document.getElementById('messageForm').addEventListener('submit', function(e) {
        e.preventDefault();
        alert('感谢您的留言！您的寄语已提交。');
        this.reset();
        });

        // 数字动画
        function animateNumbers() {
        const statNumbers = document.querySelectorAll('.stat-number');
        statNumbers.forEach(el => {
        const rect = el.getBoundingClientRect();
        if (rect.top < window.innerHeight - 100 && !el.classList.contains('animated')) {
        el.classList.add('animated');
        const target = parseInt(el.textContent);
        if (target) {
        let current = 0;
        const increment = target / 50;
        const timer = setInterval(() => {
        current += increment;
        if (current >= target) {
        el.textContent = el.textContent.replace(/\d+/, target);
        clearInterval(timer);
        } else {
        el.textContent = el.textContent.replace(/\d+/, Math.floor(current));
        }
        }, 30);
        }
        }
        });
        }

        window.addEventListener('scroll', animateNumbers);
    </script>
</body>
</html>
