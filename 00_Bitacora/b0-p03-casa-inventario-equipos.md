

- Alumno: Alvaro Garcia
- Bloque: 00018.04 
- Fase / ejercicio: Práctica B0.P03 Casa
- Fecha de inicio: 23/10/2026
- Fecha de entrega: 126/10/2026

### 🎯 Qué se pedía

Crear un inventario de equipos desde cero utilizando una bóveda de Obsidian (`Boveda_Inventario_Casa`) y un repositorio de Git (`sor-inventario-equipos-casa`). Había que registrar tres versiones sucesivas del producto (inventario inicial, actualización de estados y ampliación con documentación/imágenes), consultar la primera versión histórica antes de regresar a `main`, y cerrar la práctica con una bitácora detallada en un cuarto commit documental junto con su vídeo en una playlist.

### ⌨️ Comandos y pasos importantes

- `git --version` — Muestra la versión instalada de Git.
    
- `git init` — Inicializa un repositorio Git local en la carpeta de trabajo.
    
- `git branch -M main` — Nombra y fuerza la rama actual como `main`.
    
- `git remote add origin <url>` — Registra la URL SSH del repositorio remoto en GitHub.
    
- `git add <archivo>` — Prepara archivos específicos añadiéndolos al índice para el próximo commit.
    
- `git commit -m "mensaje"` — Guarda una versión local con un mensaje descriptivo.
    
- `git push` — Envía los commits locales al repositorio remoto en GitHub.
    
- `git status` — Consulta el estado del árbol de trabajo y los archivos preparados o sin seguimiento.
    
- `git diff` — Compara las modificaciones entre el disco y el índice.
    
- `git diff --cached` — Muestra el contenido preparado en el índice respecto al último commit.
    
- `git check-ignore -v <archivo>` — Identifica la regla y la línea del archivo excluido por `.gitignore`.
    
- `git switch --detach <código>` — Permite consultar temporalmente un commit histórico sin situarse en ninguna rama.
    
- `git switch main` — Regresa a la rama principal `main`.
    
- `git log --oneline` — Muestra el historial de commits en formato resumido.
    

### 🛠️ Qué he hecho

- Comprobación previa de la versión de Git, identidad del usuario y clave SSH.
    
- Creación de la bóveda de Obsidian `Boveda_Inventario_Casa` fuera de OneDrive y del árbol SOR, creando únicamente la estructura de carpetas inicial (`00_Grabaciones`, `01_Proyecto/00_Bitacora`, `01_Proyecto/inventario`).
    
- Creación de los archivos iniciales en `01_Proyecto`: `.gitignore`, `README.md`, `00_Bitacora/b0-p03-casa-inventario-equipos.md`, e `inventario/equipos.csv` con los datos de `EQ01` y `EQ02`.
    
- Inicialización de Git, establecimiento de la rama `main` y conexión con el repositorio remoto vacío en GitHub (`sor-inventario-equipos-casa`).
    
- Selección individual (`git add`), revisión (`git diff --cached`) y guardado de la primera versión (`git commit` y `git push`).
    
- Modificación de `inventario/equipos.csv` (cambio de ubicación de `EQ01` a Aula-3 y estado de `EQ02` a mantenimiento), seguida de su preparación, commit y push para la segunda versión.
    
- Ampliación del proyecto creando nuevas carpetas (`inventario/mantenimiento`, `inventario/imagenes`, `inventario/videos`), la ficha de `EQ02.md`, criterios de estados, adición de `EQ03` al CSV, actualización de `README.md`, captura de imagen `equipo.png` y copia de los clips locales de prueba (`revision-01.mp4`, `revision-02.mp4`).
    
- Verificación mediante `git status -short`, `git diff` y `git check-ignore`, asegurando que los vídeos están correctamente ignorados.
    
- Preparación individual de los 5 archivos de la ampliación, comprobación mediante `git diff --cached` y envío del tercer commit y push.
    
