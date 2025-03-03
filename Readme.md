¿Qué es la arquitectura de software?
La arquitectura de software es un término crucial en el desarrollo de software que se refiere a las estructuras de un sistema. Implica el modeloado de diagramas, la definición de la comunicación entre sistemas y los módulos individuales dentro de un sistema. En este curso, guiado por Guido Contreras Goda, exploraremos profundamente el papel fundamental que juega la arquitectura en cada etapa del proceso de desarrollo de software.

Este enfoque no solo ayuda a mejorar la comprensión técnica sino que también clarifica cuándo y cómo tomar decisiones arquitectónicas efectivas, determinando así el éxito o fracaso de un sistema.

Se refiere a las estructuras de un sistema => 

	- modelado de diagrama 
	- Definición entre sistemas  
	- Definición de los modulo de un sistema 
	- modelado de diagrama 

===================================
Resumen

El proceso de desarrollo tradicional tiene etapas muy marcadas, que tienen entradas, procesos y salidas que funcionan como entradas de la siguiente etapa.

Análisis de requerimientos: Todo nace de un disparador que nos crea la necesidad de crear un artefacto o un sistema. Necesitamos entender cuál es el problema que queremos resolver. Hay requerimientos de negocio, requerimientos funcionales, requerimientos no funcionales.

Diseño de la solución: Análisis profundo de los problemas para trabajar en conjunto y plantear posibles soluciones. El resultado de esto debe ser el detalle de la solución, a través de requerimientos, modelado, etc.

Desarrollo y evolución: Implementación de la solución, para garantizar que lo que se esta construyendo es lo que se espera. Al finalizar esta etapa tendremos un artefacto de software.

Despliegue: Aquí vamos a necesitar de infraestructura y de roles de operación para poder poner el artefacto a disponibilidad.

Mantenimiento y evolución: Desarrollo + despliegue + mantenimiento, en esta etapa estamos atentos a posible mejoras que se hacen al sistema. En esta etapa el software se mantiene hasta que el software ya deja de ser necesario.


Mostrar menos

===================================
En la etapa de diseño y desarrollo estamos concentrados en encontrar cuáles son los problemas que queremos resolver. Estos problemas los podemos dividir en dos grandes tipos de problemas.

Esenciales: Los podemos dividir en 4.

La complejidad, cuándo lo que tenemos que resolver es complejo en si mismo, por ejemplo calcular la mejor ruta entre ciudades.
La conformidad.
Tolerancia al cambio.
Invisibilidad.
**Accidentales:**Está relacionado con la plataforma que vamos a implementar, tecnología, lenguajes, frameworks, integraciones, etc.
===================================
-------------- Roles en metodologías tradicionales y ágiles -------------- 
Resumen

Es importante que diferenciemos el ROL del puesto de trabajo, hay roles que pueden ser desarrollados por la misma persona.

Experto del dominio: En una metodología tradicional, es la persona a la que acudimos para entender las necesidades del negocio. En metodologías ágiles y stakeholders.

Analista del negocio: funcional/de negocio, la persona responsable de definir los requerimientos que van a llevar al software a u buen puerto. En el caso de Ágiles el dueño del producto es quien arma las historias y que nos acompaña en el proceso de construcción del software.

Administrador de sistemas / DevOps: Es el rol de operaciones y desarrollo, son las personas responsables de la infraestructura que alojara nuestra aplicación.

Equipo de desarrollo: QA / Testing se encargan de la evaluación de nuestro software, comprobar que lo que se está haciendo es lo que se espera que se haga. Desarrolladores involucrados en la construcción del software. Arquitecto, diseña la solución y análisis de los requerimientos, es un papel más estratégico. La arquitectura emerja del trabajo de un equipo bien gestionado.

Gestor del proyecto / facilitador: Llevan al equipo a través del proceso iterativo e incremental, entender lo que pasa con el equipo y motivar el avance en el desarrollo del producto.
scrum master trata de ser facilitador 



===================================
## ¿Qué es la arquitectura de software?

La arquitectura de software es un concepto amplio que muchas veces se asocia con modelos y diagramas llenos de líneas y cajas que representan la solución de un sistema. Sin embargo, va más allá del simple modelado. Se trata de un análisis profundo de lo que hay que construir, los requerimientos que se deben considerar y cómo el sistema los resolverá.

### Definiciones clave de la arquitectura de software

