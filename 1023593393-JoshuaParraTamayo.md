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

2. **Diferencias clave entre Git y GitHub.** (Expliquen por qué no son lo mismo).

    Aunque a menudo se usan juntos y muchas personas tienden a confundirlos, **Git y GitHub no son lo mismo**. La confusión es normal porque GitHub lleva la palabra "Git" en su nombre, pero cumplen roles completamente diferentes en el ecosistema de desarrollo.

    Diferencias clave y por qué son herramientas distintas:

    ---

    ### Tabla comparativa rápida

    | Característica | Git | GitHub |
    | --- | --- | --- |
    | **¿Qué es?** | Un **software** (una herramienta de línea de comandos). | Una **plataforma web** (un servicio en la nube). |
    | **¿Dónde vive?** | En tu computadora local (es local). | En servidores remotos en internet (en la nube). |
    | **Conexión a internet** | Funciona **sin conexión** a internet. | Requiere **conexión a internet** para usarse. |
    | **Propósito principal** | Rastrear el historial de cambios y gestionar versiones del código. | Alojamiento remoto de repositorios, trabajo en equipo y redes sociales para desarrolladores. |
    | **Creador** | Linus Torvalds (2005). | Microsoft (fundado originalmente por Tom Preston-Werner, Chris Wanstrath y PJ Hyett en 2008; adquirido por Microsoft en 2018). |

    ---

    ### ¿Por qué no son lo mismo? (Explicación detallada)

    #### 1. La naturaleza de cada herramienta (Software vs. Servicio)

    * **Git es la tecnología (el motor):** Es un software libre que instalas en tu sistema operativo. Se ejecuta en tu máquina local para registrar cada línea de código que escribes, permitirte crear ramas, hacer fusiones y viajar en el tiempo a través de tu historial de commits, todo sin necesidad de tocar internet.
    * **GitHub es el espacio de almacenamiento y colaboración (el garaje compartido):** Es una plataforma basada en la nube que toma los repositorios que creas con Git en tu computadora y te permite subirlos (hacer *push*) para guardarlos de forma segura en internet.

    #### 2. Colaboración local vs. Colaboración en la nube

    * **Git** por sí solo es capaz de manejar versiones en tu computadora, e incluso puedes colaborar con otros en una red local. Sin embargo, no provee una interfaz gráfica avanzada para revisar código de terceros ni gestiona perfiles de usuarios globales.
    * **GitHub** amplía las capacidades de Git agregando herramientas de colaboración social y empresarial:
    * **Pull Requests (Solicitudes de extracción):** Permiten proponer cambios y discutirlos línea por línea antes de integrarlos al código principal.
    * **Gestión de proyectos (Issues y Projects):** Tableros estilo Kanban para rastrear tareas, errores y características.
    * **Revisiones de código (Code Review):** Facilitan que otros desarrolladores aprueben o rechacen cambios en equipo.



    #### 3. Dependencia técnica

    * Puedes usar **Git sin GitHub** perfectamente (puedes guardar todo tu código de manera local en tu disco duro).
    * No puedes usar **GitHub sin Git** (GitHub está construido específicamente para almacenar, interpretar y gestionar proyectos que utilizan Git como sistema de control de versiones).

3. **¿Qué es una nube de repositorios?** Expliquen este concepto y mencionen al menos tres alternativas diferentes en el mercado (por ejemplo, además de GitHub, ¿qué otras plataformas existen?).

    Una **nube de repositorios** (también conocida como servicio de alojamiento de código o *Git hosting*) es una plataforma basada en la nube que actúa como un servidor centralizado en internet para almacenar, gestionar y colaborar en proyectos que utilizan Git.

    Mientras que Git vive en tu computadora local, la nube de repositorios permite subir (*push*) tu código para que esté respaldado de forma segura fuera de tu disco duro y accesible para otros desarrolladores desde cualquier parte del mundo. Además de guardar el código, estas plataformas integran herramientas esenciales para el flujo de trabajo moderno, como gestión de tareas (issues), control de acceso por roles, revisión de código, automatización de pruebas (CI/CD) y despliegues automáticos.

    ---

    ### Principales alternativas en el mercado

    Aunque GitHub es la más popular de la industria, existen varias opciones muy potentes que se utilizan ampliamente según las necesidades de los equipos o las empresas:

    #### 1. GitLab

    * **Qué es:** Una plataforma completa de DevOps que ofrece todo en uno (desde la gestión del código fuente hasta la integración continua, entrega continua, seguridad y monitoreo).
    * **Características destacadas:** Es famosa por su potente sistema integrado de **CI/CD** (Integración Continua y Despliegue Continuo) y por ofrecer una versión *Self-Hosted* (puedes instalarla en tus propios servidores locales o privados de forma gratuita con su edición Community).

    #### 2. Bitbucket

    * **Qué es:** La plataforma de alojamiento de Git desarrollada por **Atlassian**, la empresa creadora de herramientas de gestión de proyectos como **Jira** y Confluence.
    * **Características destacadas:** Su mayor fortaleza es la **integración nativa con Jira y Trello**. Si un equipo ya utiliza las herramientas de Atlassian para la gestión ágil de proyectos (Scrum/Kanban), Bitbucket conecta automáticamente los commits, ramas y solicitudes de extracción con las tareas correspondientes.

    #### 3. Azure DevOps (anteriormente Visual Studio Team Services)

    * **Qué es:** La plataforma integral de Microsoft orientada tanto al desarrollo en la nube (con soporte para repositorios Git y Team Foundation Version Control) como a la gestión de ciclos de vida de software corporativo.
    * **Características destacadas:** Está profundamente integrada con el ecosistema de **Microsoft Azure** y herramientas empresariales. Ofrece tableros Kanban muy robustos, gestión de pipelines de despliegue avanzados y un fuerte enfoque en la seguridad y cumplimiento para grandes corporaciones.

