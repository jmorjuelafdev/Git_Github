# Git y GitHub

Por: Johanna Marcela Orjuela Flórez
Curso profesional de Git y Github en Platzi
Proyecto final
2024

## 1. Introducción a Git
Git es una herramienta de control de versiones creada por Linus Torvalds en 2005. Es fundamental para equipos de desarrollo, ya que permite registrar y gestionar los cambios realizados en el código fuente de un proyecto de forma eficiente.

**Características clave de Git:**
- **Distribuido**: Cada colaborador tiene una copia completa del repositorio, incluyendo todo el historial.
- **Velocidad**: Git está diseñado para realizar operaciones de manera rápida.
- **Colaboración**: Git permite que múltiples desarrolladores trabajen simultáneamente en un proyecto.
- **Control de versiones**: Ayuda a gestionar múltiples versiones de un proyecto, permitiendo revertir cambios o comparar versiones anteriores.

## 2. Comandos básicos en Git
Los comandos básicos son el núcleo del uso de Git. Algunos comandos esenciales para trabajar con Git son:

- **`git init`**: Crea o inicializa un nuevo repositorio en la carpeta actual.
- **`git add`**: Agrega cambios de archivos específicos al área de preparación (staging), preparándolos para ser confirmados.
- **`git commit`**: Registra los cambios en el repositorio con un mensaje descriptivo que explique qué se hizo.
- **`git push`**: Sube los cambios confirmados al repositorio remoto.
- **`git pull`**: Trae los últimos cambios desde el repositorio remoto.
- **`git status`**: Muestra qué archivos han sido modificados y cuáles están listos para el commit.
- **`git log`**: Lista el historial de commits en orden cronológico.

## 3. Flujos de trabajo en Git
El flujo de trabajo en Git sigue una estructura clara para mantener el orden en el desarrollo:

### Flujo básico:
1. Editar archivos: Realiza los cambios necesarios en los archivos del proyecto.
2. Preparar los cambios con `git add`: Indica cuáles de estos cambios deseas incluir en el commit.
3. Confirmar los cambios con `git commit`: Guarda una versión en el repositorio.
4. Subir los cambios al repositorio remoto con `git push`.
5. Trabajar con ramas `git branch`: Permite desarrollar nuevas funcionalidades sin afectar la rama principal
6. Integrar cambios `git merge`: Combina ramas al proyecto principal, resolviendo posibles conflictos en el proceso.

## 4. Flujos de trabajo profesionales
En proyectos grandes o en equipo, es fundamental seguir flujos de trabajo organizados. Algunos métodos populares incluyen:

### Flujo Gitflow:
Divide el desarrollo en ramas principales como main, develop y ramas específicas para funcionalidades, fixes y lanzamientos.
- Crear una nueva rama: `git checkout -b feature/nueva-funcionalidad`.
- Trabajar en la rama y realizar commits.
- Hacer merge con la rama principal: `git checkout main` seguido de `git merge feature/nueva-funcionalidad`.

## 5. Múltiples entornos de trabajo en Git

Git permite gestionar varias ramas y entornos de trabajo. Algunos comandos útiles son:

- **`git stash`**: Guarda cambios no confirmados temporalmente.

    `git stash`
    `git stash pop`

- **`git cherry-pick`**: Aplica un commit específico de otra rama.

     `git cherry-pick <hash_del_commit>`

- **`git cherry-pick`**: Aplica un commit específico de otra rama.

    `git clean: Elimina archivos no rastreados`

## 6. Trabajando con repositorios remotos en GitHub

GitHub es una plataforma de desarrollo colaborativo basada en la web que permite a los programadores y desarrolladores almacenar, gestionar y compartir proyectos de software. Se basa en el sistema de control de versiones Git, lo que permite a los equipos trabajar en proyectos de manera simultánea, gestionando de forma eficiente los cambios y las versiones del código.

GitHub sirve principalmente para:

- **Almacenamiento de código fuente**: Puedes almacenar y organizar tu código en repositorios de forma remota.
- **Control de versiones: Permite seguir**: y registrar el historial de cambios en los archivos, lo que   facilita la colaboración y la gestión de proyectos a largo plazo.
-**Colaboración: Permite que varios**: desarrolladores trabajen juntos en el mismo proyecto, gestionando las diferentes versiones y evitando conflictos de código mediante herramientas como ramas (branches), pull requests y revisiones.
- **Documentación**: Puedes agregar documentación en archivos como README.md para explicar el proyecto, su uso y su instalación.
**Control de calidad**: GitHub incluye herramientas como GitHub Actions, que permiten automatizar procesos como la ejecución de pruebas o la implementación del código.

