# primeros pasos con git 🌱
- 🚀 al comenzar con el proceso de nuestro git debemos seguir una serie de pasos con los cuales hacemos una buena practica y al mismo tiempo eficiente nuestro proceso

## creacion de nuestro repositorio local 🛠️
- ➡️ con el comando **git init** inicializamos nuestro repositorio local, permitiendonos trabajar sin problemas.

## gestion en nuestro repositorio local 🗂️
- 🧭 ya creado nuestros archivos y teniendo los resultados esperados podemos comenzar un nuevo  proceso que consta de lo siguiente:

### agregar los archivos a staging area ➕
- 🚶 esto prepara los archivos para posteriormente ser enviados al remoto
• ① para hacer esto  contamos con nuestro comando **git add .** si deseas agregarlos todos sin excepcion
• ② para agregar uno en especifico es con nuestro comando **git add + el nombre de archivo**

### eliminar los archivos de staging area 🗑️
- 🚫 si en un caso dado que los archivos esten el en staging area pero no deseas agregar un en especifico puedes eliminarlo o descartarlo asi:
• ✂️ con el comando **git rm --cached + el nombre del archivo** se elimina ese archivo, si deseas eliminar dos o mas archivo solo haces lo mismo con la diferencia de que en el nombre del archivo se va a poner los nombre de todos separadod por un espacio

### realizar un commit 🆕
- 🚀 Un commit es una instantánea de tu proyecto en un momento determinado. Cada vez que realizas un commit, estás guardando el estado actual de tu proyecto.
• ① para realizar un commit es con el comando **git commit -m "change: emoji: descripcion de lo realizado" 

**tipos de changes** 🔠

| Tipo de Commit     | Descripción                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------|
| `fix`              | Arregla un problema en el código fuente.                                                         |
| `feat`             | Inserta algo nuevo, ya sea código fuente o archivos.                                             |
| `refactor`         | Mejoras internas del código fuente, como reestructuración de carpetas o comentarios.             |
| `release`          | Se ha creado una nueva versión del documento ‘tag’.                                              |
| `docs`             | Cambios en la documentación (por ejemplo, en `README.md`).                                       |
| `chore`            | Tareas de mantenimiento como dar formato al código o cambiar rutas de archivos o endpoints.      |
| `style`            | Cambios en la apariencia de la web (CSS, HTML), sin afectar la lógica.                           |
| `BREAKING CHANGE!` | Cambios que rompen compatibilidad (como funciones o APIs modificadas). Requiere símbolo `!`.     |

**Emojis comunes** 🔠

| Emoji                             | Propósito                           | Tipo sugerido (Conventional Commit) |
| -------------------------------   | ----------------------------------- | ----------------------------------- |
| ✨ (`:sparkles:`)                 | Añadir una nueva funcionalidad      | `feat`                              |
| 🐛 (`:bug:`)                      | Corrección de errores               | `fix`                               |
| 📝 (`:memo:`)                     | Actualizar documentación            | `docs`                              |
| 🎨 (`:art:`)                      | Mejoras de formato o estilo         | `style`                             |
| 🔥 (`:fire:`)                     | Eliminar código o archivos          | `refactor`                          |
| 🚑️ (`:ambulance:`)                | Hotfix (corrección urgente)         | `fix`                               |
| ♻️ (`:recycle:`)                  | Refactorización de código           | `refactor`                          |
| ✅ (`:white_check_mark:`)         | Añadir o modificar pruebas          | `test`                              |
| 🔧 (`:wrench:`)                   | Cambios en configuración            | `chore`                             |
| 🚀 (`:rocket:`)                   | Implementar algo en producción      | `chore`                             |
| ⚡ (`:zap:`)                      | Mejoras de rendimiento              | `perf`                              |
| 🐳 (`:whale:`)                    | Cambios relacionados con Docker     | `chore`                             |
| 📦️ (`:package:`)                  | Añadir o actualizar dependencias    | `chore`                             |
| 💄 (`:lipstick:`)                 | Cambios en el diseño o UI           | `style`                             |
| 🚨 (`:rotating_light:`)           | Solución de advertencias de linting | `fix`                               |
| 🔒 (`:lock:`)                     | Solución de problemas de seguridad  | `fix`                               |
| 🚧 (`:construction:`)             | Trabajo en progreso (WIP)           | `chore`                             |
| 🗑️ (`:wastebasket:`)              | Borrar archivos o código            | `chore`                             |
| 🌱 (`:seedling:`)                 | Inicialización de proyecto          | `chore`                             |
| 📈 (`:chart_with_upwards_trend:`) | Mejorar análisis o seguimiento      | `feat`                              |
| 🐿️ (`:chipmunk:`)                 | Cambios experimentales              | `feat`                              |

