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

## 2. Comandos básicos en Git
Algunos comandos esenciales para trabajar con Git son:

- **`git init`**: Inicializa un nuevo repositorio en el directorio actual.
- **`git add`**: Prepara los cambios para confirmarlos.
- **`git commit`**: Registra los cambios en el historial del repositorio.
- **`git push`**: Sube los cambios confirmados al repositorio remoto.
- **`git pull`**: Trae los últimos cambios desde el repositorio remoto.
- **`git status`**: Muestra el estado actual del repositorio.

## 3. Flujos de trabajo en Git
### Flujo básico:
1. Modificar archivos en tu proyecto.
2. Preparar los cambios con `git add`.
3. Confirmar los cambios con `git commit`.
4. Subir los cambios al repositorio remoto con `git push`.

### Flujo Gitflow:
- Crear una nueva rama: `git checkout -b feature/nueva-funcionalidad`.
- Trabajar en la rama y realizar commits.
- Hacer merge con la rama principal: `git checkout main` seguido de `git merge feature/nueva-funcionalidad`.

## 4. Trabajando con repositorios remotos en GitHub
Para trabajar con un repositorio remoto en GitHub:
1. **Conectar un repositorio local**:
   `git remote add origin https://github.com/usuario/repositorio.git`

2. **Subir cambios al repositorio remoto**:
   `git push -u origin main`**: Muestra el estado actual del repositorio.

3. **Hacer un Pull Request**:
- Crea una rama y sube tus cambios: `git push origin nombre-de-la-rama`.
- Ve al repositorio en GitHub, selecciona tu rama y crea una Pull Request.
- Describe los cambios y solicita revisión.

## 5. Publicar con GitHub Pages
Puedes usar GitHub Pages para alojar sitios web estáticos directamente desde tu repositorio:

1. **Crea una rama llamada gh-pages**:
- `git checkout -b gh-pages`
- `git push origin gh-pages`

2. **Habilita GitHub Pages en la configuración del repositorio y selecciona la rama gh-pages.**:
Consejo adicional: Si tu proyecto incluye archivos que comienzan con _ o no utiliza Jekyll, agrega un archivo vacío llamado .nojekyll en la raíz del repositorio para desactivar el procesamiento de Jekyll.

## 6. Recursos adicionales
- [Archivo con resumen detallado de comandos y conceptos: Resumen de comandos Git](./resumen.txt)
- [Documentación oficial de Git: Git Docs](https://git-scm.com/doc)
- [Guías de GitHub: GitHub Guides](https://guides.github.com/)


