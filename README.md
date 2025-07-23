#AdSoul Marketing
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AdSoul Marketing - Publicidad con Alma</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Tailwind CSS Configuration for custom colors and font -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'adsoul-orange': '#FF7F50', // Naranja vibrante
                        'adsoul-purple': '#4B0082', // Morado oscuro
                        'adsoul-white': '#FFFFFF',
                        'adsoul-light-gray': '#D3D3D3', // Gris claro para fondos de sección (Más oscuro para mejor contraste)
                        'adsoul-dark-gray': '#2C2C2C', // Gris oscuro para texto
                        'adsoul-light-purple': '#8A2BE2', // Un morado más claro para degradados (Azul Violeta)
                        'adsoul-dark-orange': '#E65C00', // Un naranja más oscuro para degradados
                        'adsoul-soft-purple': '#6C3483', // Un morado más suave para el header
                        'adsoul-soft-orange': '#FF9F70', // Un naranja más suave para el header
                    },
                    fontFamily: {
                        sans: ['Poppins', 'sans-serif'], // Cambiado a Poppins
                    },
                }
            },
        }
    </script>
    <!-- Google Fonts - Poppins -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Custom styles for smooth scrolling */
        html {
            scroll-behavior: smooth;
        }

        /* Custom styling for cards and buttons */
        .service-card {
            transition: all 0.3s ease-in-out;
            border: 2px solid transparent;
        }
        .service-card:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.15);
            border-color: #FF7F50; /* adsoul-orange */
        }
        .service-card:hover .service-icon {
            transform: scale(1.1);
            color: #FF7F50; /* adsoul-orange */
        }

        .portfolio-item {
            transition: all 0.3s ease-in-out;
            overflow: hidden;
        }
        .portfolio-item img {
            transition: all 0.3s ease-in-out;
        }
        .portfolio-item:hover img {
            transform: scale(1.05);
            filter: brightness(0.8);
        }
        .portfolio-overlay {
            opacity: 0;
            transition: opacity 0.3s ease-in-out;
            background-color: rgba(75, 0, 130, 0.6); /* adsoul-purple with transparency */
        }
        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        .btn-primary {
            display: inline-block;
            padding: 0.75rem 2rem;
            border-radius: 9999px; /* Fully rounded */
            font-size: 1.125rem; /* text-xl */
            font-weight: 600; /* font-semibold */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease-in-out;
            background: linear-gradient(to right, theme('colors.adsoul-orange'), theme('colors.adsoul-dark-orange'));
            color: theme('colors.adsoul-white');
        }
        .btn-primary:hover {
            transform: translateY(-2px) scale(1.02);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
            background: linear-gradient(to right, theme('colors.adsoul-dark-orange'), theme('colors.adsoul-orange'));
        }

        /* Gradient backgrounds */
        .section-gradient-purple {
            background: linear-gradient(to bottom right, theme('colors.adsoul-purple'), theme('colors.adsoul-light-purple'));
        }
        .section-gradient-orange {
            background: linear-gradient(to bottom left, theme('colors.adsoul-orange'), theme('colors.adsoul-dark-orange'));
        }
        .header-gradient {
            background: linear-gradient(to right, theme('colors.adsoul-soft-purple'), theme('colors.adsoul-soft-orange'));
        }

        /* Text shadow for hero section for better readability */
        .hero-title-shadow {
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.5);
        }
        .hero-slogan-shadow {
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.4);
        }
    </style>
