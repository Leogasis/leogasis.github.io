---
lang: es
title: "¿Cómo decide una empresa a dónde enviar sus camiones?"
excerpt: "Una inmersión profunda en el Vehicle Routing Problem (VRP), el rompecabezas matemático que ahorra millones de galones de combustible y define la logística moderna."
date: 2026-05-07
layout: null
---
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Optimización de Rutas (VRP) | Divulgación Dr. Hernández Landa</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Lexend:wght@400;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        :root {
            --slate-dark: #0F172A;
            --blue-glow: #3B82F6;
            --orange-vibrant: #F97316;
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--slate-dark);
            color: #E2E8F0;
            line-height: 1.6;
        }
        h1, h2, h3, h4 { font-family: 'Lexend', sans-serif; }
        
        .glass-panel {
            background: rgba(30, 41, 59, 0.5);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
        }
        
        .gradient-border {
            position: relative;
            background: linear-gradient(var(--slate-dark), var(--slate-dark)) padding-box,
                        linear-gradient(135deg, #3B82F6, #F97316) border-box;
            border: 2px solid transparent;
        }
        
        .accent-text {
            background: linear-gradient(135deg, #60A5FA 0%, #FDBA74 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .step-card {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .step-card:hover {
            transform: scale(1.02) translateY(-10px);
            border-color: rgba(59, 130, 246, 0.5);
        }

        .math-box {
            font-family: 'Courier New', Courier, monospace;
            background: rgba(0,0,0,0.3);
            border-left: 4px solid var(--blue-glow);
        }
    </style>
</head>
<body class="antialiased selection:bg-orange-500/30">

    <!-- Hero Section -->
    <header class="relative min-h-[80vh] flex items-center justify-center overflow-hidden pt-20">
        <div class="absolute inset-0 z-0">
            <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-blue-600/10 rounded-full blur-[120px]"></div>
            <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-orange-600/10 rounded-full blur-[120px]"></div>
        </div>

        <div class="container mx-auto px-6 z-10 text-center">
            <div class="inline-flex items-center space-x-2 px-4 py-2 rounded-full bg-white/5 border border-white/10 mb-8">
                <span class="flex h-2 w-2 rounded-full bg-orange-500 animate-pulse"></span>
                <span class="text-xs font-bold tracking-widest uppercase text-slate-400">Ciencia de Datos & Logística</span>
            </div>
            
            <h1 class="text-5xl md:text-7xl font-black text-white mb-6 leading-tight">
                ¿Cómo decide una empresa <br>
                <span class="accent-text">a dónde enviar sus camiones?</span>
            </h1>
            
            <p class="text-xl md:text-2xl text-slate-400 max-w-4xl mx-auto font-light leading-relaxed mb-12">
                Una exploración al <strong>Vehicle Routing Problem (VRP)</strong>: el rompecabezas matemático que ahorra millones de galones de combustible y define la eficiencia del siglo XXI.
            </p>
            
            <div class="flex flex-wrap justify-center gap-6">
                <div class="flex items-center space-x-3 bg-slate-800/50 px-6 py-3 rounded-2xl border border-white/5">
                    <img src="/assets/images/profile.png" alt="Dr. Hernández Landa" class="w-10 h-10 rounded-full border border-blue-500/50">
                    <div class="text-left">
                        <p class="text-sm font-bold text-white leading-none">Dr. Leonardo Hernández Landa</p>
                        <p class="text-xs text-slate-500 uppercase tracking-tighter">Investigador SNII | UANL</p>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <main class="container mx-auto px-6 py-24 max-w-5xl space-y-32">

        <!-- Introduction -->
        <section class="grid md:grid-cols-2 gap-16 items-center">
            <div class="space-y-6">
                <h2 class="text-4xl font-bold text-white">El Caos del Mensajero</h2>
                <p class="text-lg text-slate-400">
                    Imagina que tienes 10 camiones y debes entregar paquetes en 50 puntos distintos de la ciudad. Parece sencillo, ¿verdad? Un mapa, unas cuantas líneas y listo. 
                </p>
                <p class="text-lg text-slate-400">
                    Pero la realidad es que el número de combinaciones posibles es mayor que el número de átomos en el universo observable. Este es el corazón del <strong>Vehicle Routing Problem (VRP)</strong>.
                </p>
                <div class="math-box p-6 rounded-2xl mt-8">
                    <p class="text-blue-400 text-sm font-bold mb-2">Dato Curioso:</p>
                    <p class="text-slate-300 italic">Con solo 10 paradas, hay más de 3.6 millones de rutas posibles. Con 20 paradas, hay trillones. ¡La mente humana no puede procesarlo sola!</p>
                </div>
            </div>
            <div class="glass-panel p-8 rounded-[3rem] border-blue-500/20 relative overflow-hidden group">
                <i class="fa-solid fa-truck-fast text-[12rem] absolute -bottom-10 -right-10 text-blue-500/10 group-hover:text-blue-500/20 transition-all duration-700"></i>
                <div class="relative z-10">
                    <h3 class="text-2xl font-bold text-white mb-6">Variables en Juego</h3>
                    <ul class="space-y-4">
                        <li class="flex items-start space-x-4">
                            <div class="bg-blue-500/20 p-2 rounded-lg text-blue-400"><i class="fa-solid fa-clock"></i></div>
                            <div>
                                <h4 class="font-bold text-white text-sm">Ventanas de Tiempo</h4>
                                <p class="text-xs text-slate-500">"Entregar solo entre las 2 y las 4 PM".</p>
                            </div>
                        </li>
                        <li class="flex items-start space-x-4">
                            <div class="bg-orange-500/20 p-2 rounded-lg text-orange-400"><i class="fa-solid fa-weight-hanging"></i></div>
                            <div>
                                <h4 class="font-bold text-white text-sm">Capacidad</h4>
                                <p class="text-xs text-slate-500">El camión no es infinito; tiene un límite de peso/volumen.</p>
                            </div>
                        </li>
                        <li class="flex items-start space-x-4">
                            <div class="bg-blue-500/20 p-2 rounded-lg text-blue-400"><i class="fa-solid fa-traffic-light"></i></div>
                            <div>
                                <h4 class="font-bold text-white text-sm">Tráfico Dinámico</h4>
                                <p class="text-xs text-slate-500">Un accidente cambia la ruta óptima en segundos.</p>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- The "NP-Hard" explanation -->
        <section class="text-center space-y-12">
            <h2 class="text-4xl font-bold text-white">¿Por qué es tan difícil? (El desafío NP-Hard)</h2>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="glass-panel p-10 rounded-3xl step-card border-t-4 border-t-blue-500">
                    <div class="text-5xl font-black text-blue-500/20 mb-4">01</div>
                    <h3 class="text-xl font-bold text-white mb-4">Crecimiento Exponencial</h3>
                    <p class="text-sm text-slate-400">Añadir un solo cliente a la ruta no suma una opción más; multiplica las posibilidades de forma astronómica.</p>
                </div>
                <div class="glass-panel p-10 rounded-3xl step-card border-t-4 border-t-orange-500">
                    <div class="text-5xl font-black text-orange-500/20 mb-4">02</div>
                    <h3 class="text-xl font-bold text-white mb-4">Conflictos de Interés</h3>
                    <h3 class="text-xl font-bold text-white mb-4">Conflicto de Interés</h3>
                    <p class="text-sm text-slate-400">A veces, la ruta más corta no es la más rápida, y la más rápida no es la que gasta menos combustible.</p>
                </div>
                <div class="glass-panel p-10 rounded-3xl step-card border-t-4 border-t-blue-500">
                    <div class="text-5xl font-black text-blue-500/20 mb-4">03</div>
                    <h3 class="text-xl font-bold text-white mb-4">El Muro Computacional</h3>
                    <p class="text-sm text-slate-400">Incluso la supercomputadora más potente tardaría siglos en encontrar la ruta "perfecta" absoluta para 100 clientes.</p>
                </div>
            </div>
        </section>

        <!-- Case Studies -->
        <section class="bg-gradient-to-br from-blue-600/10 to-orange-600/5 rounded-[4rem] p-12 md:p-20 border border-white/5">
            <div class="flex flex-col md:flex-row gap-16 items-center">
                <div class="md:w-1/3">
                    <h2 class="text-4xl font-bold text-white mb-6">Casos de Éxito: <br><span class="text-orange-500">UPS & ORION</span></h2>
                    <p class="text-slate-400">
                        UPS utiliza un sistema llamado <strong>ORION</strong> (On-Road Integrated Optimization and Navigation). Este algoritmo analiza millones de paradas por minuto.
                    </p>
                </div>
                <div class="md:w-2/3 grid grid-cols-1 sm:grid-cols-2 gap-6">
                    <div class="bg-slate-900/80 p-8 rounded-3xl border border-white/5">
                        <p class="text-4xl font-black text-blue-400 mb-2">10M</p>
                        <p class="text-xs uppercase tracking-widest text-slate-500 font-bold">Galones de combustible ahorrados al año</p>
                    </div>
                    <div class="bg-slate-900/80 p-8 rounded-3xl border border-white/5">
                        <p class="text-4xl font-black text-orange-400 mb-2">100K</p>
                        <p class="text-xs uppercase tracking-widest text-slate-500 font-bold">Toneladas de CO2 no emitidas</p>
                    </div>
                    <div class="bg-slate-900/80 p-8 rounded-3xl border border-white/5">
                        <p class="text-4xl font-black text-white mb-2">$400M</p>
                        <p class="text-xs uppercase tracking-widest text-slate-500 font-bold">Ahorro operativo anual estimado</p>
                    </div>
                    <div class="bg-slate-900/80 p-8 rounded-3xl border border-white/5">
                        <p class="text-4xl font-black text-blue-400 mb-2">0 Giros</p>
                        <p class="text-xs uppercase tracking-widest text-slate-500 font-bold">Famosa política de evitar giros a la izquierda</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Deep Research Quote -->
        <section class="max-w-3xl mx-auto text-center space-y-8">
            <i class="fa-solid fa-quote-left text-5xl text-blue-500/20"></i>
            <h2 class="text-3xl font-bold text-white italic">"No buscamos la perfección, buscamos la excelencia operativa en tiempo récord."</h2>
            <p class="text-slate-500">
                En la investigación académica, utilizamos **Metaheurísticas**: algoritmos inspirados en la naturaleza (como el comportamiento de hormigas o la evolución genética) para encontrar soluciones "suficientemente buenas" en apenas unos segundos.
            </p>
        </section>

        <!-- Scientific Footer / References -->
        <footer class="border-t border-slate-800 pt-20 space-y-12">
            <div class="grid md:grid-cols-2 gap-12">
                <div>
                    <h4 class="text-white font-bold mb-4 uppercase tracking-widest text-xs">Anotaciones para el SNII</h4>
                    <p class="text-xs text-slate-500 leading-relaxed">
                        Este artículo de divulgación forma parte de la línea de investigación en **Optimización de Sistemas Productivos y Logísticos**. El VRP representa uno de los pilares de la Investigación de Operaciones moderna, con aplicaciones directas en la descarbonización del transporte y la eficiencia de la última milla.
                    </p>
                </div>
                <div class="bg-white/5 p-8 rounded-3xl border border-white/10">
                    <h4 class="text-white font-bold mb-4 text-sm">Referencias Seleccionadas</h4>
                    <ul class="text-[10px] space-y-2 text-slate-400 font-mono">
                        <li>Dantzig, G. B., & Ramser, J. H. (1959). "The Truck Dispatching Problem". Management Science.</li>
                        <li>Toth, P., & Vigo, D. (2014). "Vehicle Routing: Problems, Methods, and Applications". SIAM.</li>
                        <li>UPS Pressroom (2020). "ORION: The math behind the magic".</li>
                        <li>Braekers, K., et al. (2016). "The vehicle routing problem: State of the art classification and review".</li>
                    </ul>
                </div>
            </div>
            
            <div class="text-center py-10 border-t border-white/5">
                <p class="text-[10px] uppercase tracking-[0.4em] text-slate-600">
                    © 2026 Dr. Leonardo Hernández Landa | Universidad Autónoma de Nuevo León
                </p>
            </div>
        </footer>

    </main>

    <!-- Floating Back Button -->
    <a href="/divulgacion/" class="fixed bottom-10 right-10 bg-blue-600 hover:bg-orange-600 text-white w-12 h-12 rounded-full flex items-center justify-center shadow-2xl transition-all duration-300 z-50">
        <i class="fa-solid fa-arrow-left"></i>
    </a>

</body>
</html>
