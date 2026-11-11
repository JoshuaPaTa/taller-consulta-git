## Parte 1: Contextualización e Investigación

1. **¿Qué es Git y qué problema resuelve en el desarrollo de software?**
    **Git** es un **sistema de control de versiones distribuido** de código abierto, diseñado para rastrear los cambios en el código fuente de un proyecto a lo largo del tiempo. Fue creado por Linus Torvalds en 2005 y se ha convertido en el estándar de la industria para el desarrollo de software.



    ### ¿Qué problemas resuelve en el desarrollo de software?

    Antes de Git (y de los sistemas de control de versiones en general), el desarrollo colaborativo y la gestión de código enfrentaban problemas críticos que Git soluciona de raíz:

    #### 1. El caos de las versiones y nombres de archivos

    * **El problema tradicional:** Era común ver carpetas llenas de archivos con nombres como `app_v1.js`, `app_v2_final.js`, `app_final_corregido_definitivo.js`. Era imposible saber qué cambios exactos se habían hecho entre una versión y otra, o cuál era la última versión real.
    * **Cómo lo resuelve Git:** Mantiene un historial único, ordenado y comprimido de cada modificación. Cada cambio ("commit") registra **quién** lo hizo, **cuándo** se hizo y **por qué**, permitiendo viajar en el tiempo y volver a cualquier estado anterior del proyecto de forma instantánea.

    #### 2. Colaboración en equipo sin pisarse el código

    * **El problema tradicional:** Cuando varios programadores trabajaban en el mismo proyecto, solían enviarse archivos por correo o compartirlos en carpetas de red. Si dos personas modificaban la misma línea de código en archivos separados, el trabajo de uno borraba o sobrescribía el del otro (el clásico problema de sobreescritura).
    * **Cómo lo resuelve Git:** Introduce el concepto de **ramas (branches)**. Cada desarrollador puede trabajar en su propia línea de desarrollo aislada (una rama para una nueva característica, otra para corregir un error) y, al terminar, **fusionar (merge)** sus cambios de forma controlada. Git detecta automáticamente si hay conflictos y ayuda a resolverlos antes de integrar el código.

    #### 3. Miedo a romper el código en producción

    * **El problema tradicional:** Probar una nueva funcionalidad arriesgada a menudo significaba arruinar el sistema funcional que ya estaba funcionando, sin una forma rápida o segura de deshacer los cambios.
    * **Cómo lo resuelve Git:** Permite experimentar con total libertad. Puedes crear una rama de pruebas, romper todo lo que quieras y, si no funciona, simplemente descartarla o volver al estado estable anterior con un solo comando sin afectar el software principal.

    #### 4. Pérdida de datos y falta de respaldos centralizados

    * **El problema tradicional:** Si el disco duro de la computadora principal o del servidor fallaba, todo el historial del proyecto podía perderse para siempre.
    * **Cómo lo resuelve Git:** Al ser un sistema **distribuido**, cada desarrollador que clona el repositorio tiene una **copia completa** de toda la historia del proyecto en su máquina local. Esto significa que cada copia actúa como un respaldo integral y redundante.