4. **Glosario básico:** Definan con sus propias palabras, de forma clara y **agregando un ejemplo práctico para cada uno**, los siguientes conceptos fundamentales de Git:
   * *Commit*
   * *Branch* (Rama)
   * *Merge* (Fusión)
   * *Pull* y *Push*
   * *Pull Request (PR)*
   * *Clone* (Clonar)
   * *Upstream* (y su diferencia con *Origin*)
    ---

    ### 1. Commit

    * **Definición:** Es el equivalente a hacer una "fotografía" o un punto de control guardado en el historial del proyecto. Cada commit registra qué archivos cambiaron, quién los modificó, cuándo y un mensaje corto que describe el propósito de la actualización.
    * **Ejemplo práctico:** Estás programando una página web, terminas de diseñar el formulario de contacto y ejecutas el comando:
    `git commit -m "feat: add contact form validation"`
    Esto guarda ese estado específico del código de forma permanente en el historial de Git.

    ---

    ### 2. Branch (Rama)

    * **Definición:** Es una línea de desarrollo independiente. Permite trabajar en una nueva característica, experimentar o corregir un error en paralelo sin alterar el código estable principal (por lo general llamado `main` o `master`).
    * **Ejemplo práctico:** Tu aplicación de software está funcionando perfectamente en la rama `main`. Creas una nueva rama llamada `feature/shopping-cart` para programar el carrito de compras de forma aislada, sabiendo que si te equivocas o rompes algo, la versión principal de la app sigue intacta.

    ---

    ### 3. Merge (Fusión)

    * **Definición:** Es el proceso mediante el cual Git toma los cambios realizados en una rama (por ejemplo, una rama de características) y los integra formalmente dentro de otra (como la rama principal).
    * **Ejemplo práctico:** Ya terminaste y probaste con éxito el carrito de compras en tu rama `feature/shopping-cart`. Te pasas a la rama `main` y ejecutas la fusión (`merge`) para combinar el código nuevo con el software oficial que usan los usuarios.

    ---

    ### 4. Pull y Push

    * **Definición:** Son los comandos clave para sincronizar tu computadora local con un servidor remoto en la nube (como GitHub):
    * **Push (Empujar):** Sube los commits que has hecho en tu computadora local hacia el repositorio remoto.
    * **Pull (Jalar):** Descarga los cambios más recientes que están en el servidor remoto hacia tu computadora local.


    * **Ejemplo práctico:**
    * *Push:* Terminaste de corregir un error en tu laptop y escribes `git push origin main` para enviar el código a GitHub y que tu equipo lo tenga disponible.
    * *Pull:* Tu compañero de equipo subió cambios al repositorio en la mañana; al llegar a trabajar, escribes `git pull` para descargar esos cambios a tu computadora antes de empezar a programar.


    ---

    ### 5. Pull Request (PR)

    * **Definición:** Una solicitud formal dentro de una plataforma web (como GitHub o GitLab) donde avisas a tu equipo que has terminado una tarea en una rama y pides que revisen, discutan y aprueben tu código antes de fusionarlo con el proyecto principal.
    * **Ejemplo práctico:** Creaste una rama para solucionar un fallo de seguridad, la subiste a GitHub y abres un Pull Request titulado *"Fix: Patch database injection vulnerability"*. Tus compañeros revisan línea por línea tu código en la web, te dejan comentarios y, al dar el visto bueno, aprueban el PR para que se una al sistema.

    ---

    ### 6. Clone (Clonar)

    * **Definición:** La acción de descargar por primera vez una copia completa de un repositorio remoto existente (incluyendo todo su historial de commits) desde la nube hacia tu disco duro local.
    * **Ejemplo práctico:** Te acaban de contratar en una empresa y te dan el enlace de un proyecto. Abres tu terminal y escribes `git clone [https://github.com/empresa/proyecto-backend.git](https://github.com/empresa/proyecto-backend.git)` para descargar todo el código base y empezar a trabajar de inmediato.

    ---

    ### 7. Upstream vs. Origin

    * **Definición:** Son nombres de alias que se le asignan a los repositorios remotos:
    * **Origin:** Es el alias predeterminado que Git le asigna al repositorio remoto **desde el cual clonaste** el proyecto (generalmente tu propia bifurcación o el repositorio oficial donde tienes permisos directos).
    * **Upstream:** Es el alias que convencionalmente se utiliza para referirse al **repositorio original y central** (el de los creadores del proyecto) cuando has hecho una copia personal (*fork*) y necesitas recibir sus actualizaciones oficiales.


    * **Ejemplo práctico:**
    * Creas una copia (*fork*) del código de un proyecto de código abierto de la biblioteca de React en tu propia cuenta de GitHub. Tu repositorio en tu cuenta es tu **`origin`** (donde guardas tus cambios).
    * El repositorio oficial principal de React es tu **`upstream`** (desde donde descargas las últimas actualizaciones oficiales de los mantenedores principales para mantener tu copia al día).