- Consulta del primer commit histórico en modo desacoplado (`git switch --detach`) para comprobar el estado antiguo de los datos y posterior regreso seguro a `main` (`git switch main`).
    
- Grabación de la sesión con OBS, guardado fuera de Git, subida del vídeo como No listado a la playlist con sus 9 marcas de tiempo, y cierre documental de la bitácora mediante un cuarto commit.
    

### 🚩 Qué me ha fallado y cómo lo he resuelto

Nada. Se siguieron rigurosamente las comprobaciones paso a paso de ruta (`pwd`), identidad, estado (`git status`) y revisión de diferencias (`git diff`) antes de cada operación para evitar errores de archivos no deseados o modificaciones en ramas incorrectas.

### 🤔 Respuestas a las preguntas

1. **¿Por qué el repositorio está en 01_Proyecto y no en la raíz de la bóveda?** Porque la bóveda de Obsidian almacena archivos de configuración y grabaciones pesadas o externas que no deben formar parte del control de versiones del código del proyecto.
    
2. **¿Qué dos celdas de datos cambiaste en la segunda versión y cómo se ven en diff?** Se cambió la ubicación de `EQ01` de `Aula-1` a `Aula-3` y el estado de `EQ02` de `disponible` a `mantenimiento`. En el `git diff`, la línea eliminada aparece con `-` y la nueva línea introducida con `+`.
    
3. **¿Qué diferencia hay entre editar una fila y preparar ese cambio con add?** Editar modifica el archivo en el disco local, mientras que `git add` actualiza el área de preparación (índice) seleccionando esos cambios para ser incluidos en el próximo commit.
    
4. **¿Por qué la ficha nueva aparece en status y no en el diff de equipos.csv?** Porque `EQ02.md` es un archivo nuevo sin seguimiento (`??`), y `git diff` solo compara cambios en archivos que ya están bajo seguimiento o control de Git.
    
5. **¿Qué archivos preparaste individualmente en la ampliación y qué mostró diff --cached?** Se prepararon individualmente `inventario/mantenimiento/EQ02.md`, `inventario/criterios-estados.md`, `inventario/imagenes/equipo.png`, `inventario/equipos.csv` y `README.md`. El comando `git diff --cached --stat` mostró el resumen de estos 5 archivos listos para el commit.
    
6. **¿Cómo demostraste que los clips existen y están ignorados sin subirlos?** Utilizando el comando `git check-ignore -v`, el cual identifica la regla exacta del `.gitignore` que los excluye, confirmando además en el explorador de archivos que seguían presentes en local sin ser rastreados.
    
7. **¿Qué ubicación y estado recuperaste al visitar el primer commit y qué ocurrió con EQ03?** Al visitar el primer commit (`--detach`), `EQ01` volvió a `Aula-1`, `EQ02` apareció como `disponible`, y `EQ03` no apareció porque fue añadido en una fase posterior.
    
8. **¿Por qué este CSV necesita historial y qué limitaciones tiene frente a un inventario multiusuario real?** Necesita historial para mantener la trazabilidad de las entregas y auditar qué cambios sufrieron los equipos. Sus limitaciones frente a un sistema multiusuario son la ausencia de control de concurrencia, bloqueos de edición simultánea, validación estricta de esquemas y permisos por roles en tiempo real.
    
9. **¿Cómo comprobaste la subida de la bitácora y por qué su cierre ocurre después del vídeo?** Se comprobó mediante `git status`, `git log --oneline` y la visualización directa del repositorio en GitHub. Su cierre ocurre después de la grabación porque la bitácora debe incluir obligatoriamente la URL real del vídeo publicado y sus marcas de tiempo definitivas.
## 🔗 Enlaces

- **Vídeo de esta fase:** https://youtu.be/XXXXXXXXXXX
- **Playlist:** B0_Prerrequisitos

## 💭 Dudas / a repasar

- (lo que no te ha quedado claro)