- **Estructura de un sistema:** Según el libro *Software Architecture in Practice*, la arquitectura es la estructura compuesta por elementos y sus propiedades. La arquitectura se centra en la organización estructural del software, que puede involucrar agrupación en módulos u objetos, ocultamiento de propiedades y exposición de APIs públicas.
- **Conjunto de decisiones:** *Software Architecture Foundations, Theory, and Practice* se enfoca en las decisiones de diseño que son cruciales para la construcción del sistema. Este enfoque destaca la importancia de decisiones que impactan en los requerimientos y la calidad del software.
- **Importancia de las actividades:** Martin Fowler, en *Patterns of Enterprise Application Architecture*, define la arquitectura como cualquier actividad importante para el sistema. Su planteamiento está alineado con metodologías ágiles, sugiriendo que la arquitectura debe emerger del equipo de desarrollo mediante decisiones críticas.

### ¿Cómo influyen los arquitectos de software en las organizaciones?

Un arquitecto de software no solamente diseña sistemas, también juega un rol esencial dentro de las organizaciones. Su labor se ve impactada por las distintas metodologías de trabajo y la dinámica organizativa.

#### Responsabilidades de un arquitecto de software

- **Toma de decisiones:** Los arquitectos deben evaluar los requerimientos y decidir cómo estructurarlos para maximizar la calidad del sistema.
- **Influir en la implementación:** Sus decisiones son clave para guiar la implementación del software hacia los objetivos planteados.
- **Adaptación a metodologías:** En contextos ágiles, la arquitectura emerge de decisiones colaborativas y el arquitecto debe facilitar este proceso dentro del equipo.

### Ejemplos de arquitecturas en la práctica

#### La arquitectura de Twitter
La arquitectura de Twitter es un ejemplo ilustrativo de cómo una aplicación maneja grandes volúmenes de datos e interacción en tiempo real:

- **Write API:** Al enviar un tweet, la petición pasa a través de una API que distribuye información a distintos módulos.
- **Procesamiento de mensajes:** Servicios internos gestionan hashtags, menciones y se encargan de actualizar las *timelines* adecuadas, conectando al autor del mensaje con todos los seguidores.

#### La arquitectura de Amazon
Amazon ofrece otra perspectiva centrada en el despliegue de aplicaciones:

- **Despliegue escalable:** Utilizan servidores autoescalables y contenedores para maximizar la eficiencia del despliegue.
- **Servicios complementarios:** Ofrecen servicios de base de datos, caché, y más para facilitar la implementación y operación de aplicaciones en su infraestructura.

#### Arquitectura de una aplicación Flax
Esta aplicación muestra cómo manejar el flujo de datos a través de su arquitectura:

- **Flujo de datos unidireccional:** Flax establece conexiones entre módulos asegurando que los datos viajen en una única dirección, crucial para aplicaciones *frontend* modernas como las de React.

### ¿Cómo se refleja la arquitectura en diagramas?
Cada sistema de software puede ser visualizado mediante diferentes diagramas arquitectónicos que resaltan atributos o vistas distintas del sistema. Estas vistas ayudan a evaluar criterios como el flujo de datos, la disponibilidad, y la carga del sistema, influenciando las decisiones arquitectónicas. Por ejemplo, Flax se enfoca en el flujo de datos, mientras que Amazon se preocupa por la disponibilidad y distribución de carga, aspectos críticos en la elección de una arquitectura adecuada.



===================================
-------------- -------------- 


===================================
-------------- -------------- 

===================================
-------------- -------------- 
# ¿Cómo iniciar un proyecto de software con éxito?

Iniciar un proyecto de software es una tarea que va más allá de solo tener una gran idea. Necesita de planificación, estructura y una comunicación eficiente para asegurar el éxito a largo plazo. Uno de los primeros pasos cruciales es entender la arquitectura y conformar un equipo de trabajo ideal. Un proyecto exitoso se construye desde sus cimientos, comenzando por una estructura bien definida que facilite la comunicación y colaboración entre las distintas partes involucradas.

## ¿Cuál es el papel del arquitecto y el dueño del proyecto?

Los roles de arquitecto y dueño del proyecto son clave en el desarrollo de software. El arquitecto se encarga de diseñar la estructura del sistema, asegurando que todas las piezas encajen y se comuniquen de manera efectiva. Por otro lado, el dueño del proyecto mantiene la visión y los objetivos en línea y accede al sistema desde una perspectiva global, asegurando que todas las partes están trabajando hacia el mismo fin.

- **Arquitecto**: Define la estructura y facilita la comunicación entre las piezas del sistema.
- **Dueño del proyecto**: Mantiene la visión general y objetivos del proyecto, asegurando la alineación del equipo.

