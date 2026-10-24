

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portafolio - JT </title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&family=Bodoni+Moda:ital,opsz,wght@0,6..96,400;0,6..96,700;0,6..96,900;1,6..96,400&family=Dancing+Script:wght@400;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-color: #fff5f9;
            --text-color: #2d2d2d;
            --accent-color: #f283af; /* Rosa Principal */
            --accent-dark: #C43670;
            --secondary-bg: #e0608e;
            --card-shadow: 0 10px 30px rgba(242, 131, 175, 0.25);
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* --- Header / Navigation --- */
        header {
            padding: 1.05rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            background: rgba(252, 249, 249, 0.85);
            backdrop-filter: blur(15px);
            z-index: 1000;
            transition: var(--transition);
        }

        .logo {
            font-family: 'Bodoni Moda', serif;
            font-size: 1.6rem;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--text-color);
            text-decoration: none;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        nav a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: var(--transition);
        }

        nav a:hover {
            color: var(--accent-dark);
        }

        /* --- Hero Section --- */
        .hero {
            min-height: 60vh;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            padding: 0 5% 0 10%;
            background: radial-gradient(circle at 30% center, #ffffff 0%, var(--bg-color) 100%);
            overflow: hidden;
            gap: 2rem;
        }

        .hero-text {
            flex: 0 0 48%;
            max-width: 520px;
            text-align: left;
        }

        .hero-image {
            flex: 0 0 52%;
            align-self: stretch;
            overflow: hidden;
        }

        .hero-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center 28%;
            display: block;
        }

        .hero h1 {
            font-family: 'Bodoni Moda', serif;
            font-size: 4.5rem;
            margin-bottom: 1.2rem;
            line-height: 1.1;
            font-weight: 700;
        }

        .hero p {
            font-size: 1.1rem;
            max-width: 520px;
            margin-bottom: 2.5rem;
            color: #666;
            font-weight: 300;
        }
        /* --- Social Icons --- */
        .social-links {
            display: flex;
            gap: 0.6rem;
            align-items: center;
        }

        .social-icon {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 38px;
            height: 38px;
            border-radius: 50%;
            background: var(--accent-dark);
            color: #fff;
            transition: var(--transition);
            text-decoration: none;
        }

        .social-icon:hover {
            background: var(--accent-color);
            transform: translateY(-3px);
        }

        .social-icon svg {
            width: 18px;
            height: 18px;
            fill: #fff;
        }

        .btn-contact {
            padding: 1.2rem 3rem;
            background: var(--accent-dark);
            color: #ffffff;
            text-decoration: none;
            border-radius: 100px;
            font-weight: 600;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: var(--transition);
            border: 2px solid var(--accent-dark);
            box-shadow: 0 4px 15px rgba(196, 54, 112, 0.35);
        }

        .btn-contact:hover {
            background: var(--accent-color);
            border-color: var(--accent-color);
            color: #ffffff;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(242, 131, 175, 0.5);
        }
        
        /* --- Section Titles --- */
        .section-title {
            font-family: 'Dancing Script', cursive;
            font-size: 2.8rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 3rem;
            color: var(--text-color);
        }