5. **La importancia de las ramas (Branches):** ¿Por qué se deben crear ramas en un proyecto de software? Expliquen para qué sirven y qué ventajas ofrecen tanto en el trabajo individual como en equipo.

    Las **ramas (*branches*)** son uno de los conceptos más potentes y revolucionarios de Git. En esencia, una rama es un **puntero móvil hacia un commit específico** que te permite crear una línea de desarrollo independiente dentro de un mismo proyecto, completamente aislada del código principal.

    ---

    ### ¿Por qué se deben crear ramas en un proyecto de software?

    La razón principal es **proteger la estabilidad del código base** mientras se introducen cambios, se experimenta o se desarrollan nuevas funcionalidades. Sin ramas, cualquier error al escribir código afectaría de inmediato y de forma permanente el software en funcionamiento.

    ---

    ### Ventajas en el trabajo individual

    Incluso si estás programando un proyecto tú solo, las ramas ofrecen beneficios operativos indispensables:

    1. **Entorno de pruebas seguro ("Sandbox"):** Puedes experimentar con una nueva librería, cambiar la estructura de la base de datos o probar un enfoque de código arriesgado sin temor a dañar lo que ya funciona. Si todo sale mal, simplemente descartas la rama y tu proyecto principal sigue intacto.
    2. **Organización por tareas (*Feature branches*):** Te permite separar el trabajo por objetivos. Puedes tener una rama llamada `feature/login` para el módulo de acceso, otra llamada `fix/button-color` para corregir un detalle estético y la rama `main` limpia y lista. Esto evita mezclar cambios de diferentes tareas en un solo historial confuso.
    3. **Pausas limpias:** Si estás mitad de una característica compleja y surge una urgencia (por ejemplo, corregir un error crítico en producción), puedes cambiar de rama temporalmente, solucionar el problema, y luego regresar a tu desarrollo anterior sin perder el hilo.

    ---

    ### Ventajas en el trabajo en equipo

    En entornos colaborativos, las ramas son obligatorias para que múltiples desarrolladores puedan coexistir en el mismo proyecto sin destruirse el trabajo mutuamente:

    1. **Desarrollo paralelo y simultáneo:** Varios programadores pueden trabajar al mismo tiempo en el mismo repositorio sin pisarse el código. Mientras un desarrollador crea el carrito de compras en la rama `feature/cart`, otro diseña la pasarela de pagos en `feature/payment` y un tercero corrige un error en `hotfix/login`.
    2. **Revisiones de código estructuradas (*Code Review*):** Al trabajar en ramas separadas, el código no llega al sistema principal por accidente. Cada rama debe pasar por un proceso de revisión (a través de un *Pull Request*) donde el equipo analiza las líneas modificadas, debate mejoras y detecta errores antes de integrarlo.
    3. **Flujos de trabajo profesionales:** Permiten implementar metodologías estandarizadas de la industria (como *GitFlow* o *GitHub Flow*), donde existen ramas específicas para desarrollo (`dev`), pruebas (`staging`) y producción (`main`), asegurando que solo el código 100% probado llegue a los usuarios finales.