## ¿Cómo se forma y se organiza el equipo de trabajo?

La formación de un equipo de trabajo es un proceso dinámico que se adapta a las necesidades del proyecto. Al principio, el equipo puede ser pequeño, pero a medida que el proyecto crece, es probable que deban añadirse más miembros y roles de liderazgo. Con el crecimiento del equipo, también aumenta la complejidad de la comunicación y la coordinación, lo que a veces puede requerir una reestructuración.

Para mantener la eficiencia y claridad en la comunicación, es común dividir a los miembros en sub-equipos según sus responsabilidades.

- **Estructura de comunicación inicial**: Todo el equipo trabaja unido, favoreciendo un entorno de comunicación simple, pero monolítico.
- **Crecimiento y complejidad**: Con más miembros surgen nuevos roles y la estructura de comunicación se vuelve más compleja.
- **Organización en equipos separados**: La creación de sub-equipos que se comunican entre ellos y mantienen una vía de comunicación formal entre sí puede facilitar la gestión y avanzar hacia una comunicación distribuida.

## ¿Qué es la ley de Conway y cómo afecta a la estructura del proyecto?

La ley de Conway es una observación sobre cómo las organizaciones tienden a producir diseños de sistemas que son copias de las estructuras de comunicación de esas organizaciones. Esto implica que si tu organización tiene una estructura de comunicación definida, es probable que los sistemas que desarrolles sigan esa misma estructura.

Al dividir a la organización en equipos independientes, puede lograrse una aplicación distribuida, donde cada equipo se vuelve autónomo en su parte de la aplicación y se asegura una comunicación más clara entre sistemas.

## ¿Cuáles son los beneficios de una estructura distribuida?

Esencialmente, una estructura distribuida puede ofrecer múltiples beneficios:

- **Escalabilidad y flexibilidad**: Permite que cada equipo sea responsable de una parte del sistema, lo que facilita ajustar o escalar esa parte cuando sea necesario.
- **Eficiencia en el desarrollo**: Equipos autónomos pueden innovar y mejorar su sección del sistema sin esperar al alineamiento o permisos del resto de la organización.
- **Reducción de problemas de comunicación**: Al tener claras vías de comunicación, los equipos evitan malentendidos y logran una mejor coordinación.
- **Adaptación al cambio**: Proveer a la organización la habilidad de responder más ágilmente a las demandas del mercado o a cambios tecnológicos.

Empezar bien un proyecto y saber gestionarlo adecuadamente a lo largo del tiempo marca la diferencia. Al estructurar los equipos y entender las comunicaciones internas, no solo se mejora el producto final, sino que también se enriquece el entorno de trabajo, promoviendo una cultur organizacional sólida.

==================================
-------------- -------------- 
# ¿Cómo separar correctamente el problema de la solución en los requerimientos?

Identificar y separar el problema de la solución es esencial para el desarrollo exitoso de un proyecto. Al enfrentar un nuevo desafío, es crucial no confundir los elementos tecnológicos, como la plataforma o la arquitectura, con el problema en sí mismo. En su lugar, debemos centrarnos en entender la idea central y qué es lo que realmente se quiere resolver. Un ejemplo clásico de este enfoque es **Airbnb**. Su propósito es facilitar el hospedaje al conectar a turistas con propietarios que tienen espacios disponibles, rompiendo así el monopolio que tenían las cadenas hoteleras.

## ¿Qué estrategias usan empresas como Airbnb para identificar problemas?

Airbnb constituye un excelente ejemplo de cómo abordar un problema de manera efectiva. Se enfocan en el problema principal: ofrecer una alternativa más económica, divertida y culturalmente rica a los hoteles tradicionales. Esto se logra al no centrarse directamente en el software, sino en comprender las necesidades del usuario y cómo estas se pueden cubrir con la idea propuesta. En este sentido, imaginarse las **historias de los usuarios** es clave para entender cómo interactuarán con el sistema a futuro.

## ¿Cuál es el papel de las historias de usuario?

Las **historias de usuario** son narrativas que describen cómo un usuario típico interactuaría con una solución para cubrir una necesidad o resolver un problema. En el caso de Airbnb, una historia podría ser la de un turista que desea hospedarse en un lugar más económico y culturalmente enriquecedor que un hotel promedio. Estas historias ayudan a identificar características del problema, como el **trato impersonal de los hoteles** y la **falta de conexión cultural**.

## ¿Cómo se aborda el espacio de la solución?

