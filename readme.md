## Git Manual:

## Commits en Git

1. **Realizar cambios significativos**: Antes de hacer un commit, asegúrate de que los cambios que has realizado sean significativos y estén relacionados con una funcionalidad específica o una corrección de errores.

2. **Staging**: Agrega los archivos modificados al área de _staging_ utilizando el comando `git add <nombre_archivo>` o `git add .` para agregar todos los archivos modificados.

3. **Commit**: Realiza el commit con el comando `git commit -m "Mensaje descriptivo"`. El mensaje debe ser claro y conciso.

## Mensajes de Commit

Los mensajes de commit deben seguir una estructura clara para facilitar la comprensión y el seguimiento del historial del proyecto. Se recomienda el siguiente formato:

```
<tipo>: <descripción breve>
<detalles opcionales>
```

- **Tipo**: Indica el propósito del commit. Algunos tipos comunes son:

  - `feat`: Nueva funcionalidad.
  - `fix`: Corrección de errores.
  - `docs`: Cambios en la documentación.
  - `style`: Cambios en el formato o estilo del código.
  - `refactor`: Refactorización del código.
  - `test`: Agregar o modificar pruebas.
  - `chore`: Tareas de mantenimiento o configuración.

- **Descripción breve**: Resume el cambio realizado en una línea.

- **Detalles opcionales**: Proporciona más contexto o detalles sobre el cambio.

## Subfijos de Commit

Además de los tipos de commit, puedes utilizar subfijos para indicar el alcance o la categoría del cambio. Algunos ejemplos son:

- `feat(login)`: Nueva funcionalidad relacionada con el inicio de sesión.
- `fix(api)`: Corrección de un error en la API.
- `docs(readme)`: Actualización de la documentación en el archivo README.

## Tipos de Ramas

1. **Rama principal (main o master)**:

   - Contiene la versión estable del código.
   - Se fusionan con otras ramas después de pruebas exhaustivas.

2. **Ramas de características (feature branches)**:

   - Creadas para desarrollar nuevas funcionalidades.
   - Se fusionan con la rama principal cuando la funcionalidad está completa.

3. **Ramas de corrección (bugfix branches)**:

   - Creadas para corregir errores.
   - Se fusionan con la rama principal después de solucionar el problema.

4. **Ramas de liberación (release branches)**:

   - Preparadas para lanzamientos.
   - Se utilizan para pruebas finales y ajustes antes de la versión final.

5. **Ramas de hotfix (hotfix branches)**:
   - Creadas para corregir errores críticos en producción.
   - Se fusionan con la rama principal y las ramas de liberación.

## Ayudas

1. **Resetear Ramas**:

   - Hard Reset: Si deseas descartar todos los cambios en una rama y volver al estado del último commit, puedes usar git reset --hard HEAD. Ten en cuenta que esto eliminará todos los cambios no guardados.

   - Soft Reset: Si solo deseas deshacer los commits sin perder los cambios en los archivos, utiliza git reset --soft HEAD~1. Esto mantendrá los cambios en el área de staging.

2. **Deshacer Cambios en Archivos**:

   - Si has añadido un archivo por error, puedes quitarlo del área de staging con git reset <nombre_archivo>.
   - Si ya has hecho commit del archivo, puedes usar git reset HEAD~1 para deshacer el último commit y mantener los cambios en el área de trabajo.

3. **Revertir Commits**:

   - Utiliza git revert <hash_commit> para crear un nuevo commit que deshaga los cambios introducidos por un commit específico. Esto es útil para mantener un historial limpio.

4. **Ignorar Archivos**:
   - Crea un archivo .gitignore para especificar los archivos o patrones que Git debe ignorar (por ejemplo, archivos de compilación, archivos temporales, etc.).
