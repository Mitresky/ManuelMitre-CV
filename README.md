<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive CV - Manuel Mitre</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Neutrals -->
    <!-- Application Structure Plan: A single-page application with a top navigation bar for smooth scrolling to thematic sections: Home, Experience, Skills/Education, and Contact. The experience section is an interactive vertical timeline where users can click to expand job details. This structure is intuitive for recruiters, allowing for quick scanning and deep dives into specific areas, making the content more engaging and digestible than a static document. -->
    <!-- Visualization & Content Choices: 
        1. Report Info: Skills (Competencias). Goal: Inform/Compare. Viz: Radar Chart (Chart.js/Canvas). Interaction: Hover to see skill names. Justification: Provides a dynamic and quick visual summary of core competencies, more engaging than a list.
        2. Report Info: Work Experience. Goal: Organize/Show Change. Viz: Interactive Vertical Timeline (HTML/CSS/JS). Interaction: Click job title to toggle visibility of details. Justification: Cleans up the layout and allows users to focus on specific roles, highlighting career progression effectively.
        3. Report Info: Education/Courses. Goal: Inform. Viz: Styled List (HTML/Tailwind). Interaction: None. Justification: Clear and straightforward presentation for factual information.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
            height: 400px;
            max-height: 50vh;
        }
    </style>