Una vez que hemos identificado claramente el problema, podemos pasar al **espacio de la solución**. Aquí es donde se empiezan a definir los detalles técnicos que permitirán implementar la idea. Este proceso incluye:

- **Desarrollo**: Creación del software que dará vida a la solución.
- **Diseño**: Planificación de la estructura y funcionalidades del software.
- **Evaluación**: Pruebas y análisis del software para asegurar su efectividad.

## ¿Cómo establecer criterios de aceptación del software?

Para asegurar que el software desarrollado está alineado con el problema identificado, se deben definir **criterios de aceptación** claros. Estos criterios especifican cómo sabemos que el software resuelve el problema de manera efectiva. Además, es crucial garantizar que todas las historias de usuario previstas en la fase inicial se puedan llevar a cabo sin inconvenientes.

## ¿Por qué es importante cerrar el ciclo de feedback?

El **ciclo de feedback** permite entender cómo los usuarios interactúan con el sistema una vez implementado. Esto se logra mediante el uso de **métricas, alertas y logs**, asegurando que el sistema esté disponible y los usuarios tengan acceso continuo. A través de esta retroalimentación, se pueden hacer ajustes que mejoren la experiencia de usuario y optimicen la solución.

## Resumen de la importancia de separar el problema de la solución

En resumen, **separar el problema del espacio de la solución** nos permite entender mejor qué vamos a resolver, sin perdernos en los detalles técnicos prematuros. Al enfocar nuestros esfuerzos en comprender las necesidades y problemas del usuario, podemos desarrollar **soluciones tecnológicas más efectivas** y que verdaderamente añadan valor. 

Este proceso, reflejado en el ejemplo de Airbnb, nos enseña que un análisis y división claros pueden ser la clave para lograr productos que **satisfagan las expectativas del usuario** y resuelvan problemas reales.

===================================
-------------- requerimientos -------------- 
# Análisis de Requerimientos del Sistema

Una vez que entendemos el **espacio del problema** y el **espacio de la solución**, podemos analizar los **requerimientos** de nuestro sistema.

## Requerimientos de Producto

Podemos dividir los requerimientos de producto en **tres capas**:

1. **Capa de Requerimientos de Negocio**  
   Son las reglas del negocio que alimentan los requerimientos del producto.

2. **Capa de Usuario**  
   Relacionada con la experiencia del usuario, define cómo se desenvuelve en el sistema y qué atributos deben priorizarse.

3. **Capa Funcional**  
   Se basa en los requerimientos del sistema y define qué procesos deben ejecutarse operativamente.  
   - Esta capa puede verse afectada por **restricciones** que impactan su funcionamiento.

## Requerimientos de Proyecto

Estos requerimientos están más ligados a la **gestión del proyecto** y se utilizan para dar prioridad a los requerimientos del producto.  

Los **requerimientos de producto y proyecto** trabajan en conjunto para establecer las prioridades del equipo de trabajo.

## Tipos de Requerimientos de Producto

### Requerimientos Funcionales  
Se relacionan con las **historias de usuario**, describiendo específicamente las acciones del sistema.  
**Ejemplo:** Un usuario debe poder iniciar sesión en el sistema.

### Requerimientos No Funcionales  
Añaden **cualidades** al sistema, como seguridad, rendimiento o accesibilidad.  
**Ejemplo:** El inicio de sesión debe realizarse de manera segura.

---
Este enfoque nos permite estructurar claramente los requerimientos para garantizar un desarrollo eficiente y alineado con las necesidades del negocio y los usuarios.

===================================
-------------- Riesgos -------------- 
¿ que pasaria se fracasamos ?

# Gestión de Riesgos en Arquitectura de Software

Los **riesgos** son fundamentales para priorizarlos y atacarlos en orden, asegurando que las **soluciones arquitectónicas** resuelvan los problemas más críticos.

## Cómo Identificar los Riesgos  

Es importante analizar los riesgos desde distintos ángulos, considerando posibles **escenarios de fracaso** y sus consecuencias en caso de que el riesgo se materialice.  

Algunas fuentes clave de riesgo incluyen:

- **Toma de Requerimientos** → **Dificultad / Complejidad**  
  - Riesgos asociados a la ambigüedad o falta de claridad en los requerimientos.  

- **Atributos de Calidad** → **Incertidumbre**  
  - Cuanto mayor es la incertidumbre en un atributo de calidad (rendimiento, escalabilidad, seguridad), mayor es el riesgo.  