### visualizar los commit realizados 👀
- 📊 al crear un commit a esta se le genera un número unico el cual es de mucha ayuda para navegar entre ellos
• 🔍 para ver todos los commit con su ID completo, autor, fecha y el mensaje que se le colocó es con el comando **git los**
• 👓 para ver todos los commit pero solo los primeros 6 números del dígito y la descripción de lo que se hizo es con el comando **git log --oneline**

### navegar entre commits  🚗
- sugerido
🧭 navegar entre los commits hace referencia a que podemos dirigirnos de un commit hacia otro, permitiendonos visualizar los cambios o ver el estado de nuestros archivos en ese espacio del tiempo, podemos hacerlo de las siguientes maneras
• ① para dirigirnos a un commit en especifico primero **listamos los commit existentes** para poder visualizar su id, luego con el comando **git checkout + id del commit** podemos dirigirnos o posarnos en ese commit
**volver a tu momento actual**
• ② lo hacemos con el comando **git checkout main**

- 🚀 con el comando **git checkout** no solo permite viajar entre commit si no tambien crear ramas desde el commit pasado en el que nos encontramos
• esto se puede hacer con el comando **git checkout -b nombre-de-nueva-rama + id del commit**

## Clonar un repositorio, hace push y pull

### clonar repositorios 🧬
- 📄 para clonar un repositorio que se encuentra en el remoto lo podemos hacer con los siguientes pasos
• ① en nuestra terminal nos ubicamos en la carpeta donde queremos que se guarden, esto lo hacemos con el comando **cd + la ruta**
• ② ya ubicados podemos clonar con el comando **git clone + URL del repositorio que deseamos clonar

### utilizar pull y push 🔧
- cabe recalcar que para poder utilizar estos comando debemos tener el sincronizados tu repositorio local con el remoto.
• ① **git push** → Se realiza para mandar desde el repositorio local al remoto, mandar que? el código de como va hasta el momento con el proyecto localmente, después de que vea que todo esta bien lo que se hace es actualizar el repositorio remoto con lo del local 
• ② **git pull** → Se hace con el fin de poder actualizar el repositorio local, esto pasa cuando se esta trabajando y alguien sube algún cambio o feature nueva al remoto, lo que se hace para ir al día con el remoto es traer todo lo que hay allí para tener todo actualizado en el repositorio local 

### revertir cambios ↩️  
- 🔄 revertir cambios consiste en que si en un momento dado realizamos un commit pero los cambios q hicimos, si estos no son utiles y al contrario nos dañan el codigo podemos revertir esos cambios que hicimos para volver a tener el codigo fuente, esto lo podemos hacer de las siguientes maneras:
#### git resert ⏪
- 🔙 este comando solo se usa en nuestro repositorio local, y se recomienda no elimianar o tocar commits que ya se encuentran en el remoto
• para utilizarlo es con el comando **git reset --hard idcommit**
#### git revert ⏩
- ♻️ este comando te dirije a un commit en especifico permitiendonos hacer cambios en ese commit, como ventaja tiene que no se nos barrará los commits que se encuentran despues del commit al que nos posicionamos.