/* --- Estilo Seccion Marcas (Estilo Imagen Adjunta) --- */
        .brands-section {
            padding: 4rem 10%; text-align: center; background: #fff;
        }
        .brands-section .section-title,
        #videos .section-title {
            margin-bottom: 0.5rem;
        }
        .brands-section .brand-hint {
            margin-bottom: 3rem;
            font-size: 0.85rem;
            color: var(--accent-dark);
            text-align: center;
        }
        #videos .brand-hint {
            margin-bottom: 1.5rem;
            font-size: 0.85rem;
            color: var(--accent-dark);
            text-align: center;
        }
        .brands-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 2rem; justify-items: center; align-items: center; max-width: 1000px; margin: 0 auto;
        }
        .brand-circle {
            width: 110px; height: 110px; border-radius: 50%;
            overflow: hidden; background: #fff;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            display: flex; align-items: center; justify-content: center;
            position: relative;
            transition: var(--transition); border: 2px solid transparent;
        }
                .brand-item { display: flex; flex-direction: column; align-items: center; gap: 0.5rem; }
        .brand-name { font-size: 0.6rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px; color: var(--text-color); text-align: center; max-width: 110px; }
        .brand-circle:hover { transform: scale(1.1); border-color: var(--accent-color); }
        .brand-circle img { width: 80%; height: 80%; object-fit: contain; }

        /* --- Stats Section --- */
        .stats-section { padding: 5rem 10%; background: #C43670; border-y: 1px solid #fff0f7; }
        .stats-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 2rem; max-width: 900px; margin: 0 auto; }
        .stat-item { text-align: center; }
        .stat-number { display: block; font-size: 3rem; font-weight: 800; color: var(--text-color); }
        .stat-label { font-size: 0.7rem; font-weight: 600; text-transform: uppercase; color: #999; }

        /* --- Dashboard Section --- */
        .dashboard-section { padding: 6rem 10%; background: #fff; }
        .dashboard-container {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px; max-width: 1100px; margin: 0 auto;
        }
        .dash-card {
            background: var(--bg-color); padding: 2rem; border-radius: 20px;
            text-align: center; border: 1px solid #eee;
        }
        .dash-card h4 { font-family: 'Dancing Script', cursive; font-size: 1.1rem; text-transform: none; color: #888; margin-bottom: 1rem; }
        .dash-value { font-size: 2.5rem; font-weight: 800; color: var(--accent-dark); display: block; }

        /* --- Video Carousel --- */
        .carousel-wrapper {
            position: relative;
            padding: 1rem 0 2rem;
        }

        .carousel-outer {
            overflow: hidden;
            padding: 1.5rem 0;
        }

        .carousel-track {
            display: flex;
            gap: 24px;
            width: max-content;
            will-change: transform;
            align-items: flex-start;
        }

        .card-item {
            flex-shrink: 0;
            width: 252px;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
        }

        .phone-card {
            width: 252px;
            aspect-ratio: 9/16;
            border-radius: 30px;
            overflow: hidden;
            background: #fff5f9;
            border: 4px solid rgba(255, 255, 255, 0.95);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.13);
            position: relative;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .phone-card:hover {
            transform: translateY(-8px) scale(1.04);
            box-shadow: 0 22px 55px rgba(0, 0, 0, 0.2);
        }

        .phone-card.instagram-post {
            background: linear-gradient(#ffffff, #ffffff) padding-box,
                        linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888) border-box;
            border: 4px solid transparent;
            box-shadow: 0 14px 45px rgba(225, 48, 108, 0.25);
        }

        .phone-card-coming {
            position: absolute;
            inset: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            color: rgba(255, 255, 255, 0.85);
            font-size: 0.6rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            font-weight: 600;
        }

        .phone-card-coming svg {
            width: 28px;
            height: 28px;
            fill: rgba(255, 255, 255, 0.75);
        }

        .phone-card-frame {
            position: absolute;
            inset: 0;
            display: none;
            overflow: hidden;
        }

        .phone-card-frame iframe {
            width: 320px;
            height: 569px;
            border: none;
            display: block;
            transform: scale(0.7875);
            transform-origin: top left;
        }

        .card-meta {
            text-align: center;
            width: 100%;
        }

        .card-num {
            display: block;
            font-size: 0.65rem;
            color: #bbb;
            letter-spacing: 2px;
            margin-bottom: 0.15rem;
        }

        .card-meta h3 {
            font-family: 'Bodoni Moda', serif;
            font-size: 1rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--text-color);
            margin-bottom: 0.35rem;
        }

        .card-tag {
            display: inline-block;
            padding: 0.15rem 0.75rem;
            border: 1px solid #ddd;
            border-radius: 100px;
            font-size: 0.6rem;
            letter-spacing: 1px;
            text-transform: uppercase;
            color: #888;
            margin-bottom: 0.35rem;
        }

        .card-link {
            display: block;
            font-size: 0.65rem;
            color: var(--accent-dark);
            text-decoration: none;
            letter-spacing: 1px;
            text-transform: uppercase;
            font-weight: 600;
        }

        .card-link:hover { text-decoration: underline; }

        .carousel-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            z-index: 10;
            background: var(--accent-dark);
            color: #fff;
            border: none;
            width: 42px;
            height: 42px;
            border-radius: 50%;
            font-size: 1.4rem;
            line-height: 1;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 14px rgba(196, 54, 112, 0.4);
            transition: var(--transition);
        }

        .carousel-btn:hover {
            background: var(--accent-color);
            transform: translateY(-50%) scale(1.1);
        }

        .carousel-btn.prev { left: 0; }
        .carousel-btn.next { right: 0; }

        /* --- Pricing Table --- */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            align-items: center;
        }

        .pricing-card {
            background: white;
            padding: 3.6rem 1.8rem;
            border-radius: 27px;
            text-align: center;
            border: 1px solid #f0efef;
            transition: var(--transition);
            position: relative;
        }

        .pricing-card:hover {
            box-shadow: 0 20px 40px rgba(0,0,0,0.05);
        }

        .pricing-card.featured {
            background: linear-gradient(145deg, #ffffff, #fffafa);
            border: 2px solid var(--accent-dark);
            transform: scale(1.05);
            z-index: 2;
        }

        .pricing-card.featured::before {
            content: "RECOMENDADO";
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--accent-dark);
            padding: 5px 20px;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: 800;
            letter-spacing: 1px;
        }

        .pricing-card h3 {
            font-family: 'Dancing Script', cursive;
            font-size: 1.8rem;
            margin-bottom: 1.35rem;
        }

        .price {
            font-size: 3.15rem;
            font-weight: 800;
            margin-bottom: 1.8rem;
            color: var(--text-color);
        }

        .price span {
            font-size: 1.08rem;
            font-weight: 300;
            opacity: 0.5;
        }

        .features-list {
            list-style: none;
            margin-bottom: 2.7rem;
            text-align: left;
            display: inline-block;
        }

        .features-list li {
            margin-bottom: 0.9rem;
            font-size: 0.85rem;
            color: #555;
            display: flex;
            align-items: center;
        }

        .features-list li::before {
            content: "✓";
            margin-right: 12px;
            color: var(--accent-dark);
            font-weight: bold;
        }

        /* --- Footer --- */
        footer {
            padding: 2.5rem 10%;
            background: #f5c0d8;
            border-top: 1px solid #eee;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
        }

        .footer-logo {
            font-family: 'Bodoni Moda', serif;
            font-size: 1.2rem;
            display: block;
        }

        .copyright {
            font-size: 0.75rem;
            color: var(--accent-dark);
            letter-spacing: 1px;
        }

        .footer-social {
            display: flex;
            gap: 0.5rem;
            margin-top: 0.4rem;
        }

        /* --- Marquee Ticker --- */
        .marquee-wrapper {
            overflow: hidden;
            white-space: nowrap;
            background: var(--text-color);
            padding: 0.5rem 0;
            position: relative;
        }

        .marquee-track {
            display: inline-flex;
            align-items: center;
            gap: 0;
            animation: marquee-scroll 28s linear infinite;
            will-change: transform;
        }

        .marquee-wrapper:hover .marquee-track {
            animation-play-state: paused;
        }

        .marquee-item {
            font-size: 0.50rem;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: #fff;
            padding: 0 1.8rem;
            flex-shrink: 0;
        }

        .marquee-sep {
            color: var(--accent-color);
            font-size: 0.9rem;
            font-weight: 700;
            flex-shrink: 0;
        }

        @keyframes marquee-scroll {
            from { transform: translateX(0); }
            to   { transform: translateX(-50%); }
        }

        /* --- Stats Section --- */
        .stats-section {
            padding: 2.92rem 10%;
            background: #C43670;
            border-top: 1px solid #fff0f7;
            border-bottom: 1px solid #C43670;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 3rem;
            max-width: 1100px;
            margin: 0 auto;
        }

        .stat-item {
            text-align: center;
            position: relative;
        }

        .stat-item:not(:last-child)::after {
            content: "";
            position: absolute;
            right: 0;
            top: 20%;
            height: 60%;
            width: 1px;
            background: var(--bg-color);
            opacity: 0.4;
        }

        .stat-number {
            display: block;
            font-size: 3rem;
            font-weight: 800;
            color: var(--bg-color);
            line-height: 1;
            margin-bottom: 0.6rem;
            font-family: 'Inter', sans-serif;
        }

        .stat-label {
            display: block;
            font-size: 0.7rem;
            font-weight: 600;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: #fff0f7;
        }

        /* --- Hamburger Button --- */
        .hamburger {
            display: none;
            flex-direction: column;
            justify-content: center;
            gap: 5px;
            background: none;
            border: none;
            cursor: pointer;
            padding: 6px;
            z-index: 1002;
        }
        .hamburger span {
            display: block;
            width: 24px;
            height: 2px;
            background: var(--text-color);
            border-radius: 2px;
            transition: var(--transition);
        }
        .nav-close {
            display: none;
            position: absolute;
            top: 1.2rem;
            right: 5%;
            background: none;
            border: none;
            font-size: 1.8rem;
            cursor: pointer;
            color: var(--text-color);
            line-height: 1;
        }

        /* --- Responsividad Móvil --- */
        @media (max-width: 768px) {
            /* Header */
            header { padding: 1rem 5%; }
            .hamburger { display: flex; }
            .nav-close { display: block; }
            nav {
                display: none;
                position: fixed;
                inset: 0;
                background: rgba(255, 245, 249, 0.97);
                backdrop-filter: blur(20px);
                z-index: 1001;
                flex-direction: column;
                align-items: center;
                justify-content: center;
            }
            nav.open { display: flex; }
            nav ul { flex-direction: column; gap: 2.5rem; text-align: center; }
            nav a { font-size: 1.3rem; letter-spacing: 2px; }

            /* Hero */
            .hero {
                flex-direction: column;
                min-height: auto;
                padding: 0 0 2.5rem;
                text-align: center;
                gap: 0;
            }
            .hero-text {
                flex: none;
                width: 100%;
                max-width: 100%;
                order: 2;
                padding: 2rem 5% 0;
            }
            .hero-image {
                flex: none;
                width: 100%;
                order: 1;
                height: 70vw;
                min-height: 300px;
                max-height: 440px;
            }
            .hero-image img { object-position: center top; }
            .hero h1 { font-size: 2.6rem; }
            .hero p { font-size: 0.95rem; max-width: 100%; margin-bottom: 1.5rem; }
            .btn-contact { padding: 1rem 2rem; font-size: 0.8rem; }

            /* Marquee */
            .marquee-item { font-size: 0.42rem; padding: 0 1rem; }

            /* Stats */
            .stats-section { padding: 2rem 5%; }
            .stats-grid { grid-template-columns: repeat(2, 1fr); gap: 2rem; }
            .stat-item:not(:last-child)::after { display: none; }
            .stat-number { font-size: 2.2rem; }

            /* Marcas */
            .brands-section { padding: 2.5rem 5%; }
            .brands-grid { grid-template-columns: repeat(3, 1fr); gap: 1rem; }
            .brand-circle { width: 80px; height: 80px; }
            .brand-name { font-size: 0.55rem; max-width: 80px; }

            /* Videos */
            #videos { padding: 2rem 5%; }
            .section-title { font-size: 2.2rem; margin-bottom: 0.5rem; }
            .card-item { width: 190px; }
            .phone-card { width: 190px; }
            .phone-card-frame iframe { width: 320px; height: 569px; transform: scale(0.594); }
            .carousel-btn { width: 34px; height: 34px; font-size: 1.1rem; }

            /* Servicios */
            section#tarifas { padding: 2.5rem 5%; }
            .pricing-grid { grid-template-columns: 1fr; max-width: 360px; margin: 0 auto; }
            .pricing-card { padding: 2.5rem 1.5rem; }
            .pricing-card.featured { transform: scale(1); margin: 0; }

            /* General */
            section { padding: 2.5rem 5%; }
        }
    </style>
