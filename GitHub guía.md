# GitHub Guía

## Recursos de aprendizaje recomendados

### [Oh my Git!](https://ohmygit.org)
Juego para practicar el uso de comandos.

### [Learn Git Branching](https://learngitbranching.js.org)
Juego que cuenta con idioma español para practicar el uso de comandos y visualizar el uso de ramas.
Para cambiar el idioma, una vez comenzado un juego, click en el icono de globo terráqueo en la esquina inferior derecha.

### [git - la guía sencilla](https://rogerdudler.github.io/git-guide/index.es.html)
___

## Configuración inicial

### 1.Crear cuenta en GitHub
https://github.com/
### 2. Descargar e instalar Git
1. Descargar [git](https://git-scm.com/):
2. Sigue la [guía de instalación de Git](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git).
### 3. Setup username y email
```
$ git config --global user.name "Your name here"
$ git config --global user.email "your_email@example.com"
```
Comprobar que están bien configurados ejecutando los mismos comandos sin los parámetros.
### 4. Personalización (opcional)
```
$ git config --global color.ui true
$ git config --global core.editor "code --wait"
```
La segunda instrucción establece VSCode como nuestro editor por defecto. Si ejecutamos la orden `git commit` y no añadimos un mensaje, nos abrirá VSCode para escribirlo y esperará a que lo cerremos para continuar.

### 5. Configurar SSH

1. Configurar claves públicas en local
```
$ ssh-keygen -t rsa -C "your_email@example.com"
```

2. Copiar a portapapeles:
```
clip < ~/.ssh/id_rsa.pub
```
(comando en mac)
``` 
pbcopy < ~/.ssh/id_rsa.pub
```

3. Registrar SSH en GiHub: 
*Settings > SSH and GPG Keys > New SSH Key*

# Git - comandos básicos
- `git --version` Nos indica la versión en la que nos encontramos.
- `git clone "URL"` Acepta una URL SSH o HTTPS para clonar un repositorio.
- `git remote -v` muestra la URL SSH del repositorio en GitHub
- `add hello_world.txt` Añade el archivo `helloworld.txt`a la fase de preparación (stage) (lo prepara para el commit).
- `git add .` añade todos los archivos que han sufrido cambios a la fase de preparación (stage).
- `git status`Nos indica qué archivos han cambiado pero no se han preparado, cuales están preparados per no se han enviado, etc.
- `git commit -m "Añadir hello_world.txt"` Hace un commit (guarda) todos los archivos preparados (staged) y adjunta el mensaje "Añadir hello_world.txt".
- `git push origin main`  o `git push origin master`envía nuestros cambios; sincroniza nuestro git con el repositorio en GitHub.  Origin es el nombre de nuestra conexión remota. Por defecto y como costumbre, su nombre es origin pero se puede cambiar. Se podría ejecutar solo `git push`ya que no trabajamos con otra rama.
- `git log` Ver el historial de cambios realizados.
- `git init` Crea un nuevo repositorio git en el directorio actual.

# Git - Crear un repositorio localmente
Elegimos una carpeta, que puede estar vacía o no.
- `git init` Para crearlo. Aparece una carpeta oculta; podemos cambiar la configuración en el explorador de archivos para verla.
- Añadir una referencia al repositorio remoto en GitHub:
```
git remote add origin ssh_link_to_repository
```

# Git - Volver a un commit anterior:
- `git log`para ver el historial de commits
- `git checkout código`para volver a una versión anterior.
- Si ejecutamos `git log` Veremos que sigue trayendo `HEAD`, pero no `master` o `main`.
- `git branch`nos muestra las ramas actuales.
- `git switch master` para volver atrás, al commit más reciente.
- `git switch -c "rama2"` si queremos crear una rama desde el commit en que nos encontramos, tras haber hecho un `git checkout`.
- `git log`de nuevo para ver que nuestra `HEAD`está en rama2.
- si tecleamos `git branch`veremos que estamos en la rama2.

Podemos ver los cambios que aparecen en el archivo modificado cada vez que pedimos a Git cambiar de master a rama y viceversa.

# Atomic comments
Cada commit se debería centrar en la adición de cambios relacionados con una sola característica del programa. Así es más fácil deshacer si es preciso, y los mensajes son más descriptivos.
- En inglés se utiliza el imperativo:
`git commit -m "Add new method to print on screen"
- En español se utiliza el infinitivo:
`git commit -m "Añadir nuevo método para imprimir por pantalla"



## Software recomendado

### GitKraken
GitKraken es una herramienta gráfica (**GUI**) para el control de versiones Git, diseñada para facilitar el manejo de repositorios y flujos de trabajo en Git. Ofrece una interfaz visual intuitiva que simplifica muchas de las operaciones comunes de Git, como commit, push, pull, branch, merge, y rebase.
### Git Graph
Extensión para Visual Studio Code que permite visualizar las ramas de un proyecto.
 
## "Chuletas"
En español:
* https://training.github.com/downloads/es_ES/github-git-cheat-sheet.pdf
* https://www.developerro.com/2023/01/11/git-cheatsheet/
* https://elbauldelprogramador.com/mini-tutorial-y-chuleta-de-comandos-git/
* https://tutoriales.online/chuletas/git
En inglés:
* https://about.gitlab.com/images/press/git-cheat-sheet.pdf
Fondos de pantalla:
* https://dev.to/doabledanny/git-cheat-sheet-50-commands-free-pdf-and-poster-4gcn

## Guía de estilo para commits
https://midu.dev/buenas-practicas-escribir-commits-git/
## Flujo de GitHub
https://docs.github.com/es/get-started/using-github/github-flow

## Ramas o Branches
Las ramas (branches) en Git son increíblemente livianas. Son sólo referencias a un commit específico - nada más. Por ello tantos entusiastas de Git siguen el mantra:

```
crea ramas pronto y frecuentemente
```

Como no hay consumo extra de almacenamiento ni memoria al crear varias ramas, lógicamente es más fácil dividir tu trabajo que trabajar solamente con un par de ramas grandes.

Cuando empecemos a mezclar ramas y commits, vamos a ver cómo se combinan estas dos herramientas. Por ahora, en cambio, simplemente recuerda que una rama esencialmente dice "Quiero incluir el trabajo de este commit y todos su ancestros".

## Deshacer
Trabajar con Git implica muchas veces la necesidad de "deshacer" acciones, y las instrucciones `checkout`, `revert` y `reset` son esenciales para manejar diferentes situaciones. Aquí explicamos cómo y cuándo usar cada una:
### 1. `git checkout`
Esta instrucción se usa principalmente para cambiar de una rama a otra o revertir archivos a un estado anterior. Por ejemplo, para descartar los cambios no guardados en un archivo específico, puedes usar:

`git checkout -- <archivo>`

Esto restablecerá el archivo a su último estado guardado (commit). Sin embargo, desde la versión 2.23 de Git, se recomienda usar `git restore` para este propósito, ya que `checkout` se usa más comúnmente para cambiar entre ramas.
### 2. `git revert`
Cuando necesitas deshacer un commit público, `git revert` es la opción adecuada. Esta instrucción crea un nuevo commit que invierte los cambios introducidos por un commit anterior. Por ejemplo:

`git revert <commit>`

Es seguro para usar en entornos colaborativos, ya que no altera el historial de commits existente, lo que significa que no afectará al trabajo de otras personas que también estén trabajando en el mismo repositorio.
### 3. `git reset`
`git reset` se usa para deshacer commits en el historial local de tu repositorio. Dependiendo del modo que utilices (`--soft`, `--mixed`, `--hard`), puedes controlar exactamente qué se deshace:
- `--soft`: Los cambios de los commits deshechos permanecen en el área de staging (preparados para el próximo commit).
- `--mixed` (defecto): Los cambios vuelven al working directory, sin estar preparados.
- `--hard`: Elimina todo el historial y modificaciones al estado especificado, perdiendo todos los cambios en el working directory que no se hayan guardado.

Un ejemplo de uso podría ser:

`git reset --hard <commit>`

Este comando es poderoso y debe usarse con precaución, especialmente con `--hard`, ya que elimina los cambios de manera irreversible.
### Video explicativo (inglés)
Checkout, revert, reset 
https://youtu.be/RIYrfkZjWmA?si=LYJflGjTrrZIxUME

# Ejercicio

# Guías en inglés
https://www.theodinproject.com/lessons/foundations-git-basics
https://kbroman.org/github_tutorial/

Git avanzado
Mensajes commit
https://cbea.ms/git-commit/
https://thoughtbot.com/blog/5-useful-tips-for-a-better-commit-message?utm_medium=learn-more&utm_source=enki
