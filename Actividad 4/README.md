# Actividad 4: Manejo de Repositorios

## Documentación
El procedimiento no se ha documentado, ya que se realizó en clase el **09/09/2024**.

## Objetivo
Integrar varios repositorios con ejercicios específicos en un único repositorio del curso (`CC3S2`) de manera organizada y manteniendo el historial de commits.

## Solución
Se utiliza `git subtree`, que permite integrar el contenido de un repositorio en otro sin perder el historial de commits. 

### Pasos Generales
1. Posicionarse en el directorio principal.
2. Agregar el repositorio como _remote_.
3. Integrar el repositorio usando `git subtree`.
4. Eliminar el _remote_.

### Ejemplo de Comandos
```shell
cd C:\Users\ismae\Documents\GitHub\CC3S2
git remote add auto-merge file:///C:/Users/ismae/Desktop/CC3S2/try-auto-merge
git subtree add --prefix="Actividad 4/try-auto-merge" auto-merge main
git remote remove auto-merge
```

---

# Ejercicios

## Ejercicio 1: Clona un repositorio Git con múltiples ramas

1. Clonar el repositorio [ejercicio-fusionar](https://github.com/al-2100/ejercicio-fusionar).
2. Revisar el contenido de `archivo.txt` en `master`, `rama1`, y `rama2`.
3. Aplicar `git merge --ff` entre `master` y `rama1`.
4. Revisar los cambios en `master`.

### Pregunta
**¿En qué situaciones recomendarías evitar el uso de git merge --ff?**
- Cuando se desea mantener una historia clara de las ramas.
- Para asegurarse de que hay un registro de la integración de características.

**Desventajas:**
- El historial lineal puede ocultar la historia de las fusiones.
- Dificulta el seguimiento de los cambios.

---

## Ejercicio 2: Simula un flujo de trabajo de equipo

1. Usar `--no-ff` con `master` y `rama2`.
2. Revisar los cambios.

### Preguntas
**¿Ventajas de utilizar git merge --no-ff?**
- Mantiene un historial de ramas más claro.
- Facilita la identificación de integraciones de características.

**¿Problemas al depender excesivamente de commits de fusión?**
- Puede resultar en un historial más complejo si se usa en exceso.

---

## Ejercicio 3: Crea múltiples commits en una rama.

1. Hacer varios cambios en una rama `feature`.
2. Fusionar la rama usando `git merge --squash`.

### Pregunta
**¿Cuándo es recomendable utilizar una fusión squash?**
- Para consolidar varios commits en uno solo, manteniendo un historial limpio.

**Ventajas para proyectos grandes:**
- Simplifica el historial al evitar commits triviales.

---

## Ejercicio 4: Resolver conflictos en una fusión non-fast-forward

1. Crear un nuevo repositorio, añadir un archivo `index.html` y realizar commits en las ramas.
2. Aplicar merge con `--no-ff`.
3. Resolver conflictos.

### Preguntas
1. **Pasos adicionales para resolver el conflicto:**
   - Abrir `index.html`, encontrar marcas de conflicto y combinar cambios.

2. **Estrategias para evitar conflictos:**
   - Trabajar en ramas de características.
   - Mantener el repositorio local actualizado.
   - Buena comunicación en el equipo.

---

## Ejercicio 5: Comparar los historiales con git log

1. Crear un nuevo repositorio y realizar varios commits en dos ramas.
2. Fusionar `feature-1` usando _fast-forward_ y `feature-2` usando _non-fast-forward_.
3. Crear `feature-3` con múltiples commits y fusionarla usando _squash_.
4. Comparar el historial de git.

### Preguntas
1. **¿Cómo se ve el historial en cada tipo de fusión?**
   - _Fast-forward:_ Sin commit de fusión.
   - _Non-fast-forward:_ Con commit de fusión.
   - _Squash:_ Un único commit que representa todos los cambios.

2. **Métodos preferidos en diferentes escenarios:**
   - _Fast-forward:_ Para mantener un historial simple.
   - _Non-fast-forward:_ Para un registro claro de fusiones.
   - _Squash:_ Para limpiar el historial antes de fusionar.

---

## Ejercicio 6: Fusión remota en un repositorio colaborativo

1. Regresar al repositorio _ejercicio-fusionar_.
2. Crear una nueva rama y realizar cambios.
3. Hacer push a la rama.
4. Simular la fusión desde GitHub creando un pull request y aceptándolo.

### Preguntas
1. **¿Cómo cambia la estrategia de fusión al colaborar?**
   - Requiere coordinación y el uso de Pull Requests.

2. **Problemas comunes al integrar ramas remotas:**
   - Conflictos de fusión y desincronización del repositorio.

---

## Ejercicio final: flujo de trabajo completo

1. Configurar un proyecto simulado y crear un repositorio.
2. Crear ramas y realizar cambios en `feature1` y `feature2`.
3. Realizar fusiones utilizando diferentes métodos.
4. Analizar el historial de commits.

### Análisis
- **Fast-forward:** Limpio pero sin detalles de desarrollo.
- **Non-fast-forward:** Mantiene el registro de fusiones.
- **Squash:** Compacta cambios en un solo commit.

---

Espero que este formato sea útil y claro para ti. Si necesitas ajustes adicionales, házmelo saber.