¿Cómo se utiliza GitHub?

1. **Crear una cuenta en GitHub**: Lo primero es crear una cuenta en GitHub.
2. **Crear un repositorio remoto en GitHub**: Una vez dentro de GitHub, puedes crear un repositorio donde almacenarás tu código. Un repositorio puede ser público o privado.
- Ingresa a GitHub y crea un nuevo repositorio desde la interfaz web.
- Copia la URL del repositorio (HTTPS o SSH).

Para trabajar con un repositorio remoto en GitHub:

3. **Conectar un repositorio local a GitHub**:
Agrega el repositorio remoto a tu proyecto local con:
   git remote add origin <URL-del-repositorio>
Ejemplo:
   `git remote add origin https://github.com/usuario/repositorio.git`

4. **Subir cambios al repositorio remoto**: Para enviar los cambios locales al repositorio remoto, usa:
   `git push -u origin main`**: Muestra el estado actual del repositorio.
Esto configura origin como el repositorio remoto por defecto.

5. **Trabajar con repositorios remotos existentes**: Si deseas trabajar en un repositorio ya existente en GitHub:
   git clone <URL-del-repositorio>
Esto descargará el repositorio y creará una copia local.

6. **Obtener cambios del repositorio remoto**: Si otros colaboradores realizaron cambios, puedes actualizarlos en tu repositorio local con:
   `git pull origin main`

7. **Revisar la conexión con el repositorio remoto**: Para verificar qué repositorios remotos están configurados, usa:
   `git remote -v`

## 7. Hacer un Pull Request**:
Los Pull Requests son una forma de proponer cambios en un repositorio. Permiten la revisión y colaboración antes de fusionar esos cambios en la rama principal u otra rama específica.

1. **Crear un Pull Request**: Asegúrate de haber subido tus cambios a una rama específica, por ejemplo, feature/nueva-funcionalidad:
   `git checkout -b feature/nueva-funcionalidad`

Haz cambios, añade y confirma
   - `git add .`
   - `git commit -m "Añadida nueva funcionalidad"`
   - `git push origin feature/nueva-funcionalidad`

- En GitHub, ve a la pestaña "Pull Requests" del repositorio.
- Haz clic en "New Pull Request".
- Selecciona la rama base (por ejemplo, main) y la rama con tus cambios (por ejemplo, feature/nueva-funcionalidad).
- Agrega un título y descripción explicando los cambios realizados.
- Haz clic en "Create Pull Request".

2. **Revisar un Pull Request**: Los colaboradores pueden revisar el Pull Request, dejar comentarios y solicitar cambios. Si se aprueba, el propietario del repositorio o alguien con permisos puede fusionarlo a la rama base.

3. **Fusionar un Pull Request**: Una vez aprobado, puedes fusionar los cambios usando la opción de "Merge" en GitHub. Existen varias estrategias de fusión:
- Merge commit: Agrega todos los cambios en un solo commit.
- Squash and merge: Combina todos los commits del PR en uno solo.
- Rebase and merge: Reaplica los commits sobre la rama base para un historial más lineal.

4. **Cerrar un Pull Request**: Si los cambios no son necesarios o deben ser revisados más tarde, puedes cerrar el PR sin fusionarlo.

Ejemplo de uso típico de Pull Requests:
- Crea una rama de trabajo (feature/nueva-funcionalidad).
- Realiza los cambios y súbelos al repositorio remoto.
- Crea un Pull Request desde la rama feature/nueva-funcionalidad hacia main.
- Participa en la revisión, realiza ajustes si son necesarios.
- Fusiona los cambios cuando el Pull Request sea aprobado.

## 8. Publicar con GitHub Pages

GitHub Pages es un servicio de GitHub que permite alojar sitios web estáticos directamente desde un repositorio. Para configurar un sitio usando GitHub Pages, debes activar esta opción en la configuración del repositorio y seleccionar la rama desde la cual se publicarán los archivos del sitio.

Pasos para habilitar GitHub Pages en tu repositorio

1. **Crea una rama llamada gh-pages**: Esta rama será la que GitHub utilizará para publicar el contenido del sitio web.

- Primero, crea la nueva rama llamada gh-pages y cámbiate a ella:
  `git checkout -b gh-pages`
- Luego, sube la rama gh-pages al repositorio remoto:
  `git push origin gh-pages`
Esto crea y sube la rama gh-pages a tu repositorio en GitHub.

Habilita GitHub Pages en la configuración del repositorio y selecciona la rama gh-pages

2. **Dirígete a la página principal de tu repositorio en GitHub**:

