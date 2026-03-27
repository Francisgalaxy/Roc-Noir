<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Tipografía elegante estilo Gucci -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* --- RESET Y ESTILOS GLOBALES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #000;
            color: #fff;
            font-family: 'Source Sans 3', sans-serif;
            font-weight: 300;
            line-height: 1.6;
        }

        /* --- TIPOGRAFÍA ELEGANTE --- */
        h1, h2, h3, h4, .logo, .btn-gold, .nav-link {
            font-family: 'Playfair Display', serif;
            font-weight: 400;
            letter-spacing: 1px;
        }

        /* --- ENLACES --- */
        a {
            text-decoration: none;
            color: inherit;
            transition: color 0.3s;
        }

        /* --- CONTENEDOR PRINCIPAL --- */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 40px;
        }

        /* --- HEADER (INSPIRADO EN GUCCI) --- */
        header {
            padding: 30px 0;
            border-bottom: 1px solid rgba(196, 161, 90, 0.2);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .logo {
            font-size: 2rem;
            font-weight: 600;
            color: #C4A15A;
            text-transform: uppercase;
            letter-spacing: 4px;
        }

        nav ul {
            display: flex;
            gap: 40px;
            list-style: none;
        }

        .nav-link {
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: #fff;
            padding-bottom: 5px;
            border-bottom: 1px solid transparent;
            transition: border-color 0.3s, color 0.3s;
        }

        .nav-link:hover {
            border-bottom-color: #C4A15A;
            color: #C4A15A;
        }

        /* --- HERO SECTION --- */
        .hero {
            margin: 60px 0 80px;
            position: relative;
            height: 70vh;
            min-height: 500px;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?q=80&w=2070&auto=format&fit=crop') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            border-radius: 4px;
            border: 1px solid #C4A15A;
        }

        .hero-content {
            max-width: 800px;
        }

        .hero-subtitle {
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 6px;
            color: #C4A15A;
            margin-bottom: 20px;
        }

        .hero-title {
            font-size: clamp(2.5rem, 8vw, 5rem);
            font-weight: 700;
            line-height: 1.1;
            margin-bottom: 30px;
            color: #fff;
            text-transform: uppercase;
        }

        .hero-description {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 40px;
            color: #ccc;
        }

        .btn-gold {
            background: transparent;
            border: 1px solid #C4A15A;
            color: #C4A15A;
            padding: 15px 40px;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            cursor: pointer;
            transition: all 0.4s ease;
            font-weight: 600;
            display: inline-block;
        }

        .btn-gold:hover {
            background-color: #C4A15A;
            color: #000;
        }

        /* --- SECCIONES GENERALES --- */
        .section {
            margin: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title {
            font-size: 2.5rem;
            color: #C4A15A;
            text-transform: uppercase;
            letter-spacing: 4px;
            margin-bottom: 20px;
        }

        .section-subtitle {
            color: #777;
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* --- TARJETAS DE PRODUCTO (ESTILO GUCCI) --- */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .product-card {
            background-color: #0a0a0a;
            border: 1px solid #222;
            transition: border-color 0.3s;
        }

        .product-card:hover {
            border-color: #C4A15A;
        }

        .product-image {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-bottom: 2px solid #C4A15A;
        }

        .product-info {
            padding: 25px 20px;
            text-align: center;
        }

        .product-category {
            color: #C4A15A;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 8px;
        }

        .product-name {
            font-size: 1.4rem;
            margin-bottom: 10px;
            font-weight: 400;
        }

        .product-price {
            color: #C4A15A;
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 20px;
        }

        .product-btn {
            background: transparent;
            border: 1px solid #C4A15A;
            color: #C4A15A;
            padding: 10px 25px;
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.3s;
            font-family: 'Playfair Display', serif;
        }

        .product-btn:hover {
            background-color: #C4A15A;
            color: #000;
        }

        /* --- SECCIÓN DE CATEGORÍAS (TU DISEÑO ORIGINAL MEJORADO) --- */
        .categorias-grid {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
            margin-top: 30px;
        }

        .categoria-item {
            flex: 1 1 200px;
            background: #111;
            border: 1px solid #222;
            padding: 40px 20px;
            text-align: center;
            transition: border-color 0.3s;
        }

        .categoria-item:hover {
            border-color: #C4A15A;
        }

        .categoria-icono {
            font-size: 2.5rem;
            color: #C4A15A;
            margin-bottom: 20px;
        }

        .categoria-titulo {
            font-size: 1.2rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 10px;
        }

        .categoria-desc {
            color: #777;
            font-size: 0.8rem;
            margin-bottom: 20px;
        }

        /* --- FOOTER ELEGANTE --- */
        footer {
            border-top: 1px solid rgba(196, 161, 90, 0.2);
            padding: 60px 0 30px;
            margin-top: 80px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col h4 {
            color: #C4A15A;
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 20px;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col li {
            margin-bottom: 10px;
        }

        .footer-col a {
            color: #aaa;
            font-size: 0.9rem;
            transition: color 0.3s;
        }

        .footer-col a:hover {
            color: #C4A15A;
        }

        .copyright {
            text-align: center;
            color: #555;
            font-size: 0.8rem;
            border-top: 1px solid #222;
            padding-top: 30px;
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                text-align: center;
            }
            nav ul {
                gap: 20px;
                flex-wrap: wrap;
                justify-content: center;
            }
            .hero {
                height: 60vh;
            }
            .container {
                padding: 0 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- HEADER -->
        <header>
            <div class="logo">ROC NOIR</div>
            <nav>
                <ul>
                    <li><a href="#" class="nav-link">Colecciones</a></li>
                    <li><a href="#" class="nav-link">Prendas</a></li>
                    <li><a href="#" class="nav-link">Ecodiseño</a></li>
                    <li><a href="#" class="nav-link">Atelier</a></li>
                </ul>
            </nav>
        </header>

        <!-- HERO SECTION -->
        <section class="hero">
            <div class="hero-content">
                <p class="hero-subtitle">The art of wearing power</p>
                <h1 class="hero-title">Elegancia Oscura</h1>
                <p class="hero-description">Descubre la nueva colección otoño/invierno, donde la sofisticación se encuentra con la vanguardia.</p>
                <a href="#" class="btn-gold">Explorar</a>
            </div>
        </section>

        <!-- SECCIÓN DE CATEGORÍAS (similar a tu idea original pero expandida) -->
        <section class="section">
            <div class="section-header">
                <h2 class="section-title">Categorías</h2>
                <p class="section-subtitle">Precisión y calidad en cada detalle</p>
            </div>
            <div class="categorias-grid">
                <div class="categoria-item">
                    <div class="categoria-icono">👔</div>
                    <h3 class="categoria-titulo">Moda</h3>
                    <p class="categoria-desc">Alta costura con identidad</p>
                    <button class="product-btn">Ver más</button>
                </div>
                <div class="categoria-item">
                    <div class="categoria-icono">🏋️</div>
                    <h3 class="categoria-titulo">Deporte</h3>
                    <p class="categoria-desc">Elegancia en movimiento</p>
                    <button class="product-btn">Ver más</button>
                </div>
                <div class="categoria-item">
                    <div class="categoria-icono">🌿</div>
                    <h3 class="categoria-titulo">Salud</h3>
                    <p class="categoria-desc">Bienestar consciente</p>
                    <button class="product-btn">Ver más</button>
                </div>
            </div>
        </section>

        <!-- SECCIÓN DE PRODUCTOS DESTACADOS (nueva) -->
        <section class="section">
            <div class="section-header">
                <h2 class="section-title">Prendas destacadas</h2>
                <p class="section-subtitle">La nueva temporada ya está aquí</p>
            </div>
            <div class="product-grid">
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1539008835657-9e8e9680c956?q=80&w=1887&auto=format&fit=crop" alt="Vestido negro" class="product-image">
                    <div class="product-info">
                        <p class="product-category">Moda</p>
                        <h3 class="product-name">Vestido de noche</h3>
                        <p class="product-price">$1,290</p>
                        <button class="product-btn">Ver detalles</button>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1523381210434-271e8be1f52b?q=80&w=1770&auto=format&fit=crop" alt="Chaqueta de cuero" class="product-image">
                    <div class="product-info">
                        <p class="product-category">Ecodiseño</p>
                        <h3 class="product-name">Chaqueta sostenible</h3>
                        <p class="product-price">$2,450</p>
                        <button class="product-btn">Ver detalles</button>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1556905055-8f358a7a47b2?q=80&w=1770&auto=format&fit=crop" alt="Traje gris" class="product-image">
                    <div class="product-info">
                        <p class="product-category">Deporte</p>
                        <h3 class="product-name">Traje técnico</h3>
                        <p class="product-price">$890</p>
                        <button class="product-btn">Ver detalles</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECCIÓN ECODISEÑO (inspirada en tu segunda sección) -->
        <section class="section">
            <div class="section-header">
                <h2 class="section-title">Ecodiseño consciente</h2>
                <p class="section-subtitle">Sostenibilidad y rediseño</p>
            </div>
            <div style="text-align: center; max-width: 700px; margin: 0 auto;">
                <p style="color: #ccc; margin-bottom: 30px;">Cada prenda está creada con materiales reciclados y procesos éticos, sin perder la esencia del lujo.</p>
                <button class="btn-gold">Descubrir colección</button>
            </div>
        </section>

        <!-- FOOTER -->
        <footer>
            <div class="footer-content">
                <div class="footer-col">
                    <h4>ROC NOIR</h4>
                    <ul>
                        <li><a href="#">Sobre nosotros</a></li>
                        <li><a href="#">Atelier</a></li>
                        <li><a href="#">Sostenibilidad</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Ayuda</h4>
                    <ul>
                        <li><a href="#">Contacto</a></li>
                        <li><a href="#">Envíos</a></li>
                        <li><a href="#">Devoluciones</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Redes</h4>
                    <ul>
                        <li><a href="#">Instagram</a></li>
                        <li><a href="#">Pinterest</a></li>
                        <li><a href="#">X (Twitter)</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>© 2025 ROC NOIR Atelier Digital. Todos los derechos reservados.</p>
            </div>
        </footer>
    </div>
</body>
</html>
