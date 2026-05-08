---
lang: es
title: "Blockchain en la Cadena de Suministro"
excerpt: "Del abastecimiento tradicional a una arquitectura de confianza inmutable para la gestión logística del siglo XXI."
date: 2024-07-22
author: "Leonardo Gabriel Hernández Landa"
affiliation: "Universidad Autónoma de Nuevo León – Facultad de Ciencias Químicas"
header:
  overlay_image: /assets/images/blockchain-scm.png
  overlay_filter: 0.5
  teaser: /assets/images/blockchain-scm.png
---

> **Por:** **Dr. Leonardo Gabriel Hernández Landa**  
> <i class="fas fa-university"></i> Facultad de Ciencias Químicas, Universidad Autónoma de Nuevo León  
> <i class="fas fa-microchip"></i> Línea de investigación: *Optimización, Inteligencia Artificial y Logística*  
> <i class="far fa-calendar-alt"></i> Publicado originalmente: Julio 2024

---

![Blockchain SCM](/assets/images/blockchain-scm.png)

Piensa en la última vez que compraste un medicamento, un kilo de aguacate o un par de zapatos. ¿Alguna vez te preguntaste cuántas manos tocaron ese producto antes de llegar a las tuyas? ¿Cómo sabes que el medicamento es auténtico? ¿Que el aguacate realmente viene de donde dice la etiqueta? ¿Que las condiciones de fabricación de esos zapatos fueron éticas?

La respuesta honesta es: casi nunca podemos saberlo con certeza. Y ese es exactamente el problema que Blockchain promete resolver en la cadena de suministro.

---

## El problema invisible de la confianza

Históricamente, la gestión de la cadena de suministro ha dependido de silos de información, documentos en papel, correos electrónicos y procesos manuales que carecen de transparencia. Cada empresa guarda su propia versión de los datos. El proveedor tiene sus registros. El transportista tiene los suyos. El distribuidor los suyos. Y muchas veces esas versiones no coinciden.

Esto genera problemas enormes:

- **Fraude y falsificación:** La Organización Mundial de la Salud estima que hasta el 10% de los medicamentos en países de ingresos medios y bajos son falsificados. En México, el IMSS ha reportado decomisos de medicamentos apócrifos con regularidad.
- **Ineficiencia operativa:** Cuando hay una disputa entre proveedor y cliente, reconciliar los datos puede tomar semanas. Cada parte revisa sus propios archivos, busca correos, llama a intermediarios.
- **Falta de trazabilidad:** Cuando hay un brote de contaminación alimentaria, como los casos de listeria o salmonela en lechugas o fresas, los rastreos tradicionales tardan días o semanas. Para entonces, el daño ya está hecho.

La transición del modelo tradicional al **e-procurement** ya representó una reducción del **50% al 70%** en los costos operativos de muchas empresas. Pero el reto de la confianza entre partes que no se conocen entre sí sigue siendo el talón de Aquiles de la logística moderna.

---

## ¿Qué es Blockchain y cómo funciona?

Antes de hablar de cadenas de suministro, entendamos qué es Blockchain con una analogía simple.

Imagina un cuaderno de contabilidad que todos los participantes de una red pueden ver, pero que nadie puede borrar ni modificar. Cada vez que alguien registra una transacción, esa anotación queda permanentemente grabada y es visible para todos. No existe una autoridad central que controle ese cuaderno: todos tienen una copia idéntica y actualizada.

Eso, en esencia, es Blockchain: una **base de datos distribuida e inmutable** donde cada registro nuevo (llamado "bloque") se encadena criptográficamente al anterior, formando una cadena de bloques. Modificar un registro antiguo requeriría cambiar todos los bloques posteriores en todas las copias de la red simultáneamente, algo computacionalmente imposible en la práctica.

### Los tres pilares tecnológicos que lo hacen posible

**Seguridad mediante criptografía**

Cada bloque contiene un "hash", que es una especie de huella digital matemática del bloque anterior. Si alguien intentara alterar un registro antiguo, su hash cambiaría, lo que invalidaría todos los bloques posteriores. La red detectaría inmediatamente la manipulación. Es como si al borrar una palabra de un libro, todas las páginas siguientes se volvieran ilegibles automáticamente.

**Transparencia controlada**

Todos los participantes autorizados en la red pueden ver los registros en tiempo real. Esto no significa que todo sea público: las redes de Blockchain empresariales (llamadas "permisionadas") permiten definir exactamente quién puede ver qué información. El proveedor puede ver lo que le corresponde, el cliente lo suyo, el regulador lo que necesita para cumplir su función.

**Eficiencia mediante contratos inteligentes**

Los "smart contracts" o contratos inteligentes son programas que se ejecutan automáticamente cuando se cumplen ciertas condiciones. Por ejemplo: "cuando el sensor confirme que el medicamento llegó al hospital a temperatura correcta, libera automáticamente el pago al proveedor". Sin intermediarios, sin llamadas telefónicas, sin papeleo. El proceso ocurre solo.

---

## Blockchain en acción: casos reales en cadena de suministro

### Trazabilidad alimentaria: el proyecto de Walmart y IBM

En 2018, Walmart implementó junto con IBM una solución Blockchain para rastrear mangos en Estados Unidos y carne de puerco en China. El resultado fue impresionante: el tiempo para rastrear el origen de un alimento pasó de **7 días a 2.2 segundos**.