</head>
<body>

    <header id="main-header">
        <div class="social-links">
            <a href="https://www.instagram.com/jeni_torres/" target="_blank" class="social-icon" aria-label="Instagram">
                <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                </svg>
            </a>
            <a href="https://www.tiktok.com/@jenitorre5" target="_blank" class="social-icon" aria-label="TikTok">
                <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-2.88 2.5 2.89 2.89 0 0 1-2.89-2.89 2.89 2.89 0 0 1 2.89-2.89c.28 0 .54.04.79.1V9.01a6.27 6.27 0 0 0-.79-.05 6.34 6.34 0 0 0-6.34 6.34 6.34 6.34 0 0 0 6.34 6.34 6.34 6.34 0 0 0 6.33-6.34V8.69a8.18 8.18 0 0 0 4.79 1.52V6.69a4.85 4.85 0 0 1-1.02 0z"/>
                </svg>
            </a>
        </div>
        <button class="hamburger" id="hamburgerBtn" aria-label="Abrir menú">
            <span></span><span></span><span></span>
        </button>
        <nav id="mainNav">
            <button class="nav-close" id="navClose" aria-label="Cerrar menú">✕</button>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#marcas">Marcas</a></li>
                <li><a href="#videos">Top 5</a></li>
                <li><a href="#tarifas">Servicios</a></li>
                <li><a href="#" class="contact-trigger">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="inicio" class="hero">
            <div class="hero-text">
                <h1>Jeni Torres</h1>
                <p>Creadora de contenido UGC y maketing manager.<br>Te ayudo a humanizar tu marca con autenticidad y estilo.</p>
                <a href="#" class="btn-contact contact-trigger">Comenzar un proyecto</a>
            </div>
            <div class="hero-image">
                <img src="images/jeni-torres.png" alt="Jeni Torres">
            </div>
        </section>

        <div class="marquee-wrapper" aria-hidden="true">
            <div class="marquee-track">
                <span class="marquee-item">CREACIÓN DE CONTENIDO</span><span class="marquee-sep">+</span>
                <span class="marquee-item">UNBOXING</span><span class="marquee-sep">+</span>
                <span class="marquee-item">CONTENIDO PARA MARCAS</span><span class="marquee-sep">+</span>
                <span class="marquee-item">MEDIA KIT</span><span class="marquee-sep">+</span>
                <span class="marquee-item">ESTRATEGIA</span><span class="marquee-sep">+</span>
                <span class="marquee-item">UGC</span><span class="marquee-sep">+</span>
                <span class="marquee-item">FOTOGRAFÍA</span><span class="marquee-sep">+</span>
                <span class="marquee-item">REELS & TIKTOK</span><span class="marquee-sep">+</span>
                <span class="marquee-item">CREACIÓN DE CONTENIDO</span><span class="marquee-sep">+</span>
                <span class="marquee-item">UNBOXING</span><span class="marquee-sep">+</span>
                <span class="marquee-item">CONTENIDO PARA MARCAS</span><span class="marquee-sep">+</span>
                <span class="marquee-item">MEDIA KIT</span><span class="marquee-sep">+</span>
                <span class="marquee-item">ESTRATEGIA</span><span class="marquee-sep">+</span>
                <span class="marquee-item">UGC</span><span class="marquee-sep">+</span>
                <span class="marquee-item">FOTOGRAFÍA</span><span class="marquee-sep">+</span>
                <span class="marquee-item">REELS & TIKTOK</span><span class="marquee-sep">+</span>
            </div>
        </div>

        </section>
