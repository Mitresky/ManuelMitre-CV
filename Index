<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infografía: Plan de Rescate MITRECONECT</title>
    <base href="/"> 
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F3F4F6;
            color: #1F2937;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .timeline-line {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            top: 20px;
            bottom: 20px;
            width: 4px;
            background-color: #A9D0DE;
            border-radius: 2px;
        }
        .timeline-item {
            position: relative;
            width: 100%;
            padding-left: 0;
            padding-right: 0;
            margin-bottom: 50px;
        }
        .timeline-content {
            position: relative;
            width: calc(50% - 40px);
            background: white;
            border-radius: 0.5rem;
            padding: 1.5rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            border-top: 4px solid #4771B2;
        }
        .timeline-item:nth-child(odd) .timeline-content {
            float: left;
            text-align: right;
        }
        .timeline-item:nth-child(even) .timeline-content {
            float: right;
            text-align: left;
        }
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: white;
            border: 4px solid #00429D;
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1;
        }
        .timeline-item::before {
            content: "";
            display: table;
            clear: both;
        }
    </style>
</head>
<body class="bg-gray-100">

    <div class="container mx-auto p-4 md:p-8 max-w-7xl">

        <header class="text-center mb-12">
            <h1 class="text-4xl md:text-6xl font-extrabold text-[#00429D]">🛡️ RESCATE DE LA CONFIANZA EN MITRECONECT</h1>
            <p class="text-xl md:text-2xl font-semibold text-gray-700 mt-4">Plan de Acción de Gobierno Corporativo ante Fraude Reputacional</p>
            <p class="max-w-3xl mx-auto text-gray-600 mt-4">
                Esta es una aplicación interactiva que detalla el plan de respuesta de MITRECONECT para abordar las denuncias de fraude,
                reestructurar la gobernanza y restaurar la confianza de los empleados e inversores a través de acciones decisivas.
            </p>
        </header>

        <main>
            <!-- SECCIÓN 1: ACCIÓN INMEDIATA -->
            <section class="mb-16">
                <h2 class="text-3xl font-bold text-center mb-8">🚨 1. PUNTO DE CONTROL INMEDIATO (Respuesta 1.a)</h2>
                <p class="text-center text-gray-600 max-w-3xl mx-auto mb-10">
                    Ante la crisis, se requiere una acción inmediata para detener el daño financiero y moral. Estas dos acciones
                    prioritarias se ejecutan simultáneamente para estabilizar la situación y comenzar la investigación.
                </p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <!-- Tarjeta de Acción 1 -->
                    <div class="bg-white p-6 rounded-lg shadow-lg transform transition duration-300 hover:scale-105">
                        <div class="text-6xl mb-4">💵</div>
                        <h3 class="text-2xl font-bold text-[#00429D] mb-3">PAGO INMEDIATO Y CONGELACIÓN DE BONOS</h3>
                        <p class="text-gray-700 mb-4">Utilizar la solvencia real para liquidar *inmediatamente* los sueldos atrasados. Suspender cualquier bono o incentivo variable de la Alta Dirección.</p>
                        <div class="bg-gray-50 p-4 rounded-md border-l-4 border-gray-300">
                            <h4 class="font-semibold text-gray-800">Justificación (Deber Fiduciario)</h4>
                            <p class="text-sm text-gray-600">Demuestra compromiso con el empleado y detiene el posible desvío de recursos mientras se investiga.</p>
                        </div>
                    </div>
                    <!-- Tarjeta de Acción 2 -->
                    <div class="bg-white p-6 rounded-lg shadow-lg transform transition duration-300 hover:scale-105">
                        <div class="text-6xl mb-4">🔍</div>
                        <h3 class="text-2xl font-bold text-[#00429D] mb-3">AUDITORÍA FORENSE EXPRESS</h3>
                        <p class="text-gray-700 mb-4">Contratación urgente de un auditor externo enfocado en las cuentas por pagar, nóminas y gastos operativos para identificar el desvío.</p>
                        <div class="bg-gray-50 p-4 rounded-md border-l-4 border-gray-300">
                            <h4 class="font-semibold text-gray-800">Justificación (Objetividad)</h4>
                            <p class="text-sm text-gray-600">Asegura la objetividad y rapidez en el diagnóstico del problema real, aislando a los responsables.</p>
                        </div>
                    </div>
                </div>

                <!-- Visualización Clave 1.a -->
                <div class="mt-12 bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4">Visualización Clave: Focos de Auditoría (Datos Hipotéticos)</h3>
                    <p class="text-center text-gray-600 max-w-3xl mx-auto mb-6">
                        El gráfico de dona ilustra las áreas de mayor riesgo donde se centrará la auditoría forense.
                        Basado en casos similares, los gastos operativos inflados son frecuentemente la principal fuente de fraude.
                    </p>
                    <div class="chart-container">
                        <canvas id="auditChart"></canvas>
                    </div>
                </div>
            </section>
            
            <!-- SECCIÓN 2: HOJA DE RUTA DE LA REFORMA -->
            <section class="mb-16">
                <h2 class="text-3xl font-bold text-center mb-12 mt-16">🛣️ 2. PLAN DE REVISIÓN Y REFORMA ESTRUCTURAL (Respuesta 1.b)</h2>
                <p class="text-center text-gray-600 max-w-3xl mx-auto mb-10">
                    Una vez controlada la crisis inmediata, se implementa una hoja de ruta para reestructurar el Gobierno Corporativo
                    y asegurar que los principios éticos se integren en la toma de decisiones.
                </p>
                <div class="relative max-w-4xl mx-auto">
                    <div class="timeline-line hidden md:block"></div>
                    
                    <!-- Fase I -->
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <span class="text-sm font-semibold text-[#00429D] bg-[#A9D0DE] px-3 py-1 rounded-full">Corto Plazo (0-30 Días)</span>
                            <h3 class="text-xl font-bold my-2">Fase I: Transparencia y Ética</h3>
                            <p class="text-gray-700">Comunicación formal del propietario protegiendo a los **denunciantes** y confirmando la solvencia de la empresa para tranquilizar a los empleados.</p>
                        </div>
                    </div>
                    <!-- Fase II -->
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <span class="text-sm font-semibold text-[#00429D] bg-[#A9D0DE] px-3 py-1 rounded-full">Mediano Plazo (30-180 Días)</span>
                            <h3 class="text-xl font-bold my-2">Fase II: Independencia y Equidad</h3>
                            <p class="text-gray-700">Reestructurar el **Consejo de Administración** para que la mayoría de sus miembros sean **Consejeros Independientes** y no tengan conflictos de interés.</p>
                        </div>
                    </div>
                    <!-- Fase III -->
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <span class="text-sm font-semibold text-[#00429D] bg-[#A9D0DE] px-3 py-1 rounded-full">Mediano Plazo (30-180 Días)</span>
                            <h3 class="text-xl font-bold my-2">Fase III: Control y Responsabilidad</h3>
                            <p class="text-gray-700">Implementar un **Comité de Ética y Auditoría** compuesto *exclusivamente* por los nuevos Consejeros Independientes, dándoles autoridad total de supervisión.</p>
                        </div>
                    </div>

                </div>

                <!-- Visualización Clave 1.b -->
                <div class="mt-12 bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4">Visualización Clave: Reforma del Consejo (Antes vs. Después)</h3>
                    <p class="text-center text-gray-600 max-w-3xl mx-auto mb-6">
                        Este gráfico de barras compara la composición del Consejo de Administración antes y después de la reforma.
                        El cambio clave es la drástica reducción de consejeros ejecutivos y relacionados, en favor de una mayoría
                        independiente, lo cual es fundamental para un buen Gobierno Corporativo.
                    </p>
                    <div class="chart-container">
                        <canvas id="boardChart"></canvas>
                    </div>
                </div>
            </section>

            <!-- SECCIÓN 3: VIGILANCIA PERMANENTE -->
            <section class="mb-16">
                <h2 class="text-3xl font-bold text-center mb-12 mt-16">🛰️ 3. MECANISMO DE VIGILANCIA PERMANENTE (Respuesta 1.c)</h2>
                <p class="text-center text-gray-600 max-w-3xl mx-auto mb-10">
                    Para prevenir futuras crisis, se establece un sistema de "Doble Vigilancia" que combina el control humano (social)
                    con el control tecnológico (digital), creando una defensa robusta contra el fraude.
                </p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <!-- Tarjeta Vigilancia 1 -->
                    <div class="bg-white p-6 rounded-lg shadow-lg">
                        <div class="text-6xl mb-4">📣</div>
                        <h3 class="text-2xl font-bold text-[#00429D] mb-3">CONTROL SOCIAL (Whistleblowing)</h3>
                        <p class="text-gray-700">Implementación de una **Línea Ética Externa Anónima**, gestionada por un tercero independiente, para que cualquier empleado pueda reportar anomalías sin miedo a represalias.</p>
                    </div>
                    <!-- Tarjeta Vigilancia 2 -->
                    <div class="bg-white p-6 rounded-lg shadow-lg">
                        <div class="text-6xl mb-4">🚚</div>
                        <h3 class="text-2xl font-bold text-[#00429D] mb-3">CONTROL DIGITAL (Logística)</h3>
                        <p class="text-gray-700">**Auditoría Cruzada de Datos:** Vincular el sistema de flotas (TMS) con el contable para **contrastar automáticamente** gastos (ej. combustible, kilometraje) contra la actividad real de las unidades.</p>
                    </div>
                </div>

                <div class="mt-8 bg-white p-6 rounded-lg shadow-lg border-t-4 border-[#F97316]">
                    <h3 class="text-2xl font-bold text-[#00429D] mb-3 text-center">Justificación de la Doble Vigilancia</h3>
                    <p class="text-gray-700 text-center text-lg max-w-3xl mx-auto">
                        La combinación de ambos es la mejor defensa: la **vigilancia social** detecta la falta de ética,
                        mientras que el **control digital** previene la manipulación de datos financieros basados en operaciones logísticas falsas.
                    </p>
                </div>

                <!-- Visualización Clave 1.c -->
                <div class="mt-12 bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4">Visualización Clave: Impacto Proyectado de la Vigilancia</h3>
                    <p class="text-center text-gray-600 max-w-3xl mx-auto mb-6">
                        Este gráfico de líneas proyecta cómo la implementación de la línea ética (aumentando los reportes procesados)
                        impactará directamente en la reducción de las pérdidas financieras por fraude, demostrando el retorno de la inversión (ROI) de la transparencia.
                    </p>
                    <div class="chart-container">
                        <canvas id="vigilanceChart"></canvas>
                    </div>
                </div>
            </section>

        </main>

        <footer class="mt-16 text-center text-gray-500 text-sm">
            <p>Infografía SPA creada con HTML, Tailwind CSS y Chart.js. Ni Mermaid JS ni SVG fueron utilizados.</p>
        </footer>
    </div>

    <script>
        function getTooltipTitle(tooltipItems) {
            const item = tooltipItems[0];
            let label = item.chart.data.labels[item.dataIndex];
            if (Array.isArray(label)) {
                return label.join(' ');
            } else {
                return label;
            }
        }

        const commonTooltipOptions = {
            plugins: {
                tooltip: {
                    callbacks: {
                        title: getTooltipTitle
                    }
                }
            }
        };
        
        const auditCtx = document.getElementById('auditChart').getContext('2d');
        new Chart(auditCtx, {
            type: 'doughnut',
            data: {
                labels: [['Gastos Operativos', 'Inflados'], ['Bonos No', 'Autorizados'], ['Nómina Fantasma'], ['Otros Desvíos']],
                datasets: [{
                    label: 'Focos de Auditoría',
                    data: [45, 25, 20, 10],
                    backgroundColor: ['#00429D', '#4771B2', '#F97316', '#A9D0DE'],
                    hoverOffset: 4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        position: 'top',
                    },
                    title: {
                        display: false,
                        text: 'Focos de Auditoría (Hipotético)'
                    },
                    tooltip: commonTooltipOptions.plugins.tooltip
                }
            }
        });

        const boardCtx = document.getElementById('boardChart').getContext('2d');
        new Chart(boardCtx, {
            type: 'bar',
            data: {
                labels: [
                    ['Consejeros', 'Ejecutivos'], 
                    ['Consejeros', 'Independientes'], 
                    ['Consejeros', 'Relacionados']
                ],
                datasets: [
                    {
                        label: 'Antes de la Reforma',
                        data: [5, 2, 3],
                        backgroundColor: '#F97316',
                        borderColor: '#F97316',
                        borderWidth: 1
                    },
                    {
                        label: 'Después de la Reforma',
                        data: [3, 7, 1],
                        backgroundColor: '#00429D',
                        borderColor: '#00429D',
                        borderWidth: 1
                    }
                ]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        title: {
                            display: true,
                            text: 'Número de Miembros'
                        }
                    }
                },
                plugins: {
                    title: {
                        display: false,
                        text: 'Composición del Consejo de Administración'
                    },
                    tooltip: commonTooltipOptions.plugins.tooltip
                }
            }
        });

        const vigilanceCtx = document.getElementById('vigilanceChart').getContext('2d');
        new Chart(vigilanceCtx, {
            type: 'line',
            data: {
                labels: ['Ene', 'Feb', 'Mar', 'Abr', 'May', 'Jun'],
                datasets: [
                    {
                        label: 'Reportes en Línea Ética',
                        data: [5, 8, 15, 25, 22, 18],
                        borderColor: '#00429D',
                        backgroundColor: 'rgba(0, 66, 157, 0.1)',
                        fill: true,
                        tension: 0.3,
                        yAxisID: 'y'
                    },
                    {
                        label: 'Pérdidas por Fraude (Miles USD)',
                        data: [50, 45, 30, 15, 10, 5],
                        borderColor: '#F97316',
                        backgroundColor: 'rgba(249, 115, 22, 0.1)',
                        fill: true,
                        tension: 0.3,
                        yAxisID: 'y1'
                    }
                ]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                interaction: {
                    mode: 'index',
                    intersect: false,
                },
                scales: {
                    y: {
                        type: 'linear',
                        display: true,
                        position: 'left',
                        title: {
                            display: true,
                            text: 'Número de Reportes'
                        }
                    },
                    y1: {
                        type: 'linear',
                        display: true,
                        position: 'right',
                        title: {
                            display: true,
                            text: 'Pérdidas (Miles USD)'
                        },
                        grid: {
                            drawOnChartArea: false,
                        },
                    }
                },
                plugins: {
                    title: {
                        display: true,
                        text: 'Impacto Proyectado de la Vigilancia'
                    },
                    tooltip: commonTooltipOptions.plugins.tooltip
                }
            }
        });
    </script>

</body>
</html>
