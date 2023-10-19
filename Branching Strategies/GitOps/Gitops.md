**¿Ques es GitOps?**

GitOps es estrategia de branching que utiliza Git como fuente única de verdad para ofrecer una infraestructura como código.
Se basa en la idea de que todo lo relacionado con la infraestructura y las aplicaciones debe representarse en repositorios Git. 
Esta orientado principalmente en la gestion de clusters de kubernetes aunque la comunidad aplica y publica soluciones de GitOps en otros sistemas distintos de Kubernetes.
Se basa en que los cambios que se implementan durante el ciclo de vida de la aplicación se registran en el repositorio de Git y se pueden auditar. Los cambios en el código activan unas acciones automatizadas que despliegan esos cambios en el entorno de destino, lo que facilita el mantenimiento y la coherencia en los entornos de desarrollo, pruebas y producción.  

En cuanto a los equipos de operaciones, el hecho de que puedan obtener información sobre los cambios implica que les será posible rastrear y solucionar los problemas con rapidez para mejorar la seguridad general. Los registros de auditoría actualizados permiten que las empresas reduzcan el riesgo de enfrentarse a cambios no deseados y los corrijan antes de que lleguen a la etapa de producción. 

**Principios Fundamentales**

1. Declaratividad: Las especificaciones de la infraestructura y las aplicaciones se almacenan en Git como código. Por lo general, la IaC utiliza un enfoque declarativo para gestionar la infraestructura, es decir, define el estado deseado del sistema y realiza un seguimiento del estado actual. 
2. Automatización: Los cambios se aplican automáticamente en el entorno objetivo en función de lo que está definido en Git. Por lo general, los canales de CI/CD se activan por eventos externos, como la inserción de un código en un repositorio. En un flujo de trabajo de GitOps, los cambios se realizan utilizando solicitudes de incorporación de cambios, las cuales modifican el estado en el repositorio de Git. 
3. Reconciliación Continua: El estado real se compara con el estado deseado y se toman medidas para que coincidan.
Cambio solo por solicitud: Para implementar una nueva versión mediante un flujo de trabajo de GitOps, se debe realizar una solicitud de incorporación de cambios en Git, que modifica el estado declarado del clúster. De esta forma se evitan cambios manuales que no puedan ser rastreados.

Si utiliza solicitudes de incorporación de cambios y sistemas de control de versiones, como Git, obtendrá un panorama completo del proceso de implementación: visualizará y rastreará los cambios que se realizaron en el sistema, obtendrá un registro de auditoría, y podrá revertir los cambios si algo sale mal.

**Ventajas** 

1. Consistencia: Los entornos se mantienen consistentes ya que se basan en declaraciones codificadas.
2. Seguridad: Los cambios pasan por revisión y control de versiones en Git antes de implementarse.
3. Rastreabilidad: Todas las modificaciones están documentadas en el historial de Git.
4. Colaboración: Varios equipos pueden trabajar en paralelo en la misma infraestructura y aplicaciones.
5. Recuperación ante fallos: Se puede revertir fácilmente a un estado anterior en caso de problemas.

Con GitOps, las organizaciones pueden gestionar toda su infraestructura y el ciclo de desarrollo de aplicaciones utilizando una única herramienta unificada. Esto permite una mayor colaboración y coordinación entre los equipos y resulta en menos errores y una resolución de problemas más rápida.

Además, GitOps puede ayudar a las organizaciones a aprovechar los contenedores y microservicios y mantener la consistencia en toda su infraestructura, desde las configuraciones de clúster Kubernetes y las imágenes Docker hasta las instancias en la nube y cualquier recurso en local.

Los flujos de trabajo de GitOps pueden aumentar la productividad y la velocidad del desarrollo y de las implementaciones y, al mismo tiempo, mejorar la estabilidad y fiabilidad de los sistemas.

**Como usar GitOps**

GitOps no es un único producto, complemento o plataforma. No existe una respuesta única para esta pregunta, ya que la mejor manera de implementar GitOps variará según las necesidades y objetivos específicos del equipo. Sin embargo, algunos consejos sobre cómo comenzar con GitOps incluyen el uso de un repositorio de GitOps dedicado para que todos los miembros del equipo compartan configuraciones y código, la automatización de la implementación de cambios de código y la configuración de alertas para notificar al equipo cuando se produzcan cambios.

Existe un flujo basico que consite en los siguientes puntos.

1. Almacenamiento y definicion de infrastructura: Las especificaciones de infraestructura y aplicaciones se definen como código y se almacenan en un repositorio Git. El primer paso en la implementación de GitOps es definir el estado deseado de la infraestructura como código. Esto implica identificar los componentes de la infraestructura, como servidores, bases de datos y balanceadores de carga, y definir sus configuraciones como código. 
2. Merge Request:  GitOps utiliza solicitudes de extracción (MRs) como el mecanismo de cambio para todas las actualizaciones de infraestructura. Una confirmación de fusión se realiza en su rama principal (o trunk) y sirve como un registro de auditoría. Una vez aprobados, los cambios se fusionan en la rama principal del repositorio.
3. Automatización: El siguiente paso es configurar las acciones automatizadas necesarias que recuperen la última versión del código de Git, la prueben y la desplieguen en el entorno de destino.   GitOps automatiza las actualizaciones de infraestructura mediante un flujo de trabajo de Git con integración continua y entrega continua (CI/CD). Cuando se fusiona nuevo código, el pipeline de CI/CD implementa el cambio en el entorno. Cualquier desviación de configuración, como cambios manuales o errores, se sobrescribe con la automatización de GitOps, de modo que el entorno converge hacia el estado deseado definido en Git. GitLab utiliza pipelines de CI/CD para gestionar e implementar la automatización de GitOps, pero también se pueden utilizar otras formas de automatización, como operadores de definiciones.
4. Reconciliar: El estado real se compara con el estado deseado. Si hay discrepancias, se toman medidas para remediarlas.
5. Auditoria: Una vez desplegada la infraestructura, es importante supervisarla y auditar los cambios para garantizar el cumplimiento de los requisitos normativos.