<div class="stats-section" id="stats-section">
            <div class="stats-grid">
                <div class="stat-item">
                    <span class="stat-number" data-target="20" data-suffix="+">0+</span>
                    <span class="stat-label">Colaboraciones</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number" data-target="6" data-suffix="K+">0K+</span>
                    <span class="stat-label">Followers TikTok</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number" data-target="3" data-suffix="K+">0K+</span>
                    <span class="stat-label">Followers Instagram</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number" data-target="3" data-suffix="+">0+</span>
                    <span class="stat-label">Años Creando</span>
                </div>
            </div>
        </div>

        <section id="marcas" class="brands-section">
            <h2 class="section-title">Colaboraciones</h2>
            <p class="brand-hint">Toca y descubre lo que creamos juntos</p>

            <div class="brands-grid">
                <div class="brand-item">
                    <a href="https://www.instagram.com/p/DYIJFStAoH0/" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/p/DYIJFStAoH0/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Kotex</span>
                </div>
                 <div class="brand-item">
                    <a href="https://www.instagram.com/p/DdNKND_AiEK/" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/p/DdNKND_AiEK/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Nua</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/reel/CkWuuEGA0Sr/?igsh=MTUza2EyOWJlZ3Y3aw==" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/reel/CkWuuEGA0Sr/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Zafulve</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/reel/C4ZKUKIrSXx/?igsh=bWxzNTBjMng5ZzY0" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/reel/C4ZKUKIrSXx/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Respirando bajo el agua</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/reel/C5eg6mjL2iz/?igsh=MXVuNGFyMmNwNWRlcw==" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/reel/C5eg6mjL2iz/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Eco turismo extremo</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/reel/DHCPpVuSM3u/?igsh=MTZneGx3ZW03Nmdndg==" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/reel/DHCPpVuSM3u/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">A todo color</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/reel/DVhPgrKj4ZI/?igsh=MW1uZGNob3kzeXZuZw==" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/reel/DVhPgrKj4ZI/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Musart store</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/reel/CtR5Iaksyw5/?igsh=ZzUxZm9idzF3amZ2" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/reel/CtR5Iaksyw5/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Punto Go</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/p/CsUYEhcODe2/?img_index=1&igsh=cWpvcW9mMHg1NHIx" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/p/CsUYEhcODe2/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Páramo café</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/p/CfclErhrpzH/?igsh=MXhkYndzb25iYzI1Mw==" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/p/CfclErhrpzH/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Ameli</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/p/DMteHYsS-6e/?igsh=cHA4MjZ2NHZweHJ2" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/p/DMteHYsS-6e/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Toursrlg</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/p/CmOpEWHr2AM/?igsh=MXZxYjQ0dnBuMTc3MA==" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/p/CmOpEWHr2AM/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Oro café</span>
                </div>
                <div class="brand-item">
                    <a href="https://www.instagram.com/p/C-qcXheN0Ht/?igsh=N3g5MDc5cXcyZmQ2" target="_blank" class="brand-circle"><iframe src="https://www.instagram.com/p/C-qcXheN0Ht/embed/" style="position:absolute;top:0;left:0;width:612px;height:612px;border:none;transform:scale(0.1797);transform-origin:top left;pointer-events:none;" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" frameborder="0"></iframe></a>
                    <span class="brand-name">Chocology</span>
                </div>
            </div>
        </section>
        <section id="videos">
            <h2 class="section-title">Top 5</h2>
            <p class="brand-hint">De mi contenido más cool</p>
            <div class="carousel-wrapper">
                <button class="carousel-btn prev" id="carouselPrev">&#8249;</button>
                <div class="carousel-outer">
                    <div class="carousel-track" id="carouselTrack">
                        <div class="card-item">
                            <div class="phone-card">
                                <div class="phone-card-frame" style="display:block">
                                    <iframe src="https://www.tiktok.com/embed/v2/7641766299466583313" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" sandbox="allow-scripts allow-same-origin allow-popups allow-popups-to-escape-sandbox allow-presentation"></iframe>
                                </div>
                            </div>
                            <div class="card-meta">
                                <span class="card-num">01</span>
                                <h3>UNBOXING</h3>
                                <span class="card-tag">Cashea & damasco · TikTok</span>
                                <a class="card-link" href="https://vt.tiktok.com/ZSx5HNej9/" target="_blank">Ver en Redes ↗</a>
                            </div>
                        </div>
                        <div class="card-item">
                            <div class="phone-card">
                                <div class="phone-card-frame" style="display:block">
                                    <iframe src="https://www.tiktok.com/embed/v2/7650929185757711632" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" sandbox="allow-scripts allow-same-origin allow-popups allow-popups-to-escape-sandbox allow-presentation"></iframe>
                                </div>
                            </div>
                            <div class="card-meta">
                                <span class="card-num">02</span>
                                <h3>UNBOXING</h3>
                                <span class="card-tag">0% Inicial Cashea· TikTok</span>
                                <a class="card-link" href="https://www.tiktok.com/@jenitorre5/video/7650929185757711632" target="_blank">Ver en Redes ↗</a>
                            </div>
                        </div>
                        <div class="card-item">
                            <div class="phone-card">
                                <div class="phone-card-frame" style="display:block">
                                    <iframe src="https://www.tiktok.com/embed/v2/7603161537129336080" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" sandbox="allow-scripts allow-same-origin allow-popups allow-popups-to-escape-sandbox allow-presentation"></iframe>
                                </div>
                            </div>
                            <div class="card-meta">
                                <span class="card-num">04</span>
                                <h3>Construyendo mi hogar</h3>
                                <span class="card-tag">Con Cashea · TikTok</span>
                                <a class="card-link" href="https://www.tiktok.com/@jenitorre5/video/7603161537129336080" target="_blank">Ver en Redes ↗</a>
                            </div>
                        </div>
                        <div class="card-item">
                            <div class="phone-card">
                                <div class="phone-card-frame" style="display:block">
                                    <iframe src="https://www.tiktok.com/embed/v2/7647700411230489857" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" sandbox="allow-scripts allow-same-origin allow-popups allow-popups-to-escape-sandbox allow-presentation"></iframe>
                                </div>
                            </div>
                            <div class="card-meta">
                                <span class="card-num">05</span>
                                <h3>UNBOXING</h3>
                                <span class="card-tag">Tijerazo & Cashea · TikTok</span>
                                <a class="card-link" href="https://www.tiktok.com/@jenitorre5/video/7647700411230489857" target="_blank">Ver en Redes ↗</a>
                            </div>
                        </div>
                        <div class="card-item">
                            <div class="phone-card">
                                <div class="phone-card-frame" style="display:block">
                                    <iframe src="https://www.tiktok.com/embed/v2/7642143085584977153" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowtransparency="true" scrolling="no" sandbox="allow-scripts allow-same-origin allow-popups allow-popups-to-escape-sandbox allow-presentation"></iframe>
                                </div>
                            </div>
                            <div class="card-meta">
                                <span class="card-num">06</span>
                                <h3>Review</h3>
                                <span class="card-tag">Recomendación · TikTok</span>
                                <a class="card-link" href="https://www.tiktok.com/@jenitorre5/video/7642143085584977153" target="_blank">Ver en Redes ↗</a> 
                            </div>
                        </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <button class="carousel-btn next" id="carouselNext">&#8250;</button>
            </div>
        </section>


        <section id="tarifas">
            <h2 class="section-title">Paquetes</h2>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <h3>Basico</h3>
                    <div class="price">80<span>$</span></div>
                    <ul class="features-list">
                        <li>1 Reels</li>
                        <li>4 Story</li>
                        <li>1 Ronda de Cambios</li>
                    </ul>
                    <br>
                    <a href="#" class="btn-contact contact-trigger" style="padding: 0.8rem 2rem; font-size: 0.7rem;">Seleccionar</a>
                </div>
                <div class="pricing-card featured">
                    <h3>Estándar</h3>
                    <div class="price">120<span>$</span></div>
                    <ul class="features-list">
                        <li>1 Reels</li>
                        <li>Ráfaga de Story</li>
                        <li>1 Video en Tiktok</li>
                        <li>2 Rondas de Cambios</li>
                    </ul>
                    <br>
                    <a href="#" class="btn-contact contact-trigger" style="padding: 0.8rem 2rem; font-size: 0.7rem;">Seleccionar</a>
                </div>
                <div class="pricing-card">
                    <h3>Premium</h3>
                    <div class="price">150<span>$</span></div>
                    <ul class="features-list">
                        <li>2 Reels</li>
                        <li>Ráfaga de Story</li>
                        <li>1 Video en Tiktok</li>
                        <li>3 Rondas de Cambios</li>
                    </ul>
                    <br>
                    <a href="#" class="btn-contact contact-trigger" style="padding: 0.8rem 2rem; font-size: 0.7rem;">Seleccionar</a>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <span class="footer-logo">Jeni Torres</span>
        <p class="copyright">© 2026 · Creadora de contenido</p>
        <div class="footer-social">
            <a href="https://www.instagram.com/jeni_torres/" target="_blank" class="social-icon" aria-label="Instagram">
                <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                </svg>
            </a>
            <a href="https://www.tiktok.com/@jenitorre5" target="_blank" class="social-icon" aria-label="TikTok">
                <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-2.88 2.5 2.89 2.89 0 0 1-2.89-2.89 2.89 2.89 0 0 1 2.89-2.89c.28 0 .54.04.79.1V9.01a6.27 6.27 0 0 0-.79-.05 6.34 6.34 0 0 0-6.34 6.34 6.34 6.34 0 0 0 6.34 6.34 6.34 6.34 0 0 0 6.33-6.34V8.69a8.18 8.18 0 0 0 4.79 1.52V6.69a4.85 4.85 0 0 1-1.02 0z"/>
                </svg>
            </a>
        </div>
    </footer>

    <script>
        /*
          LÓGICA DE NAVEGACIÓN Y CONTACTO
        */

        //
        const CONTACT_URL = "https://api.whatsapp.com/send/?phone=584129198963&text=Hola%20Jeni!%20Me%20interesa%20trabajar%20contigo&type=phone_number&app_absent=0"; 

        const contactButtons = document.querySelectorAll('.contact-trigger');

        contactButtons.forEach(btn => {
            btn.addEventListener('click', (e) => {
                e.preventDefault();
                window.open(CONTACT_URL, '_blank');
            });
        });

        // Animated counters
        function animateCounter(el, target, suffix, duration) {
            let startTime = null;
            function step(timestamp) {
                if (!startTime) startTime = timestamp;
                const progress = Math.min((timestamp - startTime) / duration, 1);
                const value = Math.floor(progress * target);
                el.textContent = value + suffix;
                if (progress < 1) requestAnimationFrame(step);
                else el.textContent = target + suffix;
            }
            requestAnimationFrame(step);
        }

        function runCounters(section) {
            section.querySelectorAll('.stat-number').forEach((counter) => {
                const target = parseInt(counter.dataset.target, 10);
                const suffix = counter.dataset.suffix || '';
                animateCounter(counter, target, suffix, 2000);
            });
        }

        const statsSection = document.getElementById('stats-section');

        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    runCounters(entry.target);
                    statsObserver.unobserve(entry.target);
                }
            });
        }, { threshold: 0 });

        if (statsSection) {
            statsObserver.observe(statsSection);
        }

        // Carousel (solo botones, sin loop)
        (function() {
            var track = document.getElementById('carouselTrack');
            var outer = document.querySelector('.carousel-outer');
            if (!track || !outer) return;
            var STEP = 276;
            var NUM_CARDS = 10;
            var pos = 0;
            track.style.transition = 'none';
            track.style.transform = 'translateX(0)';

            function maxPos() {
                return Math.max(0, NUM_CARDS * STEP - outer.offsetWidth);
            }

            function shift(dir) {
                pos += dir * STEP;
                if (pos < 0) pos = 0;
                var max = maxPos();
                if (pos > max) pos = max;
                track.style.transition = 'transform 0.35s ease';
                track.style.transform = 'translateX(-' + pos + 'px)';
                setTimeout(function() { track.style.transition = 'none'; }, 350);
            }

            document.getElementById('carouselPrev').addEventListener('click', function() { shift(-1); });
            document.getElementById('carouselNext').addEventListener('click', function() { shift(1); });

            var touchStartX = 0;
            outer.addEventListener('touchstart', function(e) { touchStartX = e.touches[0].clientX; }, { passive: true });
            outer.addEventListener('touchend', function(e) {
                var diff = touchStartX - e.changedTouches[0].clientX;
                if (Math.abs(diff) > 40) shift(diff > 0 ? 1 : -1);
            }, { passive: true });

            window.pauseCarousel = function() {};
            window.resumeCarousel = function() {};
        })();

        // Menú hamburger
        var hamburgerBtn = document.getElementById('hamburgerBtn');
        var mainNav = document.getElementById('mainNav');
        var navClose = document.getElementById('navClose');
        if (hamburgerBtn && mainNav && navClose) {
            hamburgerBtn.addEventListener('click', function() { mainNav.classList.add('open'); });
            navClose.addEventListener('click', function() { mainNav.classList.remove('open'); });
            mainNav.querySelectorAll('a').forEach(function(a) {
                a.addEventListener('click', function() { mainNav.classList.remove('open'); });
            });
        }

    </script>
</body>
</html>
