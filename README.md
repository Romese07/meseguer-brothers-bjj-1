<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meseguer Brothers JiuJitsu | Instructor & Competidor | Barcelona</title>
    <meta name="description" content="Román Meseguer - Instructor de JiuJitsu, competidor y cinturón morado. Entrenamientos en Barcelona y Castelldefels. Clases para niños y adultos.">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700;800&family=Oswald:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #FF0000; /* Rojo del logo */
            --secondary: #000000; /* Negro del logo */
            --dark: #0A0A0A;
            --light: #F5F5F5;
            --gray: #2A2A2A;
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: var(--dark);
            color: var(--light);
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        h1, h2, h3, h4 {
            font-family: 'Oswald', sans-serif;
            font-weight: 700;
            letter-spacing: 1px;
            line-height: 1.2;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* HEADER */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(10, 10, 10, 0.9);
            backdrop-filter: blur(10px);
            padding: 15px 0;
            transition: var(--transition);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo-img {
            height: 50px;
            width: auto;
        }

        .logo-text {
            font-family: 'Oswald', sans-serif;
            font-weight: 700;
            font-size: 1.5rem;
            margin-left: 10px;
            color: var(--light);
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        /* HERO SECTION */
        .hero {
            height: 100vh;
            background: 
                linear-gradient(rgba(10, 10, 10, 0.7), rgba(10, 10, 10, 0.9)),
                url('logo_circulo_rojo_y_negro.jpg') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            animation: fadeInUp 1.2s ease;
        }

        .hero-content h1 {
            font-size: 4.5rem;
            margin-bottom: 15px;
            text-transform: uppercase;
            background: linear-gradient(to right, var(--primary), #FF6B6B);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .hero-content p {
            font-size: 1.4rem;
            margin-bottom: 30px;
            color: #DDD;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-badge {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 8px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 30px;
            letter-spacing: 1px;
        }

        .btn-main {
            display: inline-block;
            padding: 14px 32px;
            background: var(--primary);
            color: white;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.1rem;
            text-decoration: none;
            transition: var(--transition);
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 5px 15px rgba(255, 0, 0, 0.3);
            margin: 0 10px;
        }

        .btn-main:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 0, 0, 0.4);
            background: #FF3333;
        }

        .btn-secondary {
            display: inline-block;
            padding: 14px 32px;
            background: transparent;
            color: var(--light);
            border: 2px solid var(--primary);
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.1rem;
            text-decoration: none;
            transition: var(--transition);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin: 0 10px;
        }

        .btn-secondary:hover {
            background: rgba(255, 0, 0, 0.1);
            transform: translateY(-3px);
        }

        .scroll-indicator {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            color: var(--light);
            font-size: 1.5rem;
            animation: bounce 2s infinite;
        }

        /* SECTIONS */
        section {
            padding: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 70px;
        }

        .section-header h2 {
            font-size: 2.8rem;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-header h2:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary);
        }

        .section-header p {
            max-width: 700px;
            margin: 0 auto;
            color: #AAA;
            font-size: 1.1rem;
        }

        /* ABOUT SECTION */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--primary);
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .profile-photo {
            flex: 0 0 300px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            position: relative;
        }

        .profile-photo img {
            width: 100%;
            height: auto;
            display: block;
            transition: var(--transition);
        }

        .profile-photo:hover img {
            transform: scale(1.05);
        }

        .profile-photo:after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 3px solid var(--primary);
            border-radius: 10px;
            opacity: 0;
            transition: var(--transition);
        }

        .profile-photo:hover:after {
            opacity: 1;
            transform: scale(0.95);
        }

        /* TIMELINE SECTION */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline:before {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 2px;
            background: var(--primary);
            transform: translateX(-50%);
        }

        .timeline-item {
            position: relative;
            margin-bottom: 50px;
            width: 50%;
            padding: 0 40px;
        }

        .timeline-item:nth-child(odd) {
            left: 0;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
        }

        .timeline-content {
            background: var(--gray);
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            transition: var(--transition);
        }

        .timeline-content:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
        }

        .timeline-content:after {
            content: '';
            position: absolute;
            top: 20px;
            width: 20px;
            height: 20px;
            background: var(--gray);
            transform: rotate(45deg);
        }

        .timeline-item:nth-child(odd) .timeline-content:after {
            right: -10px;
        }

        .timeline-item:nth-child(even) .timeline-content:after {
            left: -10px;
        }

        .timeline-year {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 5px 15px;
            border-radius: 30px;
            font-weight: 700;
            margin-bottom: 15px;
            font-size: 0.9rem;
        }

        .timeline-content h4 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--light);
        }

        /* VALUES SECTION */
        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .value-card {
            background: var(--gray);
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            transition: var(--transition);
            border-bottom: 3px solid transparent;
        }

        .value-card:hover {
            transform: translateY(-10px);
            border-bottom: 3px solid var(--primary);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }

        .value-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .value-card h4 {
            font-size: 1.3rem;
            margin-bottom: 15px;
        }

        /* SCHEDULE SECTION */
        .schedule-container {
            display: flex;
            gap: 40px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .schedule-card {
            background: var(--gray);
            padding: 30px;
            border-radius: 10px;
            flex: 1;
            min-width: 300px;
            text-align: center;
            transition: var(--transition);
        }

        .schedule-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }

        .schedule-card h3 {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 1.5rem;
        }

        .schedule-card p {
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .schedule-highlight {
            color: var(--primary);
            font-weight: 700;
        }

        /* SOCIAL SECTION */
        .social-section {
            text-align: center;
        }

        .social-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .social-btn {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: var(--transition);
            min-width: 200px;
            justify-content: center;
        }

        .instagram-btn {
            background: linear-gradient(45deg, #405DE6, #5851DB, #833AB4, #C13584, #E1306C, #FD1D1D);
            color: white;
        }

        .whatsapp-btn {
            background: #25D366;
            color: white;
        }

        .youtube-btn {
            background: #FF0000;
            color: white;
        }

        .social-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        /* FORM SECTION */
        .form-container {
            max-width: 700px;
            margin: 0 auto;
            background: var(--gray);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .form-control {
            width: 100%;
            padding: 15px;
            background: #1A1A1A;
            border: 1px solid #444;
            border-radius: 5px;
            color: var(--light);
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(255, 0, 0, 0.2);
        }

        .submit-btn {
            width: 100%;
            padding: 15px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 5px;
            font-weight: 700;
            font-size: 1.1rem;
            cursor: pointer;
            transition: var(--transition);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .submit-btn:hover {
            background: #FF3333;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 0, 0, 0.3);
        }

        /* FOOTER */
        footer {
            background: #050505;
            padding: 60px 0 30px;
            text-align: center;
        }

        .footer-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .footer-logo {
            font-family: 'Oswald', sans-serif;
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--primary);
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: #AAA;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .copyright {
            color: #777;
            margin-top: 30px;
            font-size: 0.9rem;
        }

        /* ANIMATIONS */
        @keyframes fadeInUp {
            from {opacity: 0; transform: translateY(50px);}
            to {opacity: 1; transform: translateY(0);}
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0) translateX(-50%);}
            40% {transform: translateY(-20px) translateX(-50%);}
            60% {transform: translateY(-10px) translateX(-50%);}
        }

        /* RESPONSIVE */
        @media (max-width: 992px) {
            .hero-content h1 {
                font-size: 3.5rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .profile-photo {
                flex: 0 0 250px;
            }
            
            .timeline:before {
                left: 30px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 0;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-content:after {
                left: -10px !important;
            }
        }

        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.8rem;
            }
            
            .section-header h2 {
                font-size: 2.2rem;
            }
            
            .btn-main, .btn-secondary {
                display: block;
                margin: 10px auto;
                width: 80%;
                max-width: 300px;
            }
            
            .social-btn {
                width: 100%;
                max-width: 300px;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
        }
    </style>
</head>

<body>

<!-- HEADER -->
<header class="header">
    <div class="container header-container">
        <div class="logo">
            <img src="logo_circulo_rojo_y_negro.jpg" alt="Meseguer Brothers JiuJitsu" class="logo-img">
            <div class="logo-text">MESEGUER BROTHERS</div>
        </div>
        <nav class="nav-links">
            <a href="#perfil">Sobre Mí</a>
            <a href="#trayectoria">Trayectoria</a>
            <a href="#valores">Valores</a>
            <a href="#horarios">Horarios</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </div>
</header>

<!-- HERO SECTION -->
<section class="hero">
    <div class="hero-content">
        <div class="hero-badge">CINTURÓN MORADO · CICERO COSTHA</div>
        <h1>MESEGUER BROTHERS JIUJITSU</h1>
        <p>Instructor · Competidor · Formador de Campeones · Barcelona & Castelldefels</p>
        <div class="hero-buttons">
            <a href="#perfil" class="btn-main">Conoce Mi Historia</a>
            <a href="#contacto" class="btn-secondary">Únete al Equipo</a>
        </div>
    </div>
    <div class="scroll-indicator">
        <i class="fas fa-chevron-down"></i>
    </div>
</section>

<!-- ABOUT SECTION -->
<section id="perfil">
    <div class="container">
        <div class="section-header">
            <h2>SOBRE MÍ</h2>
            <p>Mi viaje en el JiuJitsu comenzó en 2012 y continúa con la misma pasión y dedicación</p>
        </div>
        <div class="about-content">
            <div class="about-text">
                <h3>Román Meseguer</h3>
                <p>Hola, soy <strong>Román Meseguer</strong>, practicante de JiuJitsu desde 2012. Comencé mi camino en Venezuela, continué mi crecimiento en Barcelona y actualmente entreno con el equipo <strong>Tizona</strong> bajo la línea de <strong>Cicero Costha</strong>.</p>
                <p>A lo largo de los años he tenido el privilegio de entrenar con grandes maestros y construir una filosofía basada en disciplina, humildad, marcialidad y trabajo duro. Hoy combino mi rol de competidor con el de instructor, especialmente enfocado en la formación de niños.</p>
                <p>Mi objetivo es transmitir los valores del JiuJitsu a las nuevas generaciones mientras continúo mi desarrollo como competidor y artista marcial.</p>
            </div>
            <div class="profile-photo">
                <img src="roman_perfil_exagerado.jpg" alt="Román Meseguer - Instructor de JiuJitsu">
            </div>
        </div>
    </div>
</section>

<!-- TIMELINE SECTION -->
<section id="trayectoria" style="background: #111;">
    <div class="container">
        <div class="section-header">
            <h2>MI TRAYECTORIA</h2>
            <p>Un viaje de más de una década dedicada al arte suave</p>
        </div>
        <div class="timeline">
            <div class="timeline-item">
                <div class="timeline-content">
                    <span class="timeline-year">2012</span>
                    <h4>Inicio en Venezuela</h4>
                    <p>Comienzo en VJJT con Jorge Malecón Ochoa y Ciriaco de la Porta</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <span class="timeline-year">2014-2016</span>
                    <h4>Formación en Judo</h4>
                    <p>Judo en la Universidad Marítima del Caribe con Douglas Cardoso</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <span class="timeline-year">2018</span>
                    <h4>Llegada a Barcelona</h4>
                    <p>GFTeam con Essio Andrade (cinturón azul)</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <span class="timeline-year">2018-2022</span>
                    <h4>Academia Robin Gracie</h4>
                    <p>Formación continua en la prestigiosa academia</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <span class="timeline-year">2022</span>
                    <h4>Tizona / Cicero Costha</h4>
                    <p>Castelldefels con Edu Da Casa, José Muriel y Cristofer Opazos</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <span class="timeline-year">2024</span>
                    <h4>Cinturón Morado</h4>
                    <p>Otorgado por Edu Da Casa & Cicero Costha</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <span class="timeline-year">Actualidad</span>
                    <h4>Instructor y Competidor</h4>
                    <p>Instructor de niños · Entreno 5 días por semana</p>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- VALUES SECTION -->
<section id="valores">
    <div class="container">
        <div class="section-header">
            <h2>VALORES QUE ME DEFINEN</h2>
            <p>Principios que aplico dentro y fuera del tatami</p>
        </div>
        <div class="values-grid">
            <div class="value-card">
                <div class="value-icon">
                    <i class="fas fa-hands-helping"></i>
                </div>
                <h4>Humildad</h4>
                <p>Mantener los pies en la tierra sin importar los logros alcanzados</p>
            </div>
            <div class="value-card">
                <div class="value-icon">
                    <i class="fas fa-users"></i>
                </div>
                <h4>Trabajo en Equipo</h4>
                <p>Crecer juntos es la base del desarrollo individual y colectivo</p>
            </div>
            <div class="value-card">
                <div class="value-icon">
                    <i class="fas fa-handshake"></i>
                </div>
                <h4>Respeto</h4>
                <p>Confianza, honestidad y respeto hacia compañeros y maestros</p>
            </div>
            <div class="value-card">
                <div class="value-icon">
                    <i class="fas fa-dumbbell"></i>
                </div>
                <h4>Constancia</h4>
                <p>Trabajo duro y dedicación diaria como clave del éxito</p>
            </div>
            <div class="value-card">
                <div class="value-icon">
                    <i class="fas fa-brain"></i>
                </div>
                <h4>Mentalidad Abierta</h4>
                <p>Dejar el ego a un lado para aprender y evolucionar</p>
            </div>
            <div class="value-card">
                <div class="value-icon">
                    <i class="fas fa-trophy"></i>
                </div>
                <h4>Excelencia</h4>
                <p>Buscar la mejor versión de uno mismo en cada entrenamiento</p>
            </div>
        </div>
    </div>
</section>

<!-- SCHEDULE SECTION -->
<section id="horarios" style="background: #111;">
    <div class="container">
        <div class="section-header">
            <h2>HORARIOS DE CLASES</h2>
            <p>Únete a nuestras sesiones de entrenamiento</p>
        </div>
        <div class="schedule-container">
            <div class="schedule-card">
                <h3>CLASES KIDS</h3>
                <p><span class="schedule-highlight">Martes y Jueves</span></p>
                <p>17:00 — 18:00</p>
                <p>Formación en valores y técnica para futuros campeones</p>
            </div>
            <div class="schedule-card">
                <h3>ADULTOS</h3>
                <p><span class="schedule-highlight">Lunes a Viernes</span></p>
                <p>18:00 — 21:00</p>
                <p>Open Mat / Drill / Gi / No-Gi</p>
                <p>Para todos los niveles, desde principiantes hasta avanzados</p>
            </div>
        </div>
    </div>
</section>

<!-- SOCIAL SECTION -->
<section class="social-section">
    <div class="container">
        <div class="section-header">
            <h2>CONECTA CONMIGO</h2>
            <p>Sígueme en redes sociales y mantente al día con mi evolución</p>
        </div>
        <div class="social-buttons">
            <a class="social-btn instagram-btn" href="https://instagram.com/meseguerbrothersbjj" target="_blank">
                <i class="fab fa-instagram"></i> Instagram
            </a>
            <a class="social-btn whatsapp-btn" href="https://wa.me/34600000000" target="_blank">
                <i class="fab fa-whatsapp"></i> WhatsApp
            </a>
            <a class="social-btn youtube-btn" href="#" target="_blank">
                <i class="fab fa-youtube"></i> YouTube
            </a>
        </div>
    </div>
</section>

<!-- FORM SECTION -->
<section id="contacto">
    <div class="container">
        <div class="section-header">
            <h2>ÚNETE A MESEGUER BROTHERS BJJ</h2>
            <p>Comienza tu viaje en el JiuJitsu o lleva tu práctica al siguiente nivel</p>
        </div>
        <div class="form-container">
            <form action="#" method="post">
                <div class="form-group">
                    <label for="name">Tu nombre</label>
                    <input type="text" id="name" class="form-control" placeholder="Ej: Carlos Rodríguez" required>
                </div>
                <div class="form-group">
                    <label for="email">Tu email</label>
                    <input type="email" id="email" class="form-control" placeholder="ejemplo@email.com" required>
                </div>
                <div class="form-group">
                    <label for="experience">Tu experiencia en JiuJitsu</label>
                    <select id="experience" class="form-control">
                        <option value="">Selecciona tu nivel</option>
                        <option value="beginner">Principiante (Sin experiencia)</option>
                        <option value="some">Alguna experiencia</option>
                        <option value="intermediate">Intermedio</option>
                        <option value="advanced">Avanzado</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="message">Cuéntame tu interés o objetivos</label>
                    <textarea id="message" class="form-control" placeholder="Ej: Quiero empezar JiuJitsu para mejorar mi condición física y aprender defensa personal..." rows="4"></textarea>
                </div>
                <button type="submit" class="submit-btn">Enviar Solicitud</button>
            </form>
        </div>
    </div>
</section>

<!-- FOOTER -->
<footer>
    <div class="container">
        <div class="footer-content">
            <div class="footer-logo">MESEGUER BROTHERS JIUJITSU</div>
            <p>Instructor · Competidor · Formador de Campeones</p>
            <div class="footer-links">
                <a href="#perfil">Sobre Mí</a>
                <a href="#horarios">Clases</a>
                <a href="#">Galería</a>
                <a href="#">Blog</a>
                <a href="#contacto">Contacto</a>
            </div>
            <div class="copyright">
                © 2025 Meseguer Brothers JiuJitsu · Creado por Román Meseguer · Barcelona / Castelldefels
            </div>
        </div>
    </div>
</footer>

</body>
</html>

![roman_perfil_exagerado jpg](https://github.com/user-attachments/assets/82f2ab7c-d5a6-4b1e-89e2-babb7486083f)
<img width="1024" height="1536" alt="logo_circulo_rojo_y_negro jpg" src="https://github.com/user-attachments/assets/de163fca-3d58-4567-af1a-dc7c00da6ecb" />
<img width="1024" height="1536" alt="logo_circulo_rojo_y_negro jpg" src="https://github.com/user-attachments/assets/f210d43f-1de3-4419-b77a-bc7f9fe9b0e2" />