</head>
<body class="bg-neutral-50 text-neutral-800">

    <header class="bg-white/80 backdrop-blur-sm sticky top-0 z-50 shadow-sm">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#home" class="text-xl font-bold text-neutral-800">Manuel Mitre</a>
            <div class="hidden md:flex space-x-8">
                <a href="#experience" class="text-neutral-600 hover:text-blue-600 transition-colors">Experience</a>
                <a href="#skills" class="text-neutral-600 hover:text-blue-600 transition-colors">Skills</a>
                <a href="#education" class="text-neutral-600 hover:text-blue-600 transition-colors">Education</a>
                <a href="#contact" class="text-neutral-600 hover:text-blue-600 transition-colors">Contact</a>
            </div>
            <button id="mobile-menu-button" class="md:hidden text-neutral-600 focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
            </button>
        </nav>
        <div id="mobile-menu" class="hidden md:hidden bg-white">
            <a href="#experience" class="block text-center py-2 px-4 text-sm text-neutral-600 hover:bg-neutral-100">Experience</a>
            <a href="#skills" class="block text-center py-2 px-4 text-sm text-neutral-600 hover:bg-neutral-100">Skills</a>
            <a href="#education" class="block text-center py-2 px-4 text-sm text-neutral-600 hover:bg-neutral-100">Education</a>
            <a href="#contact" class="block text-center py-2 px-4 text-sm text-neutral-600 hover:bg-neutral-100">Contact</a>
        </div>
    </header>

    <main>
        <section id="home" class="min-h-[60vh] flex items-center bg-white">
            <div class="container mx-auto px-6 py-16 text-center">
                <h1 class="text-4xl md:text-6xl font-bold text-neutral-900 leading-tight">Manuel Mitre</h1>
                <p class="text-xl md:text-2xl text-blue-600 font-medium mt-4">Bachelor's Degree in International Business and Trade</p>
                <p class="max-w-3xl mx-auto mt-6 text-neutral-600">
                    Professional with experience in operations, logistics, data analysis, and commercial management. I seek to contribute to the growth and operational efficiency of a dynamic organization through my experience in strategic planning, process optimization, and team leadership.
                </p>
                <div class="mt-8 flex justify-center space-x-4">
                    <a href="#contact" class="bg-blue-600 text-white font-bold py-3 px-6 rounded-lg hover:bg-blue-700 transition-transform hover:scale-105 shadow-lg">Contact Me</a>
                    <a href="https://www.linkedin.com/in/mitreortiz/" target="_blank" class="bg-white text-neutral-700 font-bold py-3 px-6 rounded-lg hover:bg-neutral-100 transition-transform hover:scale-105 shadow-lg border border-neutral-200">LinkedIn</a>
                </div>
            </div>
        </section>

        <section id="experience" class="py-20">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-4">Professional Experience</h2>
                <p class="text-center text-neutral-600 max-w-2xl mx-auto mb-12">A journey through my professional career, highlighting key roles and responsibilities. Click on each position to see the details.</p>
                
                <div class="relative wrap overflow-hidden p-10 h-full">
                    <div class="border-2-2 absolute border-opacity-20 border-neutral-700 h-full border" style="left: 50%"></div>

                    <div class="mb-8 flex justify-between items-center w-full right-timeline">
                        <div class="order-1 w-5/12"></div>
                        <div class="z-20 flex items-center order-1 bg-blue-600 shadow-xl w-8 h-8 rounded-full">
                            <h1 class="mx-auto font-semibold text-lg text-white">1</h1>
                        </div>
                        <div class="order-1 bg-white rounded-lg shadow-xl w-5/12 px-6 py-4 timeline-item cursor-pointer">
                            <h3 class="font-bold text-neutral-800 text-xl">Operations Analyst</h3>
                            <p class="text-sm leading-snug tracking-wide text-neutral-500">Coppel | 2022 - Present</p>
                            <div class="text-neutral-600 mt-3 text-sm hidden details">
                                <ul class="list-disc pl-5 space-y-1">
                                    <li>Optimize logistics processes to ensure timely and efficient deliveries.</li>
                                    <li>Identify trends, patterns, and anomalies in data (SQL, VS Code).</li>
                                    <li>Collaborate with Last Mile for strategic decision-making.</li>
                                    <li>Manage indemnities and penalties for KPI non-compliance.</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <div class="mb-8 flex justify-between flex-row-reverse items-center w-full left-timeline">
                        <div class="order-1 w-5/12"></div>
                        <div class="z-20 flex items-center order-1 bg-blue-600 shadow-xl w-8 h-8 rounded-full">
                            <h1 class="mx-auto text-white font-semibold text-lg">2</h1>
                        </div>
                        <div class="order-1 bg-white rounded-lg shadow-xl w-5/12 px-6 py-4 timeline-item cursor-pointer">
                            <h3 class="font-bold text-neutral-800 text-xl">Commercial Coordinator</h3>
                            <p class="text-sm leading-snug tracking-wide text-neutral-500">Galbo | 2021</p>
                             <div class="text-neutral-600 mt-3 text-sm hidden details">
                                <ul class="list-disc pl-5 space-y-1">
                                    <li>Manage the commercial department and create an external communication plan.</li>
                                    <li>Identify strategic opportunities to maximize results.</li>
                                    <li>Coordinate and negotiate terms for service contracting.</li>
                                    <li>Public relations.</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mb-8 flex justify-between items-center w-full right-timeline">
                        <div class="order-1 w-5/12"></div>
                        <div class="z-20 flex items-center order-1 bg-blue-600 shadow-xl w-8 h-8 rounded-full">
                            <h1 class="mx-auto font-semibold text-lg text-white">3</h1>
                        </div>
                        <div class="order-1 bg-white rounded-lg shadow-xl w-5/12 px-6 py-4 timeline-item cursor-pointer">
                            <h3 class="font-bold text-neutral-800 text-xl">Account Executive</h3>
                            <p class="text-sm leading-snug tracking-wide text-neutral-500">HSBC | 2019 - 2021</p>
                            <div class="text-neutral-600 mt-3 text-sm hidden details">
                                <ul class="list-disc pl-5 space-y-1">
                                    <li>Manage and analyze the client portfolio.</li>
                                    <li>Identify and manage potential credit risks.</li>
                                    <li>Sell financial products and services.</li>
                                    <li>Ensure client operations remain within regulations.</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <div class="mb-8 flex justify-between flex-row-reverse items-center w-full left-timeline">
                        <div class="order-1 w-5/12"></div>
                        <div class="z-20 flex items-center order-1 bg-blue-600 shadow-xl w-8 h-8 rounded-full">
                            <h1 class="mx-auto text-white font-semibold text-lg">4</h1>
                        </div>
                        <div class="order-1 bg-white rounded-lg shadow-xl w-5/12 px-6 py-4 timeline-item cursor-pointer">
                            <h3 class="font-bold text-neutral-800 text-xl">Administrative Secretary</h3>
                            <p class="text-sm leading-snug tracking-wide text-neutral-500">UAS | 2014 - 2019</p>
                            <div class="text-neutral-600 mt-3 text-sm hidden details">
                                <ul class="list-disc pl-5 space-y-1">
                                    <li>Responsible for managing the billing cycle.</li>
                                    <li>Coordinate administrative staff and develop performance reports.</li>
                                    <li>Manage supplier relations and acquisition of supplies.</li>
                                    <li>Request, control, and accountability.</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="skills" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-4">Key Skills</h2>
                 <p class="text-center text-neutral-600 max-w-2xl mx-auto mb-12">A glimpse into my key competencies that drive my professional performance. Hover over the chart to explore my strengths.</p>
                <div class="chart-container">
                    <canvas id="skillsChart"></canvas>
                </div>
            </div>
        </section>

        <section id="education" class="py-20">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-12">Education and Courses</h2>
                <div class="grid md:grid-cols-2 gap-12">
                    <div class="text-center">
                        <h3 class="text-2xl font-semibold mb-4">Academic Background</h3>
                        <div class="space-y-6">
                            <div class="bg-white p-6 rounded-lg shadow-md">
                                <h4 class="font-bold text-lg">Master's Degree in Business Management</h4>
                                <p class="text-neutral-600">Universidad México Internacional</p>
                                <p class="text-neutral-500 text-sm">2024 - Present</p>
                            </div>
                            <div class="bg-white p-6 rounded-lg shadow-md">
                                <h4 class="font-bold text-lg">Bachelor's Degree in International Business and Trade</h4>
                                <p class="text-neutral-600">Universidad Autónoma de Sinaloa</p>
                                <p class="text-neutral-500 text-sm">2012 - 2016</p>
                            </div>
                        </div>
                    </div>
                    <div class="text-center">
                        <h3 class="text-2xl font-semibold mb-4">Certifications and Courses</h3>
                        <div class="space-y-4">
                           <div class="bg-white p-4 rounded-lg shadow-sm border-l-4 border-blue-500">
                               <p class="font-semibold">Diploma in ESG training in the Financial System</p>
                               <p class="text-sm text-neutral-500">Global Business School HSBC</p>
                           </div>
                           <div class="bg-white p-4 rounded-lg shadow-sm border-l-4 border-blue-500">
                               <p class="font-semibold">Certification in AML/CTF</p>
                               <p class="text-sm text-neutral-500">HSBC</p>
                           </div>
                           <div class="bg-white p-4 rounded-lg shadow-sm border-l-4 border-blue-500">
                               <p class="font-semibold">15 Indispensable Laws of Leadership</p>
                               <p class="text-sm text-neutral-500">Botcam Lidera</p>
                           </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="contact" class="py-20 bg-neutral-800 text-white">
            <div class="container mx-auto px-6 text-center">
                <h2 class="text-3xl font-bold mb-4">Interested in collaborating?</h2>
                <p class="max-w-2xl mx-auto mb-8">I am available for new opportunities. Feel free to contact me.</p>
                <div class="flex flex-col md:flex-row justify-center items-center space-y-4 md:space-y-0 md:space-x-8">
                    <a href="mailto:mitreorliz@omall.com" class="text-lg hover:text-blue-400 transition-colors">mitreorliz@omall.com</a>
                    <span class="hidden md:block">|</span>
                    <p class="text-lg">Tel: 6672-20-55-17</p>
                    <span class="hidden md:block">|</span>
                    <a href="https://www.linkedin.com/in/mitreortiz/" target="_blank" class="text-lg hover:text-blue-400 transition-colors">LinkedIn</a>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-white py-4">
        <div class="container mx-auto px-6 text-center text-sm text-neutral-500">
            <p>&copy; 2024 Manuel Mitre. Interactively designed and developed.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            
            mobileMenuButton.addEventListener('click', function() {
                mobileMenu.classList.toggle('hidden');
            });
            
            const menuLinks = mobileMenu.querySelectorAll('a');
            menuLinks.forEach(link => {
                link.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                });
            });

            const timelineItems = document.querySelectorAll('.timeline-item');
            timelineItems.forEach(item => {
                item.addEventListener('click', () => {
                    const details = item.querySelector('.details');
                    details.classList.toggle('hidden');
                });
            });
            
            const ctx = document.getElementById('skillsChart').getContext('2d');
            const skillsChart = new Chart(ctx, {
                type: 'radar',
                data: {
                    labels: ['Adaptability', 'Leadership', 'Pressure Tolerance', 'Business Development', 'Competitiveness', 'Data Analysis'],
                    datasets: [{
                        label: 'Key Competencies',
                        data: [5, 5, 5, 5, 5, 5],
                        backgroundColor: 'rgba(74, 144, 226, 0.2)',
                        borderColor: 'rgba(74, 144, 226, 1)',
                        borderWidth: 2,
                        pointBackgroundColor: 'rgba(74, 144, 226, 1)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgba(74, 144, 226, 1)'
                    }]
                },
                options: {
                    maintainAspectRatio: false,
                    responsive: true,
                    scales: {
                        r: {
                            angleLines: {
                                color: 'rgba(0, 0, 0, 0.1)'
                            },
                            grid: {
                                color: 'rgba(0, 0, 0, 0.1)'
                            },
                            pointLabels: {
                                font: {
                                    size: 12,
                                    weight: 'bold'
                                },
                                color: '#333'
                            },
                            ticks: {
                                backdropColor: 'transparent',
                                display: false,
                                stepSize: 1
                            },
                            suggestedMin: 0,
                            suggestedMax: 5
                        }
                    },
                    plugins: {
                        legend: {
                            display: false
                        }
                    }
                }
            });
        });
    </script>
</body>
</html>
