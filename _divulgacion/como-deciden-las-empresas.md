---
lang: es
title: "¿Cómo decide una empresa a dónde enviar sus camiones?"
excerpt: "Una inmersión profunda en el Vehicle Routing Problem (VRP), el rompecabezas matemático que ahorra millones de galones de combustible."
date: 2026-05-07
author: "Leonardo Gabriel Hernández Landa"
affiliation: "Universidad Autónoma de Nuevo León – Facultad de Ciencias Químicas"
header:
  overlay_image: /assets/images/vrp-map.png
  overlay_filter: 0.5
---

![VRP Map](/assets/images/vrp-map.png)

Son las 5 de la mañana en el centro de distribución de una empresa de paquetería en Monterrey. Hay 12 camionetas en el patio y 340 paquetes que deben entregarse antes de las 6 de la tarde. Algunos clientes solo están disponibles en la mañana. Otros tienen restricciones de peso en su acceso. Hay zonas con tráfico pesado a ciertas horas. Y la empresa quiere gastar el menor combustible posible.

¿Cómo se asignan los paquetes a cada camioneta? ¿En qué orden se visitan los clientes? ¿Qué ruta toma cada vehículo?

Responder bien estas preguntas puede significar la diferencia entre una empresa rentable y una que pierde dinero en cada entrega. Y hacerlo mal puede significar que tus paquetes lleguen tarde, o que simplemente no lleguen.

Este es el corazón del **Vehicle Routing Problem (VRP)**, uno de los problemas más estudiados en matemáticas aplicadas e ingeniería industrial en el mundo.

---

## El rompecabezas que nadie ve

Antes de entender por qué este problema es difícil, pongamos los números sobre la mesa.

Si tienes una sola camioneta y debes visitar 10 clientes, el número de rutas posibles supera los **3.6 millones**. Con 15 clientes, ya son más de **1.3 billones** de combinaciones. Con 20 clientes, el número de rutas posibles excede el número estimado de átomos en el universo observable.

Ninguna computadora del mundo puede revisar todas esas combinaciones en tiempo razonable cuando el número de clientes crece. Los matemáticos llaman a este tipo de problemas **NP-difíciles**, lo que básicamente significa que no existe un algoritmo que los resuelva perfectamente y rápidamente para instancias grandes.

Y aquí está la paradoja: las empresas necesitan resolver este problema todos los días, a las 5 de la mañana, antes de que salgan las camionetas. No pueden esperar días para tener la solución perfecta. Necesitan una solución muy buena en minutos o segundos.

Eso es exactamente lo que los investigadores en ingeniería industrial y matemáticas aplicadas llevan décadas construyendo.

---

## Un poco de historia: de los viajantes a los algoritmos modernos

El problema de ruteo de vehículos tiene sus raíces en un problema aún más antiguo: el **Problema del Viajante de Comercio (TSP)**, formulado matemáticamente en los años 1930. Imagina un vendedor que debe visitar N ciudades exactamente una vez y regresar a su punto de partida. ¿Cuál es la ruta más corta?

El VRP moderno fue propuesto por **Dantzig y Ramser en 1959** en un artículo seminal publicado en Management Science. La idea era extender el TSP al caso de múltiples vehículos con capacidad limitada. En ese artículo original, los autores ya planteaban el problema en el contexto de la distribución de gasolina a estaciones de servicio.

Desde entonces, el VRP se ha convertido en uno de los problemas más estudiados en la investigación de operaciones. La razón es simple: tiene aplicaciones prácticas enormes y es matemáticamente fascinante.

---

## Las variantes del problema: porque la realidad siempre es más complicada

El VRP básico asume condiciones ideales que rara vez existen en la práctica. Por eso los investigadores han desarrollado decenas de variantes que incorporan restricciones del mundo real:

**VRP con Ventanas de Tiempo (VRPTW)**
Cada cliente tiene un horario específico en que puede recibir su entrega. El hospital solo acepta suministros de 7 a 9 de la mañana. La tienda no puede recibir camiones después de las 2 de la tarde. El algoritmo debe respetar esas restricciones.

