

- **Alumno:** Islem benbeztout
- **Bloque:** B0 — Prerrequisitos
- **Fase / ejercicio:** Fase 0.8
- **Fecha de inicio:** 26/10/2026
- **Fecha de entrega:** 26/10/2026

---

## 🎯 Qué se pedía

Crear desde cero una bóveda llamada `Boveda_HTML_Casa` con su propio repositorio Git en `01_Proyecto`, conectar un repositorio remoto en GitHub (`sor-web-prestamo-portatiles-casa`) por SSH y guardar tres versiones evolutivas de una web interna de préstamo de portátiles[1][2]. Asimismo, realizar las comprobaciones del entorno, verificar el archivo `.gitignore` para archivos multimedia, inspeccionar el historial navegando entre commits y registrar un vídeo explicativo del proceso[1].
## ⌨️ Comandos y pasos importantes

- `git --version`, `git config --global user.name / user.email`, `ssh -T git@github.com` — Comprueban la versión de Git instalada, la identidad global asignada al autor de los commits y la autenticación SSH con GitHub antes de iniciar el proyecto[6][7].
- `pwd` — Muestra la ruta de trabajo actual para verificar que se está dentro de `Boveda_HTML_Casa/01_Proyecto` antes de inicializar Git[8].
- `git init` — Inicializa el repositorio local Git dentro de la carpeta `01_Proyecto`[9].
- `git branch -M main` — Renombra y establece la rama principal como `main`[9].
- `git status` / `git status --short --untracked-files=all` — Muestra el estado del árbol de trabajo (archivos sin seguimiento, modificados o preparados en el área de preparación)[9][10].
- `git remote add origin git@github.com:USUARIO/sor-web-prestamo-portatiles-casa.git` — Registra la dirección remota SSH de GitHub asociada al proyecto[11].
- `git remote -v` — Verifica las URLs de lectura y envío configuradas para el remoto `origin`[11].

## 🛠️ Qué he hecho

- **Comprobación inicial:** Inicié la grabación en OBS y ejecuté en Git Bash los comandos `git --version`, `git config` y `ssh -T git@github.com` para verificar disponibilidad, identidad y clave SSH[3][6].
- **Estructura e inicialización:** Creé en Obsidian la bóveda `Boveda_HTML_Casa` con las carpetas `00_Grabaciones` (fuera de Git), `01_Proyecto`, `01_Proyecto/00_Bitacora` y `01_Proyecto/web`[2][20].
- **Ficheros iniciales:** Configuré el archivo `.gitignore` para excluir archivos `.mp4`, `.mkv`, etc., y creé la primera versión de `web/index.html` ("Equipo 01: disponible.")[21][22].
- **Primera entrega (Versión 1):** Accedí a `01_Proyecto`, comprobé con `pwd`, ejecuté `git init`, renombré a `main`, vinculé el remoto `origin` en GitHub y realicé el primer `git commit` y `git push`[8].
- **Segunda entrega (Versión 2):** Modifiqué `index.html` para cambiar el estado a "Equipo 01: reservado para mantenimiento.", verifiqué el cambio con `git diff` y subí el segundo commit[15][23].
- **Ampliación y prueba de exclusiones (Versión 3):** Creé las páginas `normas.html`, `contacto.html`, la carpeta `imagenes/` con `portatil.png` y la carpeta `videos/` con dos clips `.mp4`[24][25]. Comprobé con `git check-ignore` que los vídeos quedaban ignorados[4].
- **Confirmación de la ampliación:** Preparé cada uno de los 4 archivos individualmente con `git add`, revisé la selección con `git diff --cached --stat` y subí la tercera entrega a GitHub[13].
- **Navegación por el historial:** Consulté el historial con `git log --oneline`, cambié temporalmente al primer commit mediante `git switch --detach` para verificar la versión inicial en el navegador y regresé a `main` con `git switch main`[5].
- **Cierre:** Detuve la grabación, subí el vídeo a YouTube como "No listado", completé las marcas de tiempo en la descripción y registré el commit documental final con la bitácora actualizada[30].

## 🚩 Qué me ha fallado y cómo lo he resuelto

copiar del pdf en vez de github pero luego lo solucione

## 🤔 Respuestas a las preguntas

- **¿Por qué** **git init** **se hizo en** **01_Proyecto** **y no en la raíz de la bóveda?** Se ejecutó en `01_Proyecto` porque es la única carpeta destinada al código del proyecto web y su documentación cuyo historial debe ser controlado por Git[2]. La raíz de la bóveda (`Boveda_HTML_Casa`) contiene la configuración interna de Obsidian (`.obsidian/`) y la carpeta de grabaciones de vídeo (`00_Grabaciones/`), las cuales deben permanecer fuera del control de versiones[2].
- **¿Qué mostró** **git status** **antes de** **add** **, después de** **add** **y después de** **commit** **?**
- **Antes de** **add** **:** Mostró los archivos como no seguidos (_untracked_) `??` o como modificados no preparados `[ ]M`[9][33].
- **Después de** **add** **:** Mostró los archivos preparados en el área de preparación (_index / staged_), marcados como `A[ ]` (archivos nuevos preparados) o `M[ ]` (modificaciones preparadas)[33][34].
- **Después de** **commit** **:** Mostró un estado limpio (_working tree clean_), indicando que no quedaban cambios pendientes en el árbol de trabajo[18][34].
- **¿Por qué creaste un repositorio de GitHub propio y lo conectaste con** **git remote add origin** **?** Porque se requería alojar un repositorio remoto independiente en GitHub (`sor-web-prestamo-portatiles-casa`) para publicar, respaldar y compartir el historial de entregables del proyecto[1]. El comando `git remote add origin` vincula la dirección SSH local con ese repositorio remoto específico para poder subir los commits mediante `git push`[11].
- **¿Por qué las páginas nuevas aparecen en** **git status** **pero no en** **git diff -- web/index.html** **?** `git status` muestra el estado general de todos los archivos del repositorio, incluidos los archivos nuevos sin seguimiento[10][14]. En cambio, `git diff -- web/index.html` compara exclusivamente las modificaciones realizadas en el archivo `index.html` frente a su versión en el índice o último commit, por lo que no muestra otros archivos nuevos sin seguimiento[10][14].
- **¿Cómo has comprobado que los vídeos existen pero no se van a subir?** Mediante el comando `git check-ignore -v web/videos/revision-01.mp4 web/videos/revision-02.mp4`[4]. Este comando confirma qué regla del archivo `.gitignore` (`*.mp4`) y en qué línea se está aplicando para ignorar ambos archivos de vídeo[4]. También se verificó en el gestor de archivos que los vídeos siguen presentes localmente en el disco[4].
- **¿Qué muestra** **git diff --cached --stat** **después de preparar los cuatro archivos?** Muestra un resumen estadístico de los cambios preparados en el índice (_staged_), detallando la lista de los cuatro archivos seleccionados (portada `index.html`, `normas.html`, `contacto.html` e imagen `portatil.png`) junto con el número de líneas añadidas o modificadas en cada uno[16][17].
- **¿Qué cambia al visitar el primer commit y qué recuperas al volver a** **main** **?**
- **Al visitar el primer commit (** **git switch --detach

## 🔗 Enlaces

- **Vídeo de esta fase:** 
- **Playlist:** 

## 💭 Dudas / a repasar
(Sin dudas pendientes)