Para ponerlo en perspectiva: en un brote de contaminación alimentaria, cada hora cuenta. Si en 2.2 segundos puedes identificar exactamente qué lote está contaminado, en qué tiendas está y retirarlo del mercado, puedes salvar vidas y evitar el retiro masivo de productos que no tienen ningún problema.

Para México, donde la exportación de aguacate, tomate y otros productos agrícolas es fundamental, este tipo de tecnología representa una oportunidad enorme de certificar origen y condiciones de producción ante mercados exigentes como el de Estados Unidos o Europa.

### Medicamentos auténticos: la lucha contra la falsificación

En Estados Unidos, la ley DSCSA (Drug Supply Chain Security Act) exige que para 2025 todos los medicamentos cuenten con rastreo electrónico a nivel de unidad individual. Blockchain es una de las tecnologías más prometedoras para cumplir este requisito.

Empresas como MediLedger han construido redes Blockchain donde farmacéuticas, distribuidores y farmacias verifican la autenticidad de los medicamentos en tiempo real. Cada pastilla tiene su historia verificable: dónde se fabricó, en qué condiciones se almacenó, por cuántas manos pasó.

### Industria automotriz: piezas con historia verificable

BMW, Volkswagen y Ford ya experimentan con Blockchain para rastrear materias primas como el cobalto (esencial para las baterías de autos eléctricos) desde su extracción en minas de África hasta la línea de ensamblaje. El objetivo es verificar que las condiciones de extracción no involucren trabajo infantil o daño ambiental, un requisito cada vez más exigido por los consumidores europeos.

Para las plantas automotrices en Nuevo León, proveedoras de marcas globales, entender y adaptarse a estos estándares se vuelve cada vez más urgente.

---

## ¿Cuáles son los retos reales?

Sería deshonesto presentar Blockchain como la solución perfecta a todos los problemas logísticos. Como toda tecnología, tiene limitaciones importantes:

**El problema del "garbage in, garbage out"**

Blockchain garantiza que los datos registrados no se alteran. Pero no garantiza que los datos sean correctos desde el inicio. Si alguien registra información falsa al ingresar un producto a la cadena (por ejemplo, dice que un medicamento se almacenó a 4°C cuando en realidad estuvo a 20°C), esa mentira quedará permanentemente grabada como verdad. La tecnología necesita complementarse con sensores confiables y procesos de verificación física.

**Escalabilidad y consumo energético**

Las redes Blockchain públicas como Bitcoin consumen cantidades enormes de energía eléctrica. Para aplicaciones empresariales se usan redes privadas más eficientes, pero la escalabilidad sigue siendo un reto cuando se habla de miles de transacciones por segundo.

**Integración con sistemas heredados**

La mayoría de las empresas, especialmente las PyMEs mexicanas, trabajan con sistemas de gestión antiguos (ERPs legacy, hojas de Excel, incluso registros en papel). Integrar Blockchain con esa infraestructura existente requiere inversión y tiempo.

**Adopción de toda la cadena**

Blockchain solo funciona si todos los participantes de la cadena lo usan. Si el proveedor más pequeño de la red no se integra, hay un eslabón roto en la trazabilidad. Lograr esa adopción masiva es un reto organizacional tanto o más difícil que el tecnológico.

---

## ¿Qué significa esto para México y para los ingenieros industriales?

México ocupa el lugar 13 entre los países con mayor volumen de comercio mundial. Somos el principal socio comercial de Estados Unidos. Nuestra industria manufacturera, automotriz, alimentaria y electrónica depende de cadenas de suministro eficientes y confiables.

La adopción de tecnologías como Blockchain en la cadena de suministro mexicana está apenas en sus primeras etapas. Pero las presiones del mercado internacional, especialmente los requisitos de trazabilidad de Estados Unidos y Europa, van a acelerar esta adopción en los próximos años.

Para los ingenieros industriales, esto representa una oportunidad concreta: las empresas necesitan profesionales que entiendan tanto la lógica de la cadena de suministro como las posibilidades y limitaciones de estas nuevas tecnologías. No se trata de convertirse en programadores de Blockchain, sino de ser capaces de identificar dónde tiene sentido aplicarla, gestionar su implementación y medir su impacto.

---

## Reflexión final

La próxima vez que compres un medicamento, un alimento importado o un componente electrónico, recuerda que detrás de ese producto hay una cadena de custodia que puede tener decenas de eslabones. La pregunta que Blockchain intenta responder es simple pero poderosa: **¿cómo construimos confianza entre personas y organizaciones que no se conocen entre sí?**

La respuesta que propone es igualmente elegante: no dependas de que alguien sea honesto, diseña un sistema donde sea prácticamente imposible ser deshonesto.

Eso es exactamente lo que la ingeniería industrial lleva décadas intentando hacer con los procesos físicos. Ahora tenemos una herramienta para hacerlo también con la información.

---

**¿Te resultó útil este contenido?**  
Si este artículo te sirvió para tu investigación o curiosidad personal, puedes citarlo de la siguiente manera:

> [!TIP]
> **Formato de cita APA:**  
> Hernández Landa, L. G. ({{ page.date | date: "%Y" }}). *{{ page.title }}*. Divulgación Científica - Leogasis Académico. Recuperado de [https://leogasis.github.io{{ page.url }}](https://leogasis.github.io{{ page.url }})

---
*Este contenido es de acceso abierto bajo licencia Creative Commons. Se permite su uso citando debidamente al autor.*

---
*Contacto: leonardo.hernandezln@uanl.edu.mx*