Como conclusion podemos resumirlo en estos cuatro puntos

1. El repositorio Git es la fuente de verdad para la configuración y el código de la aplicación.
2. El pipeline de CD es responsable de construir, probar y desplegar la aplicación.
3. La herramienta de despliegue se utiliza para gestionar los recursos de la aplicación en el entorno de destino.
4. El sistema de monitoreo realiza un seguimiento del rendimiento de la aplicación y proporciona retroalimentación al equipo de desarrollo.

**Cuándo Escoger GitOps**

GitOps es adecuado cuando se busca una automatización continua y segura de la infraestructura y las aplicaciones.
Es especialmente beneficioso en entornos de equipos distribuidos y en el despliegue de microservicios.
Despliegues de Aplicaciones: Implementación continua y controlada de aplicaciones en múltiples entornos.
Infraestructura como Código: Creación y gestión automatizada de recursos de infraestructura.
Recuperación ante Desastres: Restaurar rápidamente entornos a estados anteriores conocidos.
Escalar Horizontalmente: Añadir o quitar recursos según la demanda.

**Herramientas Populares**

1. ArgoCD: Una herramienta de GitOps de código abierto para el despliegue y gestión de aplicaciones en Kubernetes.
2. Flux: Otra herramienta de GitOps que automatiza las implementaciones en clústeres Kubernetes.
3. Jenkins X: Extiende Jenkins para proporcionar CI/CD en entornos de Kubernetes.

**Ejemplo** 

En un escenario de GitOps, un equipo identifica problemas en el rendimiento debido a una configuración incorrecta de un equilibrador de carga en su infraestructura. Utilizan un repositorio de GitOps para gestionar la configuración de la infraestructura. Luego, siguen estos pasos:

1. Encuentran y ajustan la configuración incorrecta en el repositorio de GitOps. (Infrastructura como codigo de forma declarativa)
2. Inician una solicitud de cambios para optimizar la configuración y otro miembro del equipo la revisa y aprueba. (Merge Request Approach)
3. La solicitud se fusiona en el repositorio, lo que activa un pipeline de GitOps. (Automatización de revisión y despliegue)
4. El operador de GitOps detecta el cambio y actualiza automáticamente la configuración del equilibrador de carga en el clúster. (Reconciliacion del estado)
5. El equipo monitorea el sistema para asegurarse de que vuelva a funcionar correctamente. (Auditoria)

En otro escenario, el equipo decide reemplazar completamente el equilibrador de carga debido a fallos fundamentales. Siguen un proceso similar:

1. Crean una solicitud de cambios para introducir una nueva configuración de equilibrador de carga y eliminar la anterior.
2. La solicitud se aprueba y se implementa.
3. Descubren que la nueva configuración causa problemas graves y detiene las operaciones de los usuarios.
4. Utilizan GitOps para revertir rápidamente a la configuración anterior, restaurando la funcionalidad conocida.
5. Una solicitud de cambios adicional revierte la configuración en el repositorio, y GitOps la implementa automáticamente, mejorando la infraestructura y la fiabilidad del equipo.

En ambos casos, GitOps permite a un equipo gestionar cambios en la infraestructura de manera controlada y revertir rápidamente los cambios problemáticos para mantener la estabilidad y el rendimiento del sistema.

**Conclusion**

GitOps es una metodología poderosa que combina la automatización y la gestión basada en Git para agilizar el desarrollo y las operaciones.
Ofrece ventajas en términos de consistencia, seguridad y colaboración, siendo útil en una variedad de casos, desde despliegues de aplicaciones hasta la gestión de infraestructura.

El uso de un sistema de control de versiones permite que un equipo realice un seguimiento de todas las modificaciones en la configuración de un sistema. Esto proporciona una "fuente de verdad" y un valioso registro de auditoría para revisar si algo se rompe o se comporta de manera inesperada. Los equipos pueden revisar el historial de GitOps y ver cuándo se introdujo una regresión. Además, este registro de auditoría se puede utilizar como referencia para auditorías de cumplimiento o seguridad. El historial de GitOps se puede utilizar como prueba cuando se modifican o actualizan cosas como certificados de cifrado.

GitOps puede aumentar significativamente la productividad de un equipo de DevOps. Les permite experimentar rápidamente con nuevas configuraciones de infraestructura. Si los nuevos cambios no se comportan como se esperaba, un equipo puede utilizar el historial de Git para revertir los cambios a un estado conocido y válido. Esto es increíblemente poderoso, ya que habilita la funcionalidad familiar de "deshacer" en una infraestructura complicada.

**Referencias**

https://www.redhat.com/es/topics/devops/what-is-gitops
https://www.ilimit.com/blog/gitops/
https://www.atlassian.com/es/git/tutorials/gitops
https://www.linkedin.com/pulse/qu%C3%A9-es-gitops-y-por-importante-en-las-empresas-angel-rengifo-cancino/?originalSubdomain=es