</head>
<body class="font-sans text-adsoul-dark-gray bg-adsoul-white">

    <!-- Header and Navigation -->
    <header class="header-gradient shadow-xl fixed w-full z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <!-- Logo -->
            <a href="#" class="text-adsoul-white text-3xl font-bold rounded-2xl p-2">AdSoul Marketing</a>

            <!-- Desktop Navigation (Always visible in this static version) -->
            <ul class="flex space-x-8">
                <li><a href="#hero" class="text-adsoul-white text-lg font-semibold hover:text-adsoul-orange transition duration-200">Inicio</a></li>
                <li><a href="#services" class="text-adsoul-white text-lg font-semibold hover:text-adsoul-orange transition duration-200">Servicios</a></li>
                <li><a href="#about" class="text-adsoul-white text-lg font-semibold hover:text-adsoul-orange transition duration-200">Nosotros</a></li>
                <li><a href="#portfolio" class="text-adsoul-white text-lg font-semibold hover:text-adsoul-orange transition duration-200">Portafolio</a></li>
                <li><a href="#blog" class="text-adsoul-white text-lg font-semibold hover:text-adsoul-orange transition duration-200">Blog</a></li>
                <li><a href="#contact" class="text-adsoul-white text-lg font-semibold hover:text-adsoul-orange transition duration-200">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="hero" class="relative bg-gradient-to-br from-adsoul-purple to-adsoul-orange text-adsoul-white h-screen flex items-center justify-center text-center overflow-hidden pt-16">
            <div class="absolute inset-0 z-0 opacity-20">
                <!-- Subtle background shapes for visual interest (static) -->
                <div class="absolute top-0 left-0 w-64 h-64 bg-adsoul-orange rounded-full mix-blend-screen -translate-x-1/3 -translate-y-1/3"></div>
                <div class="absolute bottom-0 right-0 w-96 h-96 bg-adsoul-purple rounded-full mix-blend-screen translate-x-1/3 translate-y-1/3"></div>
                <div class="absolute top-1/4 right-1/4 w-48 h-48 bg-adsoul-light-purple rounded-full mix-blend-screen opacity-50"></div>
            </div>
            <div class="relative z-10 p-6 max-w-4xl mx-auto">
                <h1 class="text-5xl md:text-7xl font-extrabold leading-tight mb-4 hero-title-shadow">AdSoul Marketing</h1>
                <p class="text-2xl md:text-3xl font-light mb-8 hero-slogan-shadow">Publicidad con alma</p>
                <a href="#services" class="btn-primary">
                    Descubre Nuestros Servicios
                </a>
            </div>
        </section>

        <!-- About Us Section -->
        <section id="about" class="py-16 bg-adsoul-light-gray">
            <div class="container mx-auto px-6">
                <h2 class="text-4xl font-bold text-center text-adsoul-purple mb-12">Nosotros</h2>
                <div class="flex flex-col md:flex-row items-center justify-center gap-12">
                    <div class="md:w-1/2 text-lg leading-relaxed space-y-6 text-adsoul-dark-gray">
                        <h3 class="text-3xl font-semibold text-adsoul-orange mb-4">Nuestra Historia</h3>
                        <p>En <strong>AdSoul Marketing</strong>, creemos que cada marca tiene una historia única que contar. Fundada en 2019 en la vibrante ciudad de La Paz, Bolivia, nuestra agencia nació de la visión de la Lic. Andrea Catacora Barrios, una apasionada comunicadora social y experta en publicidad y marketing.</p>
                        <p>Los primeros años fueron de exploración y aprendizaje profundo del mercado boliviano, identificando la necesidad de un enfoque publicitario que no solo generara ventas, sino que también construyera conexiones emocionales y duraderas con las audiencias. En 2021, con la creciente demanda de soluciones digitales, AdSoul Marketing dio un giro significativo, incorporando tecnologías de vanguardia como la inteligencia artificial y la automatización para ofrecer resultados más rápidos y eficientes.</p>
                        <p>Desde entonces, hemos crecido de manera constante, consolidándonos como un referente en La Paz para pequeñas y medianas empresas que buscan una publicidad innovadora, confiable y, sobre todo, con alma.</p>

                        <h3 class="text-3xl font-semibold text-adsoul-orange mb-4 mt-8">Nuestra Filosofía</h3>
                        <p>En AdSoul Marketing, nuestra filosofía se basa en la convicción de que la publicidad debe ir más allá de la simple promoción. Debe inspirar, conectar y dejar una huella significativa. Nos guiamos por tres pilares fundamentales:</p>

                        <h4 class="text-2xl font-semibold text-adsoul-purple mt-6">Visión</h4>
                        <p>Ser la agencia de marketing líder en Bolivia, reconocida por transformar marcas con soluciones publicitarias innovadoras y personalizadas que generen un impacto emocional y un crecimiento sostenible para nuestros clientes.</p>

                        <h4 class="text-2xl font-semibold text-adsoul-purple mt-6">Misión</h4>
                        <p>Empoderar a pequeñas y medianas empresas, especialmente en La Paz, a través de estrategias de marketing digital y tradicional de alta calidad, utilizando tecnología de vanguardia y un enfoque creativo centrado en el alma de cada marca, para que alcancen un reconocimiento y éxito duraderos.</p>

                        <h4 class="text-2xl font-semibold text-adsoul-purple mt-6">Valores</h4>
                        <ul class="list-disc list-inside space-y-2 pl-5">
                            <li><strong>Innovación:</strong> Abrazamos la tecnología y las nuevas ideas para ofrecer soluciones creativas y eficientes.</li>
                            <li><strong>Confianza:</strong> Construimos relaciones transparentes y duraderas con nuestros clientes, basadas en la honestidad y la integridad.</li>
                            <li><strong>Personalización:</strong> Entendemos que cada marca es única, por lo que adaptamos nuestras estrategias a sus necesidades y presupuestos específicos.</li>
                            <li><strong>Pasión:</strong> Ponemos el corazón en cada proyecto, buscando siempre la excelencia y el impacto significativo.</li>
                            <li><strong>Resultados:</strong> Nos enfocamos en generar valor medible y tangible para el crecimiento de nuestros clientes.</li>
                        </ul>
                    </div>
                    <div class="md:w-1/3 flex flex-col items-center">
                        <img src="https://placehold.co/300x300/4B0082/FFFFFF?text=Andrea+Catacora" alt="Lic. Andrea Catacora Barrios" class="rounded-3xl shadow-xl border-4 border-adsoul-orange mb-6 w-48 h-48 object-cover">
                        <h3 class="text-2xl font-semibold text-adsoul-purple">Lic. Andrea Catacora Barrios</h3>
                        <p class="text-adsoul-dark-gray text-center">Fundadora & CEO</p>
                        <p class="text-sm text-adsoul-dark-gray text-center mt-2">Comunicadora Social y Lic. en Publicidad y Marketing</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="py-16 bg-adsoul-light-gray">
            <div class="container mx-auto px-6">
                <h2 class="text-4xl font-bold text-center text-adsoul-purple mb-12">Nuestros Servicios</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Service Card 1: Branding -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-lightbulb"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Branding</h3>
                        <p class="text-adsoul-dark-gray">Creamos la identidad visual y el mensaje de tu marca desde cero, asegurando que resuene con tu audiencia.</p>
                    </div>
                    <!-- Service Card 2: Manejo de Redes Sociales -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-share-alt"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Manejo de Redes Sociales</h3>
                        <p class="text-adsoul-dark-gray">Gestionamos tus perfiles para construir comunidad, aumentar el engagement y potenciar tu presencia online.</p>
                    </div>
                    <!-- Service Card 3: Publicidad Impresa -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-print"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Publicidad Impresa</h3>
                        <p class="text-adsoul-dark-gray">Diseñamos materiales gráficos impactantes: folletos, vallas, revistas y más, para llegar a tu público offline.</p>
                    </div>
                    <!-- Service Card 4: Diseño de Páginas Web -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-globe"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Diseño de Páginas Web</h3>
                        <p class="text-adsoul-dark-gray">Creamos sitios web modernos, responsivos y optimizados para ofrecer la mejor experiencia de usuario.</p>
                    </div>
                    <!-- Service Card 5: Bots de Autorespuesta -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-robot"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Bots de Autorespuesta</h3>
                        <p class="text-adsoul-dark-gray">Implementamos soluciones de IA para automatizar la atención al cliente y mejorar la interacción.</p>
                    </div>
                    <!-- Service Card 6: Producción de Spots y Videos para TikTok -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-video"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Spots y Videos para TikTok</h3>
                        <p class="text-adsoul-dark-gray">Producimos contenido audiovisual creativo y dinámico, ideal para campañas publicitarias y redes sociales.</p>
                    </div>
                    <!-- Service Card 7: Publicidad Digital -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-bullhorn"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Publicidad Digital</h3>
                        <p class="text-adsoul-dark-gray">Estrategias de SEM, display, email marketing y más para maximizar tu alcance y conversiones en línea.</p>
                    </div>
                    <!-- Service Card 8: Publicidad Pagada -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-money-bill-wave"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Publicidad Pagada</h3>
                        <p class="text-adsoul-dark-gray">Gestionamos tus campañas de anuncios en Google, redes sociales y otras plataformas para resultados inmediatos.</p>
                    </div>
                    <!-- Service Card 9: Mascotas Corporativas -->
                    <div class="service-card bg-adsoul-white p-8 rounded-2xl shadow-md flex flex-col items-center text-center">
                        <div class="text-5xl text-adsoul-purple mb-4 service-icon">
                            <i class="fas fa-paw"></i>
                        </div>
                        <h3 class="text-2xl font-semibold text-adsoul-purple mb-3">Mascotas Corporativas</h3>
                        <p class="text-adsoul-dark-gray">Diseñamos y damos vida a personajes únicos que representen la personalidad y los valores de tu marca.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Why Choose Us Section -->
        <section id="why-choose-us" class="py-16 section-gradient-purple text-adsoul-white">
            <div class="container mx-auto px-6">
                <h2 class="text-4xl font-bold text-center mb-12">¿Por Qué Elegirnos?</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Feature 1: Tecnología e IA -->
                    <div class="bg-adsoul-orange p-8 rounded-2xl shadow-md text-center">
                        <div class="text-5xl mb-4"><i class="fas fa-microchip"></i></div>
                        <h3 class="text-2xl font-semibold mb-3">Tecnología e IA</h3>
                        <p>Somos amantes de la tecnología. Utilizamos inteligencia artificial para optimizar tus campañas y ofrecer resultados superiores.</p>
                    </div>
                    <!-- Feature 2: Rapidez en la Entrega -->
                    <div class="bg-adsoul-orange p-8 rounded-2xl shadow-md text-center">
                        <div class="text-5xl mb-4"><i class="fas fa-tachometer-alt"></i></div>
                        <h3 class="text-2xl font-semibold mb-3">Rapidez en la Entrega</h3>
                        <p>Entendemos la importancia del tiempo. Garantizamos agilidad y eficiencia en la entrega de todos nuestros proyectos.</p>
                    </div>
                    <!-- Feature 3: Productos Personalizados -->
                    <div class="bg-adsoul-orange p-8 rounded-2xl shadow-md text-center">
                        <div class="text-5xl mb-4"><i class="fas fa-hand-h