- **Conocimiento del Dominio** → **Riesgo Prototípico**  
  - Son riesgos comunes en el dominio del problema y pueden abordarse con soluciones estándar.  

## Priorización de Riesgos  

Una vez identificados los riesgos, el siguiente paso es **priorizarlos**.  

⚠️ **No es necesario mitigar todos los riesgos**, sino centrarse en aquellos que realmente pueden comprometer la **viabilidad de la solución**.  

El objetivo es tomar **decisiones estratégicas** que maximicen el valor del sistema sin perder eficiencia en la gestión de riesgos.  

===================================
===================================
-------------- Restricciones -------------- 
Las restricciones en el contexto de un proceso de desarrollo de software se refiere a las restricciones que limitan las opciones de diseño o implementaciones disponibles al desarrollar.

Los SH nos pueden poner limitaciones relacionadas con su contexto de negocio, limitaciones legales.

También hay limitaciones técnicas relacionadas con integraciones con otros sistemas.

El ciclo de vida del producto va a agregar limitaciones al producto, por ejemplo a medida que avanza el proceso de implementación el modelo de datos va a ser más difícil de modificar.

El arquitecto debe balancear entre los requerimiento y las restricciones.

-------------- -------------- 

===================================
-------------- Arquitectura, panorama y definición -------------- 
# Arquitectura, Panorama y Definición

## ¿Cuál es el panorama actual de la arquitectura de software?
La arquitectura de software es un campo en constante evolución, lleno de librerías, frameworks y conocimientos arquitectónicos implícitos en diferentes comunidades.  
Por ejemplo, términos como **MVC (Modelo-Vista-Controlador)** o **Flux con React** son parte del lenguaje arquitectónico moderno, aunque su aplicación puede no ser universal para todas las tecnologías.  

Este vasto conocimiento implícito a menudo puede llevar a suposiciones, como la idea de que los proyectos deben comenzar con una arquitectura de **microservicios** simplemente porque es la tendencia, sin un análisis profundo de los compromisos o beneficios específicos que ofrece.

---

## ¿Qué es un estilo de arquitectura?
Un **estilo de arquitectura** en software es un conjunto de decisiones de diseño que, dados ciertos contextos, proporcionan restricciones beneficiosas a las decisiones arquitectónicas futuras.  

Por ejemplo, al hablar de **páginas web**, todas comparten la estructura **cliente-servidor**, donde un navegador web interactúa con un servidor para obtener documentos HTML. Este patrón genérico define un estilo de arquitectura que se enfoca más en los problemas arquitectónicos a nivel de **conectores entre aplicaciones**, como las comunicaciones entre un navegador y un servidor o entre una aplicación móvil y una API.

---

## Importancia y aplicación de los estilos de arquitectura
Los **estilos de arquitectura** son esenciales para **reutilizar exitosamente soluciones pasadas** en nuevos contextos similares.  

Al aplicar un estilo de arquitectura:
- **Reutilizamos conocimiento previamente probado.**
- **Aprovechamos restricciones y decisiones ya tomadas en base a implementaciones anteriores.**  
- **Optimizamos las decisiones arquitectónicas para objetivos específicos.**

---

## Ejemplos y beneficios de los estilos de arquitectura
A continuación, se presentan algunos estilos de arquitectura comunes y sus beneficios:

1. **Cliente-Servidor**  
   - Facilita la interacción de aplicaciones como navegadores web con servidores.  
   - Permite la carga dinámica de contenido desde el servidor al cliente.  

2. **Microservicios**  
   - Fomenta la escalabilidad y la modularidad del sistema.  
   - Requiere un análisis detallado de sus beneficios y trade-offs en relación con la tecnología específica del proyecto.  

3. **Red de pares (Peer-to-Peer)**  
   - Facilita la comunicación directa entre dos sistemas.  
   - Útil en aplicaciones descentralizadas como redes P2P o blockchain.  

---

## Conclusión
Los **estilos de arquitectura** ofrecen una estructura sólida y adaptable que puede resultar en soluciones eficientes y escalables.  
Es fundamental **considerar los contextos específicos** y las particularidades de cada proyecto antes de elegir un estilo arquitectónico.  

Así, tomamos **decisiones informadas** que **maximizan el éxito** de nuestros sistemas.

===================================
-------------- Arquitectura, panorama y definición -------------- 

===================================
-------------- Arquitectura, panorama y definición -------------- 

===================================
-------------- Arquitectura, panorama y definición -------------- 











===================================
===================================
===================================
===================================
===================================
===================================
===================================
===================================
===================================


