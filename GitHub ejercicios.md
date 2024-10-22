Crear un Nuevo Repositorio:

- Haz clic en tu foto de perfil en la esquina superior derecha y selecciona "Your repositories".
- Haz clic en "New" para crear un nuevo repositorio.
- Nombra tu repositorio, por ejemplo, "mi-primer-repositorio".
- Elige si quieres que sea público o privado.
- Marca la opción para inicializar el repositorio con un archivo README.
- Haz clic en "Create repository".

Editar el Archivo README:

- Entra en tu nuevo repositorio y haz clic en el archivo `README.md`.
- Haz clic en el icono de lápiz para editar.
- Escribe una breve descripción o saludo.
- Al final de la página, escribe un mensaje de commit y haz clic en "Commit changes".

# Git
### Ejercicio 1: Instalación y Configuración de Git

**Objetivo:** Instalar Git y configurar tus credenciales.

1. **Descarga e Instala Git:** Visita [git-scm.com](https://git-scm.com/) y descarga la versión de Git para tu sistema operativo.

2. **Verifica la Instalación:** Abre tu terminal o línea de comandos y ejecuta `git --version` para verificar que Git esté instalado correctamente.

3. **Configura tu Nombre y Correo Electrónico:**

    - Ejecuta `git config --global user.name "Tu Nombre"`.
    - Ejecuta `git config --global user.email "tuemail@example.com"`.
	Comprobar con:
    - `git config --global user.name`
    - `git config --global user.email`  

### Ejercicio 2: Crear tu Primer Repositorio Local

**Objetivo:** Inicializar un repositorio de Git local y realizar tu primer commit.

1. **Crea una Carpeta para tu Proyecto:** En tu computadora, crea una nueva carpeta para tu proyecto, por ejemplo, `mi-proyecto`.

2. **Inicializa el Repositorio:** Abre la terminal, navega a la carpeta del proyecto y ejecuta `git init`. Esto creará un nuevo repositorio de Git en esa carpeta.
   
3. **Crea un Archivo:** Dentro de la carpeta del proyecto, crea un archivo, por ejemplo, `README.md`, y escribe algo en él.

4. **Agrega el Archivo al Staging Area:** Ejecuta `git add README.md` para agregar el archivo al staging area de Git.

6. **Realiza tu Primer Commit:** Ejecuta `git commit -m "Primer commit: añadiendo README"`.

### Ejercicio 3: Explorar el Historial de Commits

**Objetivo:** Aprender a revisar el historial de commits.

1. **Realiza Algunos Cambios y Commits:** Haz algunos cambios en `README.md` y realiza varios commits.

2. **Revisa el Historial de Commits:** Ejecuta `git log` para ver el historial de tus commits.


### Ejercicio 4: Uso de Branches

**Objetivo:** Aprender a crear y cambiar entre branches.

1. **Crea un Nuevo Branch:** Ejecuta `git branch nombre-del-branch` para crear un nuevo branch.

2. **Cambia al Nuevo Branch:** Usa `git checkout nombre-del-branch` para cambiar al branch que acabas de crear.

3. **Realiza Cambios en el Nuevo Branch:** Haz cambios en tu proyecto bajo este branch.

4. **Vuelve al Branch Principal:** Cambia de nuevo al branch principal con `git checkout main` o `git checkout master` (dependiendo del nombre de tu branch principal).


### Ejercicio 5: Fusionar Branches

**Objetivo:** Aprender a fusionar cambios de un branch a otro.

1. **Fusiona tu Branch:** Desde el branch principal (main o master), ejecuta `git merge nombre-del-branch` para fusionar los cambios del branch que creaste.

### Recursos Adicionales

- **Documentación Oficial de Git:** Revisa la [documentación oficial de Git](https://git-scm.com/doc) para una guía más detallada.
- **Tutoriales en Línea:** Hay muchos tutoriales en línea y en YouTube que pueden proporcionarte ejemplos prácticos.

Practicando estos ejercicios básicos, te familiarizarás con las operaciones fundamentales de Git. A medida que te sientas cómodo, puedes explorar características más avanzadas. ¡Buena suerte!

## Ejercicio básico 2:
1. Crea un repositorio en GitHub con el nombre "endes-t2-ej-basico-2" con un archivo README.md
2. Clona el repositorio a tu dispositivo.
3. Añade dos lineas a tu archivo readme.md
4. Haz un commit.
5. Borra una de las lineas y añade tres al archivo readme.md
6. Haz un nuevo commit
7. Sincroniza tus cambios con el repositorio en remoto en GitHub
