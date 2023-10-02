¿Qué es Github flow?

 
Es una de las estrategia de branching mas sencillas, consistiendo unicamente de una rama principal (_master_ o _main_), la cual representa el codigo productivo. El equipo de desarrollo abre ramas basadas en _master_ en las cuales se trabajan las historias de usuario antes de ser nuevamente integradas en la rama _master_.
 

Consideraciones para usar Github flow


Entregas constantes de código funcional:

Github flow hace uso de su simplicidad en los procesos de integramiento de desarrollos para acortar los ciclos producción, permitiendo que puedan existir varios despliegues al cabo de un solo dia. En consecuencia el proceso de desarrollo, pruebas, revision debe de ser tan eficiente como la planeacion de los procesos de entrega.


Unica rama de larga duración:

Los proyectos que siguen una metodologia Github flow, deben de mantener minima la cantidad de ramas activas en cada uno de sus repositorios para asi poder evitar conflictos entre los desarrollos; la unica rama que debe de persistir en el tiempo debe de ser la rama principal. Cada vez que una rama de desarrollo es cerrada debe de realizarse el proceso de CD, en el cual se ejecute el versionamiento y se borre la rama, lo cual evita la existencia de ramas _release_. Adicionalmente, las ramas de _hotfix_ son tratadas como ramas de desarrollo. 
 

Validación y Pruebas:

El modelo Github plantea la realizacion de pruebas y aseguramiento de calidad en las ramas de desarrollo antes de realizar alguna accion con la rama principal, esto con el motivo de mantener la rama principal limpia segun los casos de prueba que se realicen. Hay que tener en cuenta que la automatizacion de estas pruebas es vital para un flujo continuo y que no sea necesario la espera de una validacion manual, la cual puede tardar segun el caso
 

Trabajo en equipos pequeños o grandes pero granulares:

La falta de ramas que sirvan como intermediarios en el proceso de desarrollo como lo son las ramas _release_, _staging_, o _develop_ en otras estrategias de branching hace que el trabajo deba de ser granulado para evitar conflictos al momento del desarrollo. El trabajo del equipo debe de estar mediado siempre por la comunicacion y el estar atento que las ramas de desarrollo deben de ser efimeras. 


Ventajas de utilizar Github flow:

 - _Feedback_ en tiempo real por parte de los clientes, ya que el codigo llega al ambiente productivo rapidamente.
 - Facilidad en integración y despliegue continuo debido a la rapidez del proceso de verfiicacion de codigo.
 - Facil de entender e implementar sin importar el grado de expertice del equipo.
 - Es una estrategia facilmente mantenible como consecuencia de las ramas efimeras de desarrollo.
 - Ciclos productivos constantes.
 - Facilita los procesos de resolucion de problemas productivos y la identificacion de _bugs_.

Desventajas de utilizacion Github flow:
 - No es aconsejable el uso de otros tipos de ramas para preservar su sencillez.
 - El desarrollo tiene que ser atomico (es productivo o no se usara).
 - En caso de necesitar certificaciones puede llegar a ser dificil la coordinación por los tiempos que pueden tomar estos.
 - Depende de la velocidad que el equipo pueda desarrollar los procesos para ser una estrategia efectiva.
 - No se pueden probar multiples desarrollos en conjunto.