**VRP con Múltiples Depósitos (MDVRP)**
Una empresa grande tiene bodegas en Monterrey, Guadalajara y Ciudad de México. ¿Qué clientes atiende cada bodega? ¿Cómo se distribuye la carga entre ellas?

**VRP con Capacidad (CVRP)**
Cada vehículo tiene un límite de peso y volumen. No puedes cargar más de lo que cabe. El algoritmo debe asignar pedidos respetando esas capacidades.

**VRP con Recogida y Entrega (PDVRP)**
Algunas rutas no solo entregan, también recogen. Piensa en una empresa de logística inversa que recoge devoluciones al mismo tiempo que hace entregas nuevas.

**VRP con Accesibilidad (AVRP)**
Esta es una variante más reciente y particularmente relevante para servicios esenciales. No solo importa llegar a los clientes directos, sino garantizar que las personas en zonas no cubiertas tengan acceso razonable a algún punto de servicio. Esto es crucial en la distribución de medicamentos, alimentos o servicios de salud en zonas marginadas, donde optimizar solo por costo puede dejar sin servicio a las comunidades más vulnerables.

---

## ¿Cómo se resuelve? Los algoritmos detrás de la magia

Dado que no podemos revisar todas las rutas posibles, los investigadores han desarrollado tres grandes familias de métodos:

### Métodos exactos

Resuelven el problema garantizando la solución óptima. Se basan en técnicas de programación lineal entera y ramificación y acotamiento. El problema: solo funcionan para instancias pequeñas (pocas decenas de clientes). Para problemas grandes, pueden tardar días o semanas.

Herramientas como **CPLEX** o **Gurobi** implementan estos métodos y son usadas por investigadores y empresas grandes para validar la calidad de otras soluciones.

### Heurísticas constructivas

En lugar de buscar la solución perfecta, construyen una solución buena rápidamente siguiendo reglas lógicas.

El método más clásico es el **algoritmo de ahorros de Clarke y Wright (1964)**: empieza con una ruta separada para cada cliente y va fusionando rutas cuando la fusión genera un "ahorro" en distancia total. Simple, rápido y sorprendentemente efectivo.

### Metaheurísticas

Son el estado del arte para problemas grandes. Combinan búsqueda inteligente con mecanismos para escapar de soluciones mediocres (óptimos locales).

**Búsqueda Local Iterada (ILS):** Parte de una solución buena, hace pequeños cambios para mejorarla, y periódicamente aplica perturbaciones más grandes para explorar nuevas zonas del espacio de soluciones. Como cuando reorganizas tu cuarto: primero mueves cosas pequeñas, y si no mejora, haces un cambio más drástico.

**Algoritmos Genéticos:** Inspirados en la evolución biológica. Mantienen una "población" de soluciones y las "cruzan" y "mutan" para generar nuevas soluciones, conservando las mejores en cada generación.

**Colonias de Hormigas:** Inspirados en cómo las hormigas encuentran el camino más corto a la comida usando rastros de feromonas. Los caminos más usados se refuerzan, los menos usados se evaporan.

---

## Impacto real: el caso UPS y ORION

El ejemplo más citado en la industria es el sistema **ORION** (On-Road Integrated Optimization and Navigation) de UPS, implementado entre 2012 y 2016.

UPS tiene más de 55,000 conductores en Estados Unidos que hacen entregas diariamente. Antes de ORION, las rutas se planificaban manualmente o con herramientas básicas. Con ORION, un algoritmo sofisticado optimiza las rutas considerando cientos de variables en tiempo real.

Los resultados después de la implementación completa fueron:
- **10 millones** de galones de combustible ahorrados al año
- **100,000 toneladas** de CO₂ no emitidas anualmente
- **400 millones de dólares** en ahorro operativo por año

Y uno de los insights más contraintuitivos que surgió del análisis: UPS instruyó a sus conductores a **evitar giros a la izquierda** siempre que fuera posible (en países con manejo por la derecha). ¿Por qué? Porque los giros a la izquierda implican esperar en el tráfico oncoming, consumiendo combustible en ralentí. Eliminar esos giros redujo distancias, tiempos y consumo de manera significativa.

