# Branching strategies 

## INTRODUCCION

El mundo del desarrollo se basa en colaboracion e innovacion, en donde muchos desarrolladores de software necesitan colaborar para gestionar de forma eficiente y productiva nuevas funciones que se quieran implementar en el proyecto. Aquí es donde entran en juego las "branching strategies" o estrategias de ramificación.

Las estrategias de remificacion es la guia en la cual nos dice cuando y como se tiene que hacer una integracion del nuevo codigo a la rama principal. Esto da el espacio para que cada programador tenga su propia autonomia y haga los cambios necesarios en su rama para despues cuando finalize el ciclo de su funcion sea integrado a la rama con master. 

Si pensamos en la estrategia de ramificacion como si fuera arquitectura, cada desarrollador es encargado de realizar un area de la construccion total, al finalizar el ciclo todas las tareas de cada desarrollador debe de ir en el plano principal y cada parte debe de encajar sin tener conflictos con lo que los otros hicieron. De esto se trata las estrategias, de poder construir algo en colaboracion con las demas personas sin dañar lo que se tiene. 

## IMPORTANCIA DE LAS BRANCHING STRATEGIES

A continuacion los siguientes puntos son aquellos los cuales se tiene que tener en cuenta una branching strategy en los proyectos de gestion de software : 
- Gestion Efectiva de versiones : Las estrategias de ramificación permiten gestionar versiones de software de manera eficiente. Al crear ramas específicas para nuevas características o correcciones de errores, se puede trabajar en estas actualizaciones sin afectar la rama principal (trunk). Esto facilita la liberación ordenada de nuevas versiones mientras se mantiene la estabilidad de la versión actual en producción

- Colaboración sin Conflictos : En entornos colaborativos, múltiples desarrolladores pueden trabajar en diferentes características simultáneamente sin interferir entre sí. Cada función puede tener su propia rama, y al final, estas ramas se fusionan de manera controlada, evitando conflictos y asegurando que todos los cambios se integren de manera armoniosa

- Facilita el Despliegue Continuo : Las estrategias de ramificación son esenciales para la implementación continua y la entrega continua (CI/CD). Permiten la automatización de pruebas y despliegues en ramas específicas, asegurando que solo los cambios probados y aprobados se implementen en producción. Esto mejora la velocidad de entrega y reduce el riesgo de errores.

## Metodos de branching : 

### [Trunk Based](https://github.com/2203juan/tech-guidance-devops/blob/gitFlow-alejo/trunk-based/trunk-based.md)

### [GitHub Flow](https://github.com/2203juan/tech-guidance-devops/blob/githubflow-mateo/branching-strategy/Github%20flow/Github%20flow.md)

### [GitHub Flow](https://github.com/2203juan/tech-guidance-devops/blob/GitFlow-juanhoyos/gitflow/gitflow.md)

### [GitOps](https://github.com/2203juan/tech-guidance-devops/blob/gitops-ricardo/branching-strategy/Gitops/Gitops.md)



## Conclusiones Generales

En conclusión, las estrategias de ramificación representan una gran importancia en el desarrollo de software colaborativo. Estas no solo proporcionan una guia para la gestión eficiente de versiones, permitiendo la incorporación ordenada de nuevas funcionalidades sin perturbar la estabilidad de la versión actual, sino que también fomentan la colaboración armoniosa entre múltiples desarrolladores. Al asignar a cada programador la responsabilidad de construir y perfeccionar una parte específica del proyecto, las estrategias de ramificación actúan como el plano principal de una arquitectura, donde cada contribución encaja sin conflictos con el trabajo de los demás. Además, al facilitar el despliegue continuo a través de la automatización de pruebas y despliegues en ramas específicas, estas estrategias mejoran significativamente la velocidad de entrega y reducen el riesgo de errores en el proceso. En resumen, la implementación efectiva de estrategias de ramificación no solo es una práctica esencial para el desarrollo ordenado y colaborativo, sino que también impulsa la eficiencia y calidad en la entrega de software.