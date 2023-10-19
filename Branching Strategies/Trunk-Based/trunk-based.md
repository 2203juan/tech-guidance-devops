# Trunk base
Cuando abordamos las estrategias de branching, nos encontramos con diversas variantes, cada una adaptada a las necesidades específicas de los equipos de desarrollo. Sin embargo, una recomendación crucial es no adoptar una estrategia solo porque otro equipo la esté utilizando con éxito. Cada equipo tiene su propia idiosincrasia: clientes con requerimientos únicos, tamaños de equipos o de pruebas que varían, ausencia de roles esenciales y un sinfín de variables que complejizan la elección de la estrategia de branching adecuada. En este contexto, nos centraremos en la estrategia "Trunk Based", evaluando sus pros y contras para permitirte no solo entenderla, sino también determinar si es la elección óptima para tu proyecto.
 
## ¿Qué es Trunk Based?
 
"Trunk Based" es una estrategia de branching que utiliza un tronco ("main" o "master") como la rama principal. En esta rama, todo el equipo integra cambios de forma constante, sin recurrir a ramas de larga duración. Aunque esta metodología posibilita entregas más frecuentes de código, su implementación exige consideraciones específicas.
 
## Consideraciones para usar Trunk Based
 
### Entregas Constantes de Código Funcional:
 
En el enfoque Trunk Based, todo lo que se entrega debe estar exhaustivamente probado. En muchos proyectos, incluso se despliega directamente a producción desde el tronco, lo que implica una mayor responsabilidad para los desarrolladores y revisores. Asimismo, obliga a los equipos de infraestructura a proporcionar herramientas sólidas para las pruebas, ya que la falta de ellas dificultaría la validación y aumentaría el riesgo de impactar otros componentes.
 
### Ausencia de Ramas de Larga Duración:
 
En repositorios que siguen la estrategia Trunk Based, generalmente encontrarás dos ramas: "release" y "main" o "master". Las ramas de características ("feature") solo deberían estar abiertas mientras estén siendo desarrolladas. En cuanto a las ramas de "release", su existencia puede depender de decisiones del equipo o cliente, como lanzamientos de pruebas de rendimiento o liberaciones a entornos inferiores antes del despliegue a producción.
 
### Validación y Pruebas:
 
La labor de los revisores y de las pruebas automatizadas es esencial para habilitar o bloquear las entregas en función de la calidad del código. Esto resalta la necesidad de que los equipos que emplean Trunk Based sean maduros y experimentados, ya que esta estrategia exige un alto nivel de destreza en comparación con otras metodologías de branching.
 
 
### Mantener un Historial de Commits Limpio:
 
Dado que Trunk Based promueve entregas pequeñas y constantes de código probado, se enfoca en evitar ensuciar el tronco con commits posteriores que corrijan errores menores o realicen hotfixes. Este enfoque se deriva de la intención de mantener la integridad del tronco para futuras validaciones o circunstancias que requieran revertir cambios.
 
### Trabajo en equipos pequeños o grandes pero granularmente:
 
Debido a la velocidad de los cambios es recomendable que los equipos que trabajan en trunk based sean pequeños, o si son equipos grandes deberían trabajar granularmente, es decir, pocas personas iterando entre los diferentes componentes. Al contar con quipos más pequeños es más fácil comunicarse de manera más efectiva y ágil. Algunos prouyectos siguen la "regla de las dos pizzas", que sugiere que un equipo debe ser lo suficientemente pequeño como para alimentarse con solo dos pizzas.
 
### Condiciones regulatorias o de UX del cliente:
 
Trunk based es una estrategia que permite la inserción de cambios constantes a los diferentes ambientes, incluso los productivos, sin embargo, esto no necesariamente es positivo para todas las industrias, por ejemplo, algunas empresas tienen condiciones regulatorias en las que las salidas a producción deben ser auditadas y monitoreadas por personas, incluso por terceros, en este caso no es posible hacer despliegue continuo a ambientes productivos. Por otro lado, desdel el punto de vista de UX, insertar cambios constantes en una aplicación productiva puede generar malestar en los usuarios, ya que sus hábitos de usabilidad pueden verse alterados fácilmente, es decir, si un botón cambia de lugar constantemente debido a la velocidad en el despliegue de nuevas actualizaciones, puede ser confuso para el usuario identificar donde y cuando se dan estos cambios.
 
### Tooling:
 
Cuando utilizas trunk based necesitas tener un ecosistema de herramientas que te permitan hacer una entrega de calidad y no solo en términos de código, sino también en términos de velocidad, identificación de fallos, tests de seguridad, análisis de dependencias y automatización. Esto debido a que la idea de utilizar trunk based es hacer entregas constantes y eficientes, por lo cual contar no contar con las herramientas necesarias dificultará estas entregas.
 
## Ventajas de Utilizar Trunk Based
 
### Feedback en Tiempo Real:
 
Con herramientas adecuadas y la obligación de contar con código funcional en el tronco, se garantiza que todo sea probado antes de integrarse.
 Visibilidad para Todo el Equipo: Todos los miembros deben involucrarse en la validación del código, fomentando una comprensión colectiva de las contribuciones.
 
### Integración Continua:
 
Todo lo integrado en el tronco debe ser desplegado en un entorno, reforzando la práctica de la integración continua.
 Resolución Ágil de Problemas: La constante funcionalidad del tronco convierte a los errores en una prioridad constante, acelerando su resolución.
 
## Analicemos el siguiente caso:
 
En el "Proyecto Aurora", se desarrolla una aplicación de importancia crítica para varias empresas de servicios financieros llamada "TheGreattestFinancialApp". Esta aplicación se encarga de gestionar millones de transacciones financieras diarias en los Estados Unidos y debido a esto, está sujeta a rigurosas regulaciones de supervisión por parte de organismos como la FINRA, la SEC y la CFTC. Además de cumplir con estas regulaciones, la aplicación también debe mantener altos estándares de calidad ya que cuenta con certificaciones importantes, como SOC, HIPAA e ISO 27001, para garantizar la seguridad y la integridad de los datos financieros que maneja.
 
El equipo responsable de "TheGreattestFinancialApp" está en una etapa de consolidación después de más de una década en el mercado. Con un flujo constante de capital y una amplia experiencia, este equipo está formado por un equipo de más de cien desarrolladores con diferentes niveles de seniority, especialistas en calidad, analistas de seguridad y expertos en finanzas, la mayor parte de estos distribuída en equipos OffShore provistos por 5 partners tecnológicos. La distribución geográfica y las diferentes zonas horarias en las que operan los miembros del equipo son un testimonio de su alcance global y su capacidad para ofrecer soluciones de software de alta calidad.
 
Sin embargo, a pesar de su éxito y experiencia, el proceso de despliegue de la aplicación ha sido un desafío constante. Las implementaciones a producción son notoriamente complicadas, requieren aproximadamente ocho horas de operaciones manuales. Estas tareas manuales incluyen la carga de artefactos, la reinicialización de instancias, la modificación de archivos de configuración y la purga de la caché de servidores. Los clientes, que dependen de la aplicación las 24 horas del día, los 7 días de la semana, han expresado su frustración por estos tiempos de inactividad.
 
Desde el punto de vista de la arquitectura, la aplicación se basa principalmente en un enfoque monolítico, dividido en siete repositorios que abarcan desde los componentes de la interfaz de usuario hasta la infraestructura y el monolito central, además de algunos submódulos adicionales. El equipo de infraestructura, compuesto por seis ingenieros expertos en administración de sistemas, ha estado realizando operaciones manuales durante todo este tiempo. Sin embargo, recientemente, han iniciado un esfuerzo para modernizar la infraestructura y adoptar la automatización e Infraestructura como Código (IaC). Esto representa un cambio significativo en su enfoque, ya que anteriormente se basaban en componentes estáticos.
 
Con el objetivo de abordar los desafíos existentes y mejorar la eficiencia del desarrollo y los despliegues, el equipo de infraestructura propone una transición hacia una estrategia de "trunk based development" (desarrollo basado en tronco). Este enfoque implica una transición gradual durante un mes, durante el cual se capacitará a los desarrolladores en las mejores prácticas de integración con el tronco y se establecerá un marco de trabajo sólido para garantizar que las entregas constantes de código se realicen de la manera más eficiente posible.
 
El líder técnico del equipo de infraestructura expresó su confianza en esta transición, afirmando: "En un mes, estaremos completamente migrados a un enfoque trunk based, lo que facilitará enormemente el proceso de implementación y mejorará la eficiencia en general." Este cambio promete simplificar las operaciones de despliegue y permitir entregas más rápidas y seguras, lo que es esencial en un entorno financiero altamente competitivo y regulado como el de "TheGreattestFinancialApp".
 
¿Qué opiniones pueden quedar de la implementación que se está haciendo en TheGreattestFinancialApp?
 
 
___AQUI AMIGUITOS QUIERO QUE PONGAN SUS CONSIDERACIONES PARA PODER ALIMENTAR ESTE DOCUMENTO, PUEDEN SER BULLETS, YO TENGO ALGUNAS PERO NO QUIERO CESGARLOS___
