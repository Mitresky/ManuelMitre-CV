<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV Interactivo - Manuel Mitre</title>
    <!-- Visualization & Content Choices: 
        - Trayectoria: Report Info (Job History) -> Goal (Show Progression & Detail) -> Viz (Interactive vertical timeline/tabs) -> Interaction (Click to reveal details) -> Justification (Reduces clutter, focuses user attention, encourages engagement) -> Library/Method (HTML/CSS/JS).
        - Habilidades: Report Info (Skill list) -> Goal (Compare & Categorize) -> Viz (Horizontal Bar Chart for proficiency, Tags for competencies) -> Interaction (Chart animation, tooltips on hover) -> Justification (Bar chart is ideal for comparison, tags are scannable) -> Library/Method (Chart.js, HTML/CSS).
        - Educación: Report Info (Degrees, Courses) -> Goal (Inform Clearly) -> Viz (Two-column card layout) -> Interaction (None) -> Justification (Simple, clean, and effective for static data) -> Library/Method (HTML/CSS).
    -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F8F9FA;
            color: #212529;
        }
        .nav-link {
            transition: color 0.3s, border-bottom-color 0.3s;
            border-bottom: 2px solid transparent;
        }
        .nav-link:hover, .nav-link.active {
            color: #007BFF;
            border-bottom-color: #007BFF;
        }
        .timeline-item {
            cursor: pointer;
            transition: background-color 0.3s, border-color 0.3s, transform 0.2s;
        }
        .timeline-item:hover {
            transform: translateY(-2px);
            border-color: #007BFF;
        }
        .timeline-item.active {
            background-color: #e9ecef;
            border-color: #007BFF;
            font-weight: 600;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 45vh;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        .job-details {
            transition: opacity 0.5s ease-in-out;
        }
    </style>
</head>
<body class="antialiased">

    <header class="bg-white/80 backdrop-blur-md shadow-sm sticky top-0 z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-xl font-bold text-gray-800">Manuel Mitre</a>
            <div class="hidden md:flex space-x-8">
                <a href="#perfil" class="nav-link font-medium text-gray-600 pb-1">Perfil</a>
                <a href="#trayectoria" class="nav-link font-medium text-gray-600 pb-1">Trayectoria</a>
                <a href="#habilidades" class="nav-link font-medium text-gray-600 pb-1">Habilidades</a>
                <a href="#educacion" class="nav-link font-medium text-gray-600 pb-1">Educación</a>
            </div>
            <a href="https://www.linkedin.com/in/mitreortiz/" target="_blank" class="hidden md:inline-block bg-blue-600 text-white font-bold py-2 px-4 rounded-lg hover:bg-blue-700 transition-colors">
                LinkedIn
            </a>
            <button id="mobile-menu-button" class="md:hidden text-gray-700 focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
            </button>
        </nav>
        <div id="mobile-menu" class="hidden md:hidden px-6 pt-2 pb-4 space-y-2">
            <a href="#perfil" class="block nav-link font-medium text-gray-600">Perfil</a>
            <a href="#trayectoria" class="block nav-link font-medium text-gray-600">Trayectoria</a>
            <a href="#habilidades" class="block nav-link font-medium text-gray-600">Habilidades</a>
            <a href="#educacion" class="block nav-link font-medium text-gray-600">Educación</a>
            <a href="https://www.linkedin.com/in/mitreortiz/" target="_blank" class="block w-full text-center mt-2 bg-blue-600 text-white font-bold py-2 px-4 rounded-lg hover:bg-blue-700 transition-colors">
                LinkedIn
            </a>
        </div>
    </header>

    <main class="container mx-auto px-6 py-12">

        <section id="perfil" class="text-center py-16 md:py-24">
            <h2 class="text-4xl md:text-5xl font-bold mb-4 text-gray-900">Lic. en Negocio y Comercio Internacional</h2>
            <p class="max-w-3xl mx-auto text-lg text-gray-600">
                Esta sección introduce mi perfil profesional. Soy un profesional dinámico y orientado a resultados con sólida experiencia en operaciones, coordinación comercial y administración. Me especializo en la optimización de procesos logísticos y el análisis de datos para la toma de decisiones estratégicas, buscando siempre contribuir al crecimiento y la eficiencia de las organizaciones.
            </p>
        </section>

        <section id="trayectoria" class="py-16 md:py-24">
            <div class="text-center mb-12">
                <h3 class="text-3xl font-bold mb-2">Trayectoria Profesional</h3>
                <p class="text-gray-600 max-w-2xl mx-auto">Aquí puedes explorar mi carrera de forma interactiva. Mi experiencia abarca desde la administración y las finanzas hasta la coordinación comercial y, más recientemente, el análisis de operaciones. Haz clic en cada puesto en la línea de tiempo para ver los detalles, responsabilidades y logros clave en cada etapa.</p>
            </div>
            <div class="md:grid md:grid-cols-3 md:gap-12">
                <div class="col-span-1 mb-8 md:mb-0">
                    <div class="space-y-4">
                        <div id="job-coppel" class="timeline-item p-4 rounded-lg border-2 border-transparent active">
                            <p class="font-bold text-lg">Analista de Operaciones</p>
                            <p class="text-sm text-gray-600">Coppel | 2022 - Actualmente</p>
                        </div>
                        <div id="job-galbo" class="timeline-item p-4 rounded-lg border-2 border-transparent">
                            <p class="font-bold text-lg">Coordinador Comercial</p>
                            <p class="text-sm text-gray-600">Galbo | 2021</p>
                        </div>
                        <div id="job-hsbc" class="timeline-item p-4 rounded-lg border-2 border-transparent">
                            <p class="font-bold text-lg">Ejecutivo de Cuentas</p>
                            <p class="text-sm text-gray-600">HSBC | 2019 - 2021</p>
                        </div>
                        <div id="job-uas" class="timeline-item p-4 rounded-lg border-2 border-transparent">
                            <p class="font-bold text-lg">Secretario Administrativo</p>
                            <p class="text-sm text-gray-600">UAS | 2014 - 2019</p>
                        </div>
                    </div>
                </div>
                <div class="col-span-2">
                    <div id="details-container" class="relative">
                        <div id="details-coppel" class="job-details bg-white p-8 rounded-xl shadow-lg">
                            <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en Coppel</h4>
                            <ul class="space-y-3 list-inside">
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Liderar la optimización de procesos logísticos, garantizando entregas puntuales y eficientes.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Identificar tendencias y patrones mediante el análisis de datos (SQL, Vs Code, Dashboard) para fundamentar decisiones estratégicas.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Colaborar estrechamente con Última Milla para la toma de decisiones basadas en datos.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Gestionar proactivamente indemnizaciones y penalizaciones por incumplimiento de KPIs.</span></li>
                            </ul>
                        </div>
                        <div id="details-galbo" class="job-details hidden absolute top-0 left-0 w-full bg-white p-8 rounded-xl shadow-lg opacity-0">
                            <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en Galbo</h4>
                            <ul class="space-y-3 list-inside">
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Administrar el departamento comercial, diseñando un plan de comunicación externa para cumplir los KPIs.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Identificar oportunidades estratégicas de mercado para maximizar resultados de ventas.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Coordinar y negociar exitosamente los términos para la contratación de servicios.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Establecer y mantener sólidas relaciones públicas para fortalecer la imagen de la empresa.</span></li>
                            </ul>
                        </div>
                        <div id="details-hsbc" class="job-details hidden absolute top-0 left-0 w-full bg-white p-8 rounded-xl shadow-lg opacity-0">
                           <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en HSBC</h4>
                            <ul class="space-y-3 list-inside">
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Gestionar y hacer crecer una cartera de clientes, aumentando la satisfacción.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Resolver problemas complejos para mejorar la retención de clientes.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Identificar y mitigar potenciales riesgos crediticios, protegiendo los activos del banco.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Superar metas de venta de productos y servicios financieros de manera proactiva.</span></li>
                            </ul>
                        </div>
                         <div id="details-uas" class="job-details hidden absolute top-0 left-0 w-full bg-white p-8 rounded-xl shadow-lg opacity-0">
                            <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en la UAS</h4>
                            <ul class="space-y-3 list-inside">
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Gestionar integralmente el ciclo de facturación, optimizando el proceso.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Administrar compras internas logrando ahorros a través de negociaciones efectivas.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Coordinar y supervisar al personal administrativo para mejorar la productividad del equipo.</span></li>
                                <li class="flex items-start"><span class="text-blue-500 font-bold mr-3 mt-1">&#10003;</span><span>Gestionar la relación con proveedores y coordinar la adquisición de suministros.</span></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="habilidades" class="bg-white py-16 md:py-24 rounded-2xl">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h3 class="text-3xl font-bold mb-2">Habilidades Clave</h3>
                    <p class="text-gray-600 max-w-2xl mx-auto">Esta sección visualiza mis competencias. A la izquierda, se presentan mis habilidades profesionales clave, que fundamentan mi enfoque estratégico. A la derecha, un gráfico de barras interactivo muestra mi nivel de dominio en herramientas y áreas técnicas específicas. Pasa el cursor sobre las barras para ver más detalles.</p>
                </div>
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div class="flex flex-col items-center">
                        <h4 class="font-bold text-xl mb-6 text-center text-gray-800">Competencias Profesionales</h4>
                        <div class="grid grid-cols-2 gap-4 text-center max-w-md">
                            <div class="bg-gray-100 p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow"><p>Adaptabilidad</p></div>
                            <div class="bg-gray-100 p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow"><p>Liderazgo</p></div>
                            <div class="bg-gray-100 p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow"><p>Desarrollo de Negocios</p></div>
                            <div class="bg-gray-100 p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow"><p>Negociación Avanzada</p></div>
                            <div class="bg-gray-100 p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow"><p>Gestión de Proyectos</p></div>
                            <div class="bg-gray-100 p-4 rounded-lg shadow-sm hover:shadow-md transition-shadow"><p>Optimización de Procesos</p></div>
                        </div>
                    </div>
                    <div>
                         <div class="chart-container">
                            <canvas id="skillsChart"></canvas>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="educacion" class="py-16 md:py-24">
            <div class="text-center mb-12">
                <h3 class="text-3xl font-bold mb-2">Educación y Certificaciones</h3>
                <p class="text-gray-600 max-w-2xl mx-auto">Mi base académica y mi compromiso con el aprendizaje continuo son pilares de mi desarrollo. A continuación se detalla mi formación universitaria y los cursos y certificaciones más relevantes que he completado para mantenerme actualizado en áreas estratégicas como finanzas, liderazgo y ASG.</p>
            </div>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow">
                    <h4 class="text-2xl font-bold mb-4">Formación Académica</h4>
                    <div class="space-y-4">
                        <div>
                            <p class="font-bold text-lg">Maestría en Dirección de Negocios</p>
                            <p class="text-gray-600">Universidad México Internacional | 2024 - Actualmente</p>
                        </div>
                        <div>
                            <p class="font-bold text-lg">Lic. en Negocio y Comercio Internacional</p>
                            <p class="text-gray-600">Universidad Autónoma de Sinaloa | 2012 - 2016</p>
                        </div>
                    </div>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow">
                     <h4 class="text-2xl font-bold mb-4">Cursos y Certificaciones</h4>
                     <ul class="space-y-3">
                        <li class="flex items-center"><span class="text-blue-500 mr-3">&#9670;</span>Diplomado en Formación ASG</li>
                        <li class="flex items-center"><span class="text-blue-500 mr-3">&#9670;</span>Certificación en Materia de PLD/FT</li>
                        <li class="flex items-center"><span class="text-blue-500 mr-3">&#9670;</span>15 Leyes Indispensables del Liderazgo</li>
                        <li class="flex items-center"><span class="text-blue-500 mr-3">&#9670;</span>Educación Financiera (Condusef)</li>
                     </ul>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-gray-800 text-white">
        <div class="container mx-auto px-6 py-12 text-center">
             <h3 class="text-2xl font-bold mb-4">Contacto</h3>
             <p class="mb-2 text-gray-300">Email: <a href="mailto:mitreorliz@omall.com" class="hover:text-blue-400">mitreorliz@omall.com</a></p>
             <p class="mb-6 text-gray-300">Teléfono: 667-220-5517</p>
             <a href="https://www.linkedin.com/in/mitreortiz/" target="_blank" class="bg-blue-600 text-white font-bold py-3 px-6 rounded-lg hover:bg-blue-700 transition-all duration-300 transform hover:scale-105">
                Conectar en LinkedIn
            </a>
        </div>
    </footer>


    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Mobile menu toggle
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });

            // Timeline interaction
            const timelineItems = document.querySelectorAll('.timeline-item');
            const jobDetailsContainer = document.getElementById('details-container');
            const jobDetails = document.querySelectorAll('.job-details');

            timelineItems.forEach(item => {
                item.addEventListener('click', () => {
                    const targetId = 'details-' + item.id.split('-')[1];
                    
                    timelineItems.forEach(i => i.classList.remove('active'));
                    item.classList.add('active');

                    let activeDetail = null;
                    jobDetails.forEach(detail => {
                        if (detail.id === targetId) {
                            activeDetail = detail;
                        } else {
                            detail.classList.add('hidden', 'opacity-0');
                            detail.classList.remove('relative');
                            detail.classList.add('absolute');
                        }
                    });
                    
                    if(activeDetail) {
                        activeDetail.classList.remove('hidden', 'opacity-0');
                        activeDetail.classList.add('relative');
                        activeDetail.classList.remove('absolute');
                    }
                });
            });

            // Navigation active state on scroll
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-link');
            
            const observerOptions = {
                root: null,
                rootMargin: '0px',
                threshold: 0.5
            };

            const observer = new IntersectionObserver((entries) => {
                let activeSectionId = '';
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        activeSectionId = entry.target.id;
                    }
                });
                
                navLinks.forEach(link => {
                    const href = link.getAttribute('href');
                    if (href === `#${activeSectionId}`) {
                        link.classList.add('active');
                    } else {
                        link.classList.remove('active');
                    }
                });
            }, observerOptions);

            sections.forEach(section => {
                observer.observe(section);
            });

            // Skills Chart
            const skillsChartCanvas = document.getElementById('skillsChart');
            let skillsChart;
            const skillsChartData = {
                labels: ['Análisis de Datos (SQL, Vs Code)', 'Liderazgo de Equipos', 'Optimización Logística', 'Negociación Avanzada', 'Planificación Estratégica', 'Gestión Financiera'],
                datasets: [{
                    label: 'Nivel de Competencia',
                    data: [90, 85, 95, 88, 80, 82],
                    backgroundColor: 'rgba(0, 123, 255, 0.6)',
                    borderColor: 'rgba(0, 123, 255, 1)',
                    borderWidth: 1,
                    borderRadius: 4
                }]
            };
            const skillsChartConfig = {
                type: 'bar',
                data: skillsChartData,
                options: {
                    indexAxis: 'y',
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: { display: false },
                        tooltip: {
                            backgroundColor: '#212529',
                            titleFont: { size: 14, weight: 'bold' },
                            bodyFont: { size: 12 },
                            callbacks: {
                                label: context => `${context.dataset.label}: ${context.raw}%`
                            }
                        }
                    },
                    scales: {
                        x: {
                            beginAtZero: true,
                            max: 100,
                            grid: { drawOnChartArea: false },
                            ticks: { callback: value => value + '%' }
                        },
                        y: {
                            grid: { display: false }
                        }
                    },
                    animation: {
                        duration: 1500,
                        easing: 'easeInOutQuart'
                    }
                }
            };

            const chartObserver = new IntersectionObserver((entries) => {
                if (entries[0].isIntersecting) {
                    if (skillsChart) skillsChart.destroy();
                    skillsChart = new Chart(skillsChartCanvas.getContext('2d'), skillsChartConfig);
                    chartObserver.unobserve(skillsChartCanvas);
                }
            }, { threshold: 0.5 });
            
            chartObserver.observe(skillsChartCanvas);
        });
    </script>
</body>
</html>
