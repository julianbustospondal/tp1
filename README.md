# tp1

# Investigación sobre el archivo `.gitignore`

## 🔍 ¿Por qué es conveniente incluirlo?
El archivo `.gitignore` es un documento de texto que le indica a Git qué archivos o carpetas debe ignorar para no subirlos al repositorio. Es una buena práctica y es altamente conveniente porque:

* **Mantiene el repositorio limpio:** Evita subir archivos generados automáticamente durante la compilación de tu código (como los ejecutables `.exe` o los objetos `.o`). El repositorio solo debe contener el código fuente.
* **Protege información sensible:** Previene la subida accidental de contraseñas, claves de API o archivos de configuración locales que no deben ser públicos.
* **Ahorra espacio y evita conflictos:** Impide que se suban carpetas pesadas de dependencias o archivos ocultos del sistema operativo (como `Thumbs.db` en Windows), lo que hace que clonar el repositorio sea más rápido y evita conflictos entre distintos sistemas.

## ⏰ ¿Cuándo se debe hacer?
Lo ideal es crear y configurar el `.gitignore` **al inicio del proyecto**, justo después de inicializar el repositorio (`git init`) o clonarlo, y siempre **antes** de hacer tu primer `git add` y `git commit`. 

Si creas el `.gitignore` después de haber subido archivos que querías ignorar, Git los seguirá rastreando. Para solucionarlo, tendrías que eliminarlos de la caché de Git manualmente usando comandos adicionales (`git rm --cached`).

## ⚙️ ¿Cómo configuraría el archivo `.gitignore`?
Para configurarlo, se debe crear un archivo en la carpeta principal del proyecto llamado exactamente `.gitignore` (sin nombre antes del punto). Dentro del archivo, se escriben las reglas de lo que se desea ignorar, línea por línea. 

Se pueden usar patrones para ser más eficientes:
* `*.exe` (Ignora todos los archivos con esa extensión).
* `carpeta/` (Ignora todo el contenido de un directorio).

### Regla para ignorar `ignorado.txt`
Para cumplir con la consigna de ignorar un archivo específico llamado `ignorado.txt`, el contenido dentro del archivo `.gitignore` debe tener simplemente el nombre del archivo.