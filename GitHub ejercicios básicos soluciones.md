## Creaión y actualización de repositorios

### Ejercicio 1
```
git config --global user.name "Your-Full-Name"
git config --global user.email "your-email-address"
git config --global color.ui auto
git config --list
```

### Ejercicio 2
```
mkdir libro
cd libro
git init
ls -la
```

### Ejercicio 3
```
git status
touch indice.txt
```
Crear archivo y añadir contenido
```
git status
git add indice.txt
git status
```

### Ejercicio 4
```
git commit -m "Añadido índice del libro."
git status
```

### Ejercicio 5
Añadir contenido al archivo
```
git diff
git add indice.txt
git commit -m "Añadido capítulo 3 sobre gestión de ramas"
```

## Ejercicios de manejo del historial de cambios
```
git log
mkdir capitulos
cd capitulos
touch capitulo1.txt
```
añadir contenido
```
git add .
git commit -m "Añadido capítulo 1."
git log
```

### Ejercicio 2
```
touch capitulo2.txt
```
Añadir contenido
```
git add .
git commit -m "Añadido capítulo 2."
git diff HEAD~2..HEAD
```

### Ejercicio 3
```
touch capitulo3.txt
```
Añadir contenido
```
git add .
git commit -m "Añadido capítulo 3."
git log
git diff &lt;codigo hash de la primera version>..HEAD
```

### Ejercicio 4
Añadir contenido
```
git add .
git commit -m "Añadido capítulo 5 al índice."
git annotate indice.txt
```

