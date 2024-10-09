# Índice

1. [Conceptos básicos de Git](#conceptos-básicos-de-git)
   1. [Git config: Preséntate a Git](#1-git-config-preséntate-a-git)
   2. [git init: Donde comienza tu viaje de código](#2-git-init-donde-comienza-tu-viaje-de-código)
   3. [git add: Preparando tu código](#3-git-add-preparando-tu-código)
   4. [git commit: Registra cambios](#4-git-commit-registra-cambios)
   5. [git log: Recorrer el árbol de commits](#5-git-log-recorrer-el-árbol-de-commits)
   6. [git branch: Entendiendo los conceptos básicos de Git branch](#6-git-branch-entendiendo-los-conceptos-básicos-de-git-branch)
   7. [git checkout/git switch: Cambiar entre branches](#7-git-checkoutgit-switch-cambiar-entre-branches)
   8. [git merge: Fusionando branches y git branch -d: Eliminando una Branch](#8-git-merge-fusionando-branches-y-git-branch--d-eliminando-una-branch)
2. [Preguntas](#preguntas)
3. [Ejercicios](#ejercicios)
   1. [Ejercicio 1: Manejo avanzado de branches y resolución de conflictos](#ejercicio-1-manejo-avanzado-de-branches-y-resolución-de-conflictos)
   2. [Ejercicio 2: Exploración y manipulación del historial de commits](#ejercicio-2-exploración-y-manipulación-del-historial-de-commits)
   3. [Ejercicio 3: Creación y gestión de branches desde commits específicos](#ejercicio-3-creación-y-gestión-de-branches-desde-commits-específicos)
   4. [Ejercicio 4: Manipulación y restauración de commits con git reset y git restore](#ejercicio-4-manipulación-y-restauración-de-commits-con-git-reset-y-git-restore)
   5. [Ejercicio 5: Trabajo colaborativo y manejo de Pull Requests](#ejercicio-5-trabajo-colaborativo-y-manejo-de-pull-requests)
   6. [Ejercicio 6: Cherry-Picking y Git Stash](#ejercicio-6-cherry-picking-y-git-stash)

---

# Conceptos básicos de Git

En esta sección se siguen los pasos de la actividad 3 y al final se suben a GitHub.

## 1. Git config: Preséntate a Git

Configura tu identidad en Git usando tu nombre y correo electrónico.

## 2. git init: Donde comienza tu viaje de código

Inicia un nuevo repositorio en tu máquina local.

## 3. git add: Preparando tu código

Añade los archivos que deseas rastrear al área de preparación.

## 4. git commit: Registra cambios

Confirma tus cambios en el repositorio local con un mensaje descriptivo.

## 5. git log: Recorrer el árbol de commits

Usa `git log` para ver el historial de commits. Esto te permitirá revisar cambios anteriores.

Ejemplo de salida:

```
* f9d7baf 2 hours ago ("Jorge Barriga") Initial commit
* c4e50a9 1 day ago ("Jorge Barriga") Added new feature
|\
| * d3d2e2a 2 days ago ("Alonso Barriga") Merged branch 'feature'
|/
* e1d9c0a 3 days ago ("Jorge Barriga") Updated README.md
```

## 6. git branch: Entendiendo los conceptos básicos de Git branch

Crea y gestiona ramas en tu repositorio.

## 7. git checkout/git switch: Cambiar entre branches

Cambia entre ramas según lo necesites para trabajar en diferentes características o correcciones.

## 8. git merge: Fusionando branches y git branch -d: Eliminando una Branch

Fusiona ramas y elimina aquellas que ya no necesites.

---

# Preguntas

**Pregunta 1:** ¿Cómo te ha ayudado Git a mantener un historial claro y organizado de tus cambios?

Git ayuda a mantener un historial claro al permitir un seguimiento detallado de cada modificación a través de commits con mensajes descriptivos.

**Pregunta 2:** ¿Qué beneficios ves en el uso de branches para desarrollar nuevas características o corregir errores?

Las ramas permiten trabajar en copias aisladas del código, evitando interferencias en el código principal y facilitando la colaboración.

**Pregunta 3:** Realiza una revisión final del historial de commits para asegurarte de que todos los cambios se han registrado correctamente.

Revisa tu historial para confirmar que todas las modificaciones deseadas están registradas.

**Pregunta 4:** Revisa el uso de branches y merges para ver cómo Git maneja múltiples líneas de desarrollo.

Reflexiona sobre cómo Git gestiona diferentes líneas de desarrollo mediante ramas y fusiones.

---

# Ejercicios

## Ejercicio 1: Manejo avanzado de branches y resolución de conflictos

**Objetivo:** Practicar la creación, fusión y eliminación de ramas, así como la resolución de conflictos.

### Instrucciones:

1. **Crear una nueva rama para una característica:** Crea una rama llamada `feature/advanced-feature` desde `main`.

2. **Modificar archivos en la nueva rama:** Edita `main.py` para incluir una nueva función y confirma los cambios.

3. **Simular un desarrollo paralelo en la rama `main`:** Cambia a `main`, edita `main.py` de forma diferente y confirma los cambios.

4. **Intentar fusionar la rama `feature/advanced-feature` en `main`:** Realiza la fusión.

5. **Resolver el conflicto de fusión:** Abre el archivo con conflictos, resuélvelos y completa la fusión.

6. **Eliminar la rama fusionada:** Elimina `feature/advanced-feature`.

---

## Ejercicio 2: Exploración y manipulación del historial de commits

**Objetivo:** Aprender a navegar y manipular el historial de commits usando comandos avanzados de Git.

### Instrucciones:

1. **Ver el historial detallado de commits:** Usa `git log -p` para ver los cambios en cada commit.

2. **Filtrar commits por autor:** Muestra solo los commits realizados por un autor específico.

3. **Revertir un commit:** Usa `git revert HEAD` para deshacer el commit más reciente.

4. **Rebase interactivo:** Usa `git rebase -i HEAD~3` para combinar varios commits en uno solo.

5. **Visualización gráfica del historial:** Usa `git log --graph --oneline --all` para ver el historial de forma gráfica.

---

## Ejercicio 3: Creación y gestión de branches desde commits específicos

**Objetivo:** Practicar la creación de ramas desde commits específicos.

### Instrucciones:

1. **Crear una nueva rama desde un commit específico:** Identifica un commit antiguo y crea una nueva rama desde ahí.

2. **Modificar y confirmar cambios en la nueva rama:** Realiza cambios y confírmalos.

3. **Fusionar los cambios en la rama principal:** Cambia a `main` y fusiona la nueva rama.

4. **Explorar el historial después de la fusión:** Usa `git log` y `git log --graph` para revisar cómo se integró el commit.

5. **Eliminar la rama `bugfix/rollback-feature`:** Elimina la rama una vez que los cambios estén fusionados.

---

## Ejercicio 4: Manipulación y restauración de commits con `git reset` y `git restore`

**Objetivo:** Usar `git reset` y `git restore` para deshacer cambios.

### Instrucciones:

1. **Hacer cambios en `main.py`:** Realiza un cambio y confírmalo.

2. **Usar `git reset` para deshacer el commit:** Usa `git reset --hard HEAD~1` para revertir el último commit.

3. **Usar `git restore` para deshacer cambios no confirmados:** Realiza cambios no confirmados y luego desházalos con `git restore`.

---

## Ejercicio 5: Trabajo colaborativo y manejo de Pull Requests

**Objetivo:** Simular un flujo de trabajo colaborativo utilizando ramas y pull requests.

### Instrucciones:

1. **Crear un nuevo repositorio remoto:** Clona un nuevo repositorio desde GitHub o GitLab.

2. **Crear una nueva rama para desarrollo:** Crea una rama `feature/team-feature`.

3. **Realizar cambios y enviar la rama al repositorio remoto:** Confirma los cambios y envía la rama.

4. **Abrir un Pull Request:** Abre un PR en la plataforma remota y describe los cambios.

5. **Revisar y Fusionar el Pull Request:** Simula la revisión y fusiona el PR en `main`.

6. **Eliminar la rama remota y local:** Elimina la rama tanto localmente como en el remoto.

---

## Ejercicio 6: Cherry-Picking y Git Stash

**Objetivo:** Aplicar commits específicos a otra rama y guardar cambios no confirmados.

### Instrucciones:

1. **Hacer cambios en `main.py` y confirmarlos:** Realiza cambios y confírmalos.

2. **Crear

 una nueva rama para aplicar cambios:** Crea una rama `feature/stash-feature`.

3. **Usar Git Stash:** Guarda cambios no confirmados usando `git stash`.

4. **Aplicar cambios específicos de otro commit:** Usa `git cherry-pick` para aplicar un commit específico a la nueva rama.

5. **Restaurar cambios guardados:** Usa `git stash pop` para aplicar cambios guardados.

---

Recuerda que Git es una herramienta poderosa para el control de versiones, y practicar estos ejercicios te ayudará a comprender mejor su funcionamiento. ¡Buena suerte!

--- 

Espero que esto se ajuste a lo que necesitas. Si deseas realizar más cambios o ajustes, házmelo saber.
