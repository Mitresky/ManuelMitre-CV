<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV Interactivo - Manuel Mitre</title>
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
            transition: background-color 0.3s;
        }
        .timeline-item.active {
            background-color: #e9ecef;
        }
        .progress-bar-fill {
            transition: width 1.5s ease-in-out;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            height: 400px;
            max-height: 50vh;
        }
    </style>
</head>
<body class="antialiased">

    <header class="bg-white/80 backdrop-blur-md shadow-sm sticky top-0 z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <h1 class="text-xl font-bold text-gray-800">Manuel Mitre</h1>
            <div class="hidden md:flex space-x-8">
                <a href="#perfil" class="nav-link font-medium text-gray-600 pb-1">Perfil</a>
                <a href="#trayectoria" class="nav-link font-medium text-gray-600 pb-1">Trayectoria</a>
                <a href="#habilidades" class="nav-link font-medium text-gray-600 pb-1">Habilidades</a>
                <a href="#educacion" class="nav-link font-medium text-gray-600 pb-1">Educación</a>
            </div>
            <a href="https://www.linkedin.com/in/mitreortiz/" target="_blank" class="hidden md:inline-block bg-blue-600 text-white font-bold py-2 px-4 rounded-lg hover:bg-blue-700 transition-colors">
                LinkedIn
            </a>
        </nav>
    </header>

    <main class="container mx-auto px-6 py-12">

        <section id="perfil" class="text-center mb-24">
            <h2 class="text-5xl font-bold mb-4">Lic. en Negocio y Comercio Internacional</h2>
            <p class="max-w-3xl mx-auto text-lg text-gray-600">
                Profesional dinámico y orientado a resultados con sólida experiencia en operaciones, coordinación comercial y administración. Especializado en optimización de procesos logísticos y análisis de datos para la toma de decisiones estratégicas. Busco activamente contribuir al crecimiento y eficiencia operativa de organizaciones dinámicas.
            </p>
        </section>

        <section id="trayectoria" class="mb-24">
            <h3 class="text-3xl font-bold text-center mb-2">Trayectoria Profesional</h3>
            <p class="text-center text-gray-500 mb-12">Haz clic en cada puesto para ver los detalles y logros clave.</p>
            <div class="md:grid md:grid-cols-3 md:gap-12">
                <div class="col-span-1 mb-8 md:mb-0">
                    <div class="space-y-4">
                        <div id="job-coppel" class="timeline-item p-4 rounded-lg border border-gray-200 active">
                            <p class="font-bold text-lg">Analista de Operaciones</p>
                            <p class="text-sm text-gray-600">Coppel | 2022 - Actualmente</p>
                        </div>
                        <div id="job-galbo" class="timeline-item p-4 rounded-lg border border-gray-200">
                            <p class="font-bold text-lg">Coordinador Comercial</p>
                            <p class="text-sm text-gray-600">Galbo | 2021</p>
                        </div>
                        <div id="job-hsbc" class="timeline-item p-4 rounded-lg border border-gray-200">
                            <p class="font-bold text-lg">Ejecutivo de Cuentas</p>
                            <p class="text-sm text-gray-600">HSBC | 2019 - 2021</p>
                        </div>
                        <div id="job-uas" class="timeline-item p-4 rounded-lg border border-gray-200">
                            <p class="font-bold text-lg">Secretario Administrativo</p>
                            <p class="text-sm text-gray-600">UAS | 2014 - 2019</p>
                        </div>
                    </div>
                </div>
                <div class="col-span-2">
                    <div id="details-coppel" class="job-details bg-white p-6 rounded-xl shadow-md">
                        <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en Coppel</h4>
                        <ul class="space-y-4">
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Liderar la optimización de procesos logísticos, garantizando entregas puntuales y eficientes.</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Identificar tendencias, patrones y anomalías clave mediante el análisis de datos (SQL, Vs Code, Dashboard) para fundamentar decisiones estratégicas.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Colaborar estrechamente con Última Milla para la toma de decisiones basadas en datos.</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Gestionar proactivamente indemnizaciones y penalizaciones por incumplimiento de KPIs.</span>
                            </li>
                        </ul>
                    </div>
                    <div id="details-galbo" class="job-details hidden bg-white p-6 rounded-xl shadow-md">
                        <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en Galbo</h4>
                         <ul class="space-y-4">
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Administrar y dirigir el departamento comercial, diseñando un plan de comunicación externa para cumplir los KPIs.</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Identificar oportunidades estratégicas de mercado para maximizar resultados de ventas.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Coordinar y negociar exitosamente los términos para la contratación de servicios.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Establecer y mantener sólidas relaciones públicas para fortalecer la imagen de la empresa.</span>
                            </li>
                        </ul>
                    </div>
                    <div id="details-hsbc" class="job-details hidden bg-white p-6 rounded-xl shadow-md">
                        <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en HSBC</h4>
                        <ul class="space-y-4">
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Gestionar y hacer crecer una cartera de clientes, aumentando la satisfacción.</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Resolver problemas complejos para mejorar la retención de clientes.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Identificar y mitigar potenciales riesgos crediticios, protegiendo los activos del banco.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Superar metas de venta de productos y servicios financieros de manera proactiva.</span>
                            </li>
                        </ul>
                    </div>
                     <div id="details-uas" class="job-details hidden bg-white p-6 rounded-xl shadow-md">
                        <h4 class="text-2xl font-bold mb-4">Logros y Responsabilidades en la UAS</h4>
                        <ul class="space-y-4">
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Gestionar integralmente el ciclo de facturación, optimizando el proceso.</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Administrar compras internas logrando ahorros a través de negociaciones efectivas.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Coordinar y supervisar al personal administrativo para mejorar la productividad del equipo.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 font-bold mr-3">✓</span>
                                <span>Gestionar la relación con proveedores y coordinar la adquisición de suministros.</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section id="habilidades" class="mb-24">
            <h3 class="text-3xl font-bold text-center mb-12">Habilidades Clave</h3>
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <h4 class="font-bold text-xl mb-6 text-center">Competencias Profesionales</h4>
                    <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 text-center">
                        <div class="bg-white p-4 rounded-lg shadow-sm"><p>Adaptabilidad</p></div>
                        <div class="bg-white p-4 rounded-lg shadow-sm"><p>Liderazgo</p></div>
                        <div class="bg-white p-4 rounded-lg shadow-sm"><p>Desarrollo de Negocios</p></div>
                        <div class="bg-white p-4 rounded-lg shadow-sm"><p>Negociación Avanzada</p></div>
                        <div class="bg-white p-4 rounded-lg shadow-sm"><p>Gestión de Proyectos</p></div>
                        <div class="bg-white p-4 rounded-lg shadow-sm"><p>Optimización de Procesos</p></div>
                    </div>
                </div>
                <div>
                     <div class="chart-container">
                        <canvas id="skillsChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

        <section id="educacion" class="mb-16">
            <h3 class="text-3xl font-bold text-center mb-12">Educación y Certificaciones</h3>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <h4 class="text-2xl font-bold mb-4">Formación Académica</h4>
                    <div class="space-y-4">
                        <div>
                            <p class="font-bold">Maestría en Dirección de Negocios</p>
                            <p class="text-sm text-gray-600">Universidad México Internacional | 2024 - Actualmente</p>
                        </div>
                        <div>
                            <p class="font-bold">Lic. en Negocio y Comercio Internacional</p>
                            <p class="text-sm text-gray-600">Universidad Autónoma de Sinaloa | 2012 - 2016</p>
                        </div>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md">
                     <h4 class="text-2xl font-bold mb-4">Cursos Relevantes</h4>
                     <ul class="space-y-2">
                        <li class="flex items-center"><span class="text-blue-500 mr-2">◆</span>Diplomado en Formación ASG</li>
                        <li class="flex items-center"><span class="text-blue-500 mr-2">◆</span>Certificación en Materia de PLD/FT</li>
                        <li class="flex items-center"><span class="text-blue-500 mr-2">◆</span>15 Leyes Indispensables del Liderazgo</li>
                        <li class="flex items-center"><span class="text-blue-500 mr-2">◆</span>Educación Financiera (Condusef)</li>
                     </ul>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-gray-800 text-white">
        <div class="container mx-auto px-6 py-8 text-center">
             <h3 class="text-2xl font-bold mb-4">Contacto</h3>
             <p class="mb-2">Email: mitreorliz@omall.com</p>
             <p class="mb-4">Teléfono: 6672-20-55-17</p>
             <a href="https://www.linkedin.com/in/mitreortiz/" target="_blank" class="bg-blue-600 text-white font-bold py-3 px-6 rounded-lg hover:bg-blue-700 transition-colors">
                Ver Perfil en LinkedIn
            </a>
        </div>
    </footer>


    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Timeline interaction
            const timelineItems = document.querySelectorAll('.timeline-item');
            const jobDetails = document.querySelectorAll('.job-details');

            timelineItems.forEach(item => {
                item.addEventListener('click', () => {
                    const targetId = 'details-' + item.id.split('-')[1];
                    
                    // Update active state for timeline items
                    timelineItems.forEach(i => i.classList.remove('active'));
                    item.classList.add('active');

                    // Show/hide job details
                    jobDetails.forEach(detail => {
                        if (detail.id === targetId) {
                            detail.classList.remove('hidden');
                        } else {
                            detail.classList.add('hidden');
                        }
                    });
                });
            });

            // Navigation active state on scroll
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-link');

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        navLinks.forEach(link => {
                            const href = link.getAttribute('href').substring(1);
                            link.classList.toggle('active', href === entry.target.id);
                        });
                    }
                });
            }, { rootMargin: '-50% 0px -50% 0px' });

            sections.forEach(section => {
                observer.observe(section);
            });


            // Skills Chart
            const ctx = document.getElementById('skillsChart').getContext('2d');
            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Análisis de Datos (SQL, Vs Code)', 'Liderazgo de Equipos', 'Optimización Logística', 'Negociación Avanzada', 'Planificación Estratégica', 'Gestión Financiera'],
                    datasets: [{
                        label: 'Nivel de Competencia',
                        data: [90, 85, 95, 88, 80, 82],
                        backgroundColor: 'rgba(0, 123, 255, 0.6)',
                        borderColor: 'rgba(0, 123, 255, 1)',
                        borderWidth: 1
                    }]
                },
                options: {
                    indexAxis: 'y',
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return context.raw + '% de dominio';
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            beginAtZero: true,
                            max: 100,
                            ticks: {
                                callback: function(value) {
                                    return value + '%'
                                }
                            }
                        },
                        y: {
                           ticks: {
                                autoSkip: false,
                                callback: function(value, index, values) {
                                    const label = this.getLabelForValue(value);
                                    if (label.length > 25) {
                                        return label.substring(0, 25) + '...';
                                    }
                                    return label;
                                }
                            }
                        }
                    }
                }
            });
        });
    </script>
</body>
</html>