- Haz clic en la pestaña Settings (Configuración), que se encuentra en la parte superior del repositorio.
- Desplázate hacia abajo hasta encontrar la sección GitHub Pages.
- En el menú desplegable de Source (Fuente), selecciona la rama gh-pages.
- Guarda los cambios y GitHub automáticamente generará una URL pública para tu sitio web, algo como:
  `https://<tu-usuario>.github.io/<nombre-del-repositorio>/`


## 9. Comandos de Git para casos de emergencia

Soluciones a problemas comunes con Git:

Deshacer cambios en un archivo (sin eliminar el archivo localmente)

1. Si has realizado cambios en un archivo que aún no has confirmado (commit) y deseas revertirlos a su último estado confirmado, puedes usar. Este comando revertirá los cambios no confirmados en el archivo a la versión más reciente en el repositorio:

`git checkout -- archivo.txt`

2. Deshacer el último commit (pero conservar los cambios en el área de trabajo). Si cometiste un error en el último commit, puedes deshacerlo sin perder los cambios con:

`git reset --soft HEAD~1`

3. Eliminar el último commit (y también los cambios). Si deseas eliminar tanto el commit como los cambios realizados, puedes usar:

`git reset --hard HEAD~1`

Este comando eliminará tanto el commit como cualquier cambio que hayas hecho, así que ten cuidado.

4. Recuperar un archivo borrado (sin necesidad de hacer commit). Si accidentalmente eliminaste un archivo y deseas recuperarlo desde el último commit, puedes usar:

`git checkout <hash_del_commit> -- <archivo>`

Esto recupera el archivo del historial sin necesidad de realizar un commit adicional.

5. Volver a un commit anterior (sin eliminar cambios posteriores). Si necesitas deshacer todos los cambios realizados después de un commit específico pero sin perder esos cambios localmente, usa:

`git reset --mixed <hash_del_commit>`

Esto mueve la cabeza del repositorio al commit especificado pero mantiene los cambios en el área de trabajo.

6. Restaurar todos los archivos a su estado más reciente. Si deseas restaurar todos los archivos de tu repositorio al estado más reciente confirmado (desde el último commit), puedes usar:

`git reset --hard HEAD`

Este comando restaura todos los archivos a la última versión confirmada, eliminando cualquier cambio no confirmado.

7. Ver el historial de commits de forma simplificada. Si necesitas ver un historial de los commits de manera compacta, puedes usar:

`git log --oneline`

Muestra un historial de commits con una sola línea por cada commit, mostrando el hash corto y el mensaje del commit.

8. Forzar un push (evitar conflictos con el repositorio remoto). Si has hecho un git reset o manipulado el historial y necesitas actualizar el repositorio remoto de manera forzada, puedes usar:

`git push --force`

Este comando sobrescribe el historial remoto con tu versión local. Usar este comando con precaución, ya que puede eliminar commits previos del repositorio remoto.


# Aclaración importante:
Algunos de los comandos mencionados en esta sección no son las mejores prácticas en el uso diario de Git. Si bien pueden ser útiles en situaciones de emergencia o para resolver problemas puntuales, es recomendable utilizarlos con precaución y en circunstancias controladas. En particular, los comandos como git reset --hard o git push --force pueden alterar el historial del repositorio y eliminar cambios, lo que podría causar problemas en proyectos colaborativos. Es importante asegurarse de que no haya trabajo de otros colaboradores que se vea afectado antes de utilizarlos.

Siempre es recomendable hacer un respaldo de tu trabajo antes de ejecutar estos comandos y, si trabajas en equipo, comunicarte con tus compañeros para evitar conflictos.

## 10. Bonus sobre Git y GitHub

Consejos avanzados para optimizar el uso de Git y GitHub:

- .gitignore: Archivo donde defines qué archivos o carpetas no deben ser rastreados por Git, como archivos temporales o credenciales.
Usa .gitignore: Crea este archivo para ignorar elementos no deseados, como:

`node_modules/`
`.env`
- Hooks: Scripts personalizados que se ejecutan automáticamente en eventos específicos, como antes de un commit.Automatiza tareas como verificar errores antes de un commit. Ejemplo:

`echo "npm test" > .git/hooks/pre-commit`
`chmod +x .git/hooks/pre-commit`

- Buenas prácticas: Mantén mensajes de commit claros y concisos, utiliza ramas descriptivas y revisa regularmente el estado del proyecto.

- Colaboración en proyectos abiertos: Haz un fork del repositorio y contribuye mediante Pull Requests.


## 11. Recursos adicionales
- [Glosario de términos de Git y Github:](./glosario.txt)
- [Documentación oficial de Git: Git Docs](https://git-scm.com/doc)
- [Guías de GitHub: GitHub Guides](https://guides.github.com/)


