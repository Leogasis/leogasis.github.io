---
title: "Blockchain en la Cadena de Suministro"
excerpt: "Del abastecimiento tradicional a una arquitectura de confianza inmutable para la gestión logística del siglo XXI."
date: 2026-05-07
layout: null
---
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blockchain en SCM | Divulgación Científica Dr. Hernández Landa</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Lexend:wght@400;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        :root {
            --navy-dark: #0F172A;
            --teal-bright: #2DD4BF;
            --blue-accent: #3B82F6;
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--navy-dark);
            color: #CBD5E1;
            scroll-behavior: smooth;
        }
        h1, h2, h3 { font-family: 'Lexend', sans-serif; }
        
        .glass-card {
            background: rgba(30, 41, 59, 0.4);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(148, 163, 184, 0.1);
            transition: all 0.3s ease;
        }
        .glass-card:hover {
            border-color: var(--teal-bright);
            transform: translateY(-5px);
        }
        .gradient-text {
            background: linear-gradient(135deg, #2DD4BF 0%, #3B82F6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .hero-gradient {
            background: radial-gradient(circle at 50% 50%, rgba(45, 212, 191, 0.1) 0%, transparent 60%);
        }
        .section-number {
            font-size: 8rem;
            line-height: 1;
            opacity: 0.1;
            position: absolute;
            right: 0;
            top: -2rem;
            font-weight: 800;
        }
    </style>
</head>
<body class="overflow-x-hidden">

    <header class="min-h-screen flex flex-col justify-center items-center p-8 text-center hero-gradient relative">
        <div class="absolute top-10 left-10 opacity-20 hidden md:block">
            <i class="fa-solid fa-link text-9xl text-teal-500"></i>
        </div>
        
        <div class="max-w-5xl z-10">
            <span class="inline-block px-6 py-2 mb-8 text-xs font-bold tracking-[0.2em] text-teal-400 uppercase border border-teal-400/30 rounded-full bg-teal-400/5">
                Comunicación Social de la Ciencia | SNII - CONAHCYT
            </span>
            <h1 class="text-6xl md:text-8xl font-extrabold text-white mb-8 leading-tight">
                Blockchain en la <br><span class="gradient-text">Cadena de Suministro</span>
            </h1>
            <p class="text-xl md:text-2xl text-slate-400 mb-12 max-w-3xl mx-auto leading-relaxed font-light">
                Del abastecimiento tradicional a una arquitectura de confianza inmutable para la gestión logística del siglo XXI.
            </p>
            
            <div class="flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-8 mt-8 bg-slate-900/50 p-8 rounded-3xl border border-white/5">
                <div class="text-center md:text-left">
                    <p class="text-teal-400 font-bold text-lg">Dr. Leonardo Gabriel Hernández Landa</p>
                    <p class="text-sm uppercase tracking-wider text-slate-500">UANL | Facultad de Ciencias Químicas</p>
                </div>
                <div class="hidden md:block h-12 w-px bg-slate-700"></div>
                <div class="text-slate-400 text-sm italic">
                    Línea de investigación: <br>Tecnologías Emergentes en Abastecimiento
                </div>
            </div>
        </div>
        
        <a href="#content" class="absolute bottom-10 animate-bounce text-teal-500 text-3xl">
            <i class="fa-solid fa-chevron-down"></i>
        </a>
    </header>

    <main id="content" class="max-w-6xl mx-auto px-6 py-32 space-y-48">

        <section class="grid lg:grid-cols-2 gap-20 items-center relative">
            <div class="section-number">01</div>
            <div class="space-y-8">
                <h2 class="text-4xl font-bold text-white leading-tight">La Evolución del <span class="text-teal-400">Abastecimiento Digital</span></h2>
                <p class="text-lg leading-relaxed text-slate-400">
                    La transición del modelo tradicional (basado en papel y procesos reactivos) al <strong>e-procurement</strong> representa una reducción del <strong>50% al 70%</strong> en los costos de procesamiento de pedidos.
                </p>
                <div class="grid grid-cols-2 gap-6">
                    <div class="p-4 border-l-2 border-teal-500 bg-teal-500/5">
                        <h4 class="text-white font-bold">Tradicional</h4>
                        <p class="text-sm text-slate-500">Silos de información, fax y comunicación fragmentada.</p>
                    </div>
                    <div class="p-4 border-l-2 border-blue-500 bg-blue-500/5">
                        <h4 class="text-white font-bold">Digital</h4>
                        <p class="text-sm text-slate-500">Visibilidad End-to-End, nube y analítica predictiva.</p>
                    </div>
                </div>
            </div>
            <div class="glass-card p-10 rounded-[3rem] text-center border-teal-500/20">
                <i class="fa-solid fa-chart-line text-7xl text-teal-400 mb-6"></i>
                <h3 class="text-2xl font-bold text-white mb-4">Impacto Estratégico</h3>
                <p class="text-slate-400 text-sm">Eliminación del <em>Maverick Spending</em> y centralización del gasto mediante plataformas de integración (EDI/APIs).</p>
            </div>
        </section>

        <section class="space-y-16">
            <div class="text-center max-w-3xl mx-auto">
                <h2 class="text-4xl font-bold text-white mb-6">Blockchain: El Protocolo de Confianza</h2>
                <p class="text-slate-400">No es solo una base de datos distribuida; es una estructura criptográfica que redefine la verdad en la cadena de suministro.</p>
            </div>
            
            <div class="grid md:grid-cols-4 gap-6">
                <!-- Pillar 1 -->
                <div class="glass-card p-8 rounded-3xl text-center">
                    <i class="fa-solid fa-users-slash text-teal-400 text-3xl mb-4"></i>
                    <h4 class="text-white font-bold mb-2">Descentralización</h4>
                    <p class="text-xs text-slate-500">Sin autoridad central; el control se distribuye en la red.</p>
                </div>
                <!-- Pillar 2 -->
                <div class="glass-card p-8 rounded-3xl text-center">
                    <i class="fa-solid fa-lock text-teal-400 text-3xl mb-4"></i>
                    <h4 class="text-white font-bold mb-2">Inmutabilidad</h4>
                    <p class="text-xs text-slate-500">Registros permanentes vinculados criptográficamente.</p>
                </div>
                <!-- Pillar 3 -->
                <div class="glass-card p-8 rounded-3xl text-center">
                    <i class="fa-solid fa-eye text-teal-400 text-3xl mb-4"></i>
                    <h4 class="text-white font-bold mb-2">Transparencia</h4>
                    <p class="text-xs text-slate-500">Visibilidad compartida de una única versión de la verdad.</p>
                </div>
                <!-- Pillar 4 -->
                <div class="glass-card p-8 rounded-3xl text-center">
                    <i class="fa-solid fa-shield-halved text-teal-400 text-3xl mb-4"></i>
                    <h4 class="text-white font-bold mb-2">Seguridad</h4>
                    <p class="text-xs text-slate-500">Resistencia masiva a ciberataques y alteración de datos.</p>
                </div>
            </div>
        </section>

        <section class="grid lg:grid-cols-2 gap-20 items-center relative">
            <div class="section-number">03</div>
            <div class="order-2 lg:order-1">
                <div class="glass-card p-2 rounded-[2rem] overflow-hidden">
                    <div class="bg-slate-900 p-8 rounded-[1.8rem] border border-white/5">
                        <code class="text-teal-400 text-sm">
                            <span class="text-blue-400">if</span> (temp > 4°C && status == "In-Transit") {<br>
                            &nbsp;&nbsp;triggerPaymentPenalization(vendorID);<br>
                            &nbsp;&nbsp;notifyQualityControl(shipmentID);<br>
                            }
                        </code>
                        <div class="mt-6 pt-6 border-t border-white/10">
                            <h4 class="text-white font-bold mb-2 italic">Smart Contract Logic</h4>
                            <p class="text-xs text-slate-500">Automatización de la lógica contractual sin intermediarios legales.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="order-1 lg:order-2 space-y-8">
                <h2 class="text-4xl font-bold text-white leading-tight">Automatización con <span class="text-blue-500">Smart Contracts</span></h2>
                <p class="text-lg text-slate-400">
                    Los contratos inteligentes permiten ejecutar términos operativos de forma autónoma. Esto reduce los ciclos de conciliación y garantiza el cumplimiento normativo (ESG) en cada eslabón.
                </p>
                <ul class="space-y-4">
                    <li class="flex items-center space-x-3 text-sm">
                        <i class="fa-solid fa-check-circle text-teal-400"></i>
                        <span>Pagos automáticos por hitos verificados.</span>
                    </li>
                    <li class="flex items-center space-x-3 text-sm">
                        <i class="fa-solid fa-check-circle text-teal-400"></i>
                        <span>Trazabilidad ética y ambiental (Pasaporte Digital de Producto).</span>
                    </li>
                </ul>
            </div>
        </section>

        <section class="bg-gradient-to-br from-slate-900 to-navy-dark rounded-[4rem] p-12 md:p-20 border border-white/5 text-center">
            <h2 class="text-4xl font-bold text-white mb-8">Analítica de Datos: El Horizonte Predictivo</h2>
            <p class="text-slate-400 max-w-3xl mx-auto mb-16">
                El e-procurement avanzado evoluciona hacia el <strong>Predictive Sourcing</strong>, donde el Machine Learning analiza el riesgo del proveedor y las tendencias de precios antes de emitir una orden.
            </p>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="p-6">
                    <p class="text-5xl font-extrabold text-teal-400 mb-2">12%</p>
                    <p class="text-sm uppercase tracking-widest text-slate-500 font-bold">Ahorro en Spend Analysis</p>
                </div>
                <div class="p-6">
                    <p class="text-5xl font-extrabold text-blue-500 mb-2">5X</p>
                    <p class="text-sm uppercase tracking-widest text-slate-500 font-bold">Productividad del Comprador</p>
                </div>
                <div class="p-6">
                    <p class="text-5xl font-extrabold text-teal-400 mb-2">85%</p>
                    <p class="text-sm uppercase tracking-widest text-slate-500 font-bold">Precisión en Pronósticos</p>
                </div>
            </div>
        </section>

        <section class="border-t border-slate-800 pt-20">
            <div class="grid md:grid-cols-2 gap-16">
                <div>
                    <h3 class="text-white font-bold mb-4 uppercase tracking-tighter text-sm">Metadatos de Divulgación Académica</h3>
                    <div class="space-y-4 text-xs text-slate-500 leading-relaxed">
                        <p><strong>Clasificación SNII:</strong> Comunicación Social de la Ciencia / Acceso Abierto.</p>
                        <p><strong>Línea de Investigación:</strong> Tecnologías de la Información y Comunicación aplicadas a la Logística y Química Industrial.</p>
                        <p><strong>Institución:</strong> Universidad Autónoma de Nuevo León - Facultad de Ciencias Químicas.</p>
                        <p><strong>Licencia:</strong> <a href="#" class="text-teal-400">Creative Commons Atribución-NoComercial 4.0 Internacional</a>.</p>
                    </div>
                </div>
                <div class="bg-black/40 p-8 rounded-3xl border border-white/5">
                    <h3 class="text-white font-bold mb-4 text-sm">Formato de Citación (Harvard)</h3>
                    <p class="text-xs font-mono text-teal-400 select-all">
                        Hernández-Landa, L. G. (2026). Blockchain en la Cadena de Suministro: Arquitectura de Confianza e Inmutabilidad en el Abastecimiento Digital. [Infografía Interactiva]. Universidad Autónoma de Nuevo León. https://dr-hernandez-landa.github.io/blockchain-scm
                    </p>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-slate-950 py-20 text-center border-t border-white/5 px-6">
        <div class="max-w-4xl mx-auto">
            <img src="https://placehold.co/180x60/0F172A/2DD4BF?text=UANL+FCQ" alt="Logo Institucional" class="mx-auto mb-10 opacity-60">
            <p class="text-white font-bold text-lg mb-2">Dr. Leonardo Gabriel Hernández Landa</p>
            <p class="text-slate-500 text-sm mb-8">Facultad de Ciencias Químicas | Universidad Autónoma de Nuevo León</p>
            
            <div class="flex justify-center space-x-8 text-2xl text-teal-500/50 mb-12">
                <a href="#" class="hover:text-teal-400 transition"><i class="fa-brands fa-orcid"></i></a>
                <a href="mailto:leonardo.hernandez@uanl.mx" class="hover:text-teal-400 transition"><i class="fa-solid fa-envelope"></i></a>
                <a href="#" class="hover:text-teal-400 transition"><i class="fa-brands fa-linkedin"></i></a>
            </div>
            
            <p class="text-slate-600 text-[10px] uppercase tracking-widest leading-loose">
                Este contenido tiene licencia CC BY-NC 4.0. Proyecto financiado bajo los criterios de acceso abierto a la información científica del Sistema Nacional de Investigadoras e Investigadores (México).
            </p>
        </div>
    </footer>

</body>
</html>
