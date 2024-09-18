
### Razones para crear una rama antes de una pull request:

1. **Separación de tareas**: Trabajar en una rama separada te permite mantener tu trabajo aislado del código principal (`main` o `master`). Así puedes trabajar en nuevas funcionalidades, corregir errores o hacer cambios sin afectar el código estable.

2. **Colaboración eficiente**: Al crear una rama para cada cambio, es más fácil para otros colaboradores revisar y aprobar tus cambios sin que afecte el desarrollo principal. Esto también facilita la **revisión** y **pruebas** de tu código en el contexto correcto.

3. **Manejo de conflictos**: Si trabajas directamente en una rama principal (como `main`) y alguien más hace cambios antes de que tú subas los tuyos, es más probable que surjan conflictos de fusión (merge conflicts). Tener una rama separada ayuda a manejar mejor estos casos.

4. **Mejores prácticas en Git**: En la mayoría de los proyectos que siguen un flujo de trabajo estándar (como Gitflow o GitHub Flow), se espera que los cambios se realicen en una rama separada y luego se envíen a la rama principal a través de una pull request. Esto garantiza un flujo de trabajo organizado y limpio.

### Flujo típico con ramas y pull request:

1. Creas una nueva rama desde `main` o la rama en la que estés trabajando:
   ```bash
   git checkout -b nombre-de-la-rama
   ```

2. Realizas los cambios en esa nueva rama.

3. Subes los cambios a tu repositorio remoto:
   ```bash
   git push origin nombre-de-la-rama
   ```

4. Abres una pull request desde esa rama hacia `main` (u otra rama en la que deba integrarse).