Es el tipo de insight no obvio que solo aparece cuando analizas datos a gran escala.

---

## El VRP en México: desafíos y oportunidades

México presenta retos logísticos únicos que hacen al VRP especialmente relevante y especialmente difícil:

**Infraestructura vial heterogénea**
La diferencia entre una autopista de cuota bien mantenida y una calle sin pavimento en una zona semiurbana puede significar horas de diferencia en tiempo de entrega. Los modelos deben incorporar esa variabilidad.

**Alto porcentaje de comercio informal**
Muchos negocios no tienen dirección formal, número de calle o código postal confiable. El "Puesto de tacos en la esquina de la farmacia" no es fácil de geocodificar para un algoritmo.

**Crecimiento del comercio electrónico**
El e-commerce en México creció más del 20% anual en los últimos años. Más pedidos, más dispersos, con clientes que esperan entregas cada vez más rápidas. Esto presiona enormemente la logística de última milla.

**Zonas de difícil acceso**
En muchas colonias periféricas de ciudades como Monterrey, las calles no permiten el paso de camiones grandes. La logística debe contemplar transbordos a vehículos más pequeños o incluso a motocicletas.

---

## ¿Qué viene después? Las fronteras de la investigación

El VRP sigue siendo un área activa de investigación. Algunas de las direcciones más interesantes hoy en día:

**VRP en tiempo real y dinámico**
Los pedidos llegan constantemente durante el día. Un camión ya en ruta puede recibir nuevos pedidos o cancelaciones. Los algoritmos deben recalcular rutas en segundos mientras los vehículos están en movimiento.

**VRP con vehículos eléctricos**
Los vehículos eléctricos tienen restricciones adicionales: autonomía limitada, necesidad de recarga, tiempo de carga. Optimizar rutas para flotas eléctricas es un problema nuevo con sus propias complejidades.

**VRP con drones**
Amazon y otros actores ya experimentan con entregas por dron para la última milla. ¿Cómo coordinar una flota mixta de camiones y drones? ¿Qué pedidos asignas a cada uno?

**VRP con consideraciones de equidad y accesibilidad**
Más allá de la eficiencia pura, investigadores están incorporando criterios de equidad: asegurar que zonas de bajos recursos no queden sistemáticamente desatendidas por los algoritmos de optimización. Este enfoque es especialmente relevante para la distribución de servicios públicos esenciales.

---

## Reflexión final

Cada vez que recibes un paquete, compras en el supermercado o usas un servicio de transporte urbano, detrás hay décadas de investigación matemática trabajando silenciosamente para que todo llegue a tiempo, al menor costo posible y con el menor impacto ambiental.

El VRP no es solo un problema académico interesante. Es una herramienta concreta para hacer más eficientes los sistemas que mueven nuestra economía y, bien aplicado, puede contribuir a hacerlos también más justos y sostenibles.

La próxima vez que veas una camioneta de repartos recorriendo tu calle, recuerda: su ruta no fue elegida al azar. Fue calculada por un algoritmo que resolvió un problema que los matemáticos llevan más de 60 años estudiando.

---

*Referencias:*
- Dantzig, G.B. & Ramser, J.H. (1959). The Truck Dispatching Problem. *Management Science*, 6(1), 80-91.
- Toth, P. & Vigo, D. (2014). *Vehicle Routing: Problems, Methods, and Applications*. SIAM.
- Ibarra-Rojas, O.J., Hernandez, L. & Ozuna, L. (2018). The Accessibility Vehicle Routing Problem. *Journal of Cleaner Production*, 172, 1514-1528.

---

*Este artículo forma parte de la línea de investigación en Optimización Logística y Accesibilidad del Dr. Leonardo Gabriel Hernández Landa (UANL).*  
*Contenido de acceso libre y gratuito.*  
*Contacto: leonardo.hernandezln@uanl.edu.mx*
