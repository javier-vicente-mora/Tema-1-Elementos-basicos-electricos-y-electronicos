# 🐙 Guía de Control de Versiones y Publicación en GitHub

Esta guía proporciona las instrucciones detalladas paso a paso para inicializar, gestionar y subir los apuntes didácticos al repositorio de GitHub del proyecto.

---

## 🎯 Repositorio Oficial de Destino
* **URL del repositorio:** `https://github.com/javier-vicente-mora/Tema-1-Elementos-b-sicos-el-ctricos-y-electr-nicos.git`

---

## 🚀 Paso 1: Primera Publicación del Proyecto

Sigue estos pasos en la terminal integrada de Visual Studio Code para subir por primera vez el proyecto completo a GitHub:

### 1. Abrir la terminal en la carpeta raíz del proyecto
Asegúrate de estar ubicado en el directorio principal del proyecto:
`C:\Users\javie\Desktop\Apuntes-1-Grado-Basico`

### 2. Inicializar el repositorio Git local
Si la carpeta aún no cuenta con Git configurado, inicialízala con:
```bash
git init
```
* **Explicación:** Crea una carpeta oculta `.git` donde se almacenará todo el historial de cambios del proyecto.

### 3. Añadir los archivos al área de preparación (Staging Area)
Añade todos los archivos y carpetas del proyecto:
```bash
git add .
```
* **Explicación:** Prepara todos los archivos (`.md`, imágenes, recursos) para ser incluidos en la próxima captura o *commit*.

### 4. Crear el primer commit
Registra los cambios en el historial local con un mensaje descriptivo:
```bash
git commit -m "Añadidos apuntes del Tema 1: Elementos básicos eléctricos y electrónicos"
```
* **Explicación:** Guarda una versión de los archivos en la base de datos local de Git.

### 5. Configurar la rama principal como `main`
Renombra la rama por defecto a `main`:
```bash
git branch -M main
```
* **Explicación:** Establece `main` como el nombre estándar de la rama principal, compatible con las convenciones actuales de GitHub.

### 6. Vincular el repositorio local con el remoto en GitHub
Asocia tu repositorio local con la URL remota de GitHub:
```bash
git remote add origin https://github.com/javier-vicente-mora/Tema-1-Elementos-b-sicos-el-ctricos-y-electr-nicos.git
```
* **Explicación:** Crea el alias `origin` que apunta a la dirección de tu repositorio en la nube.

### 7. Realizar el primer push a GitHub
Sube la rama principal y establece el seguimiento remoto:
```bash
git push -u origin main
```
* **Explicación:** Transfiere todos los commits locales al repositorio remoto en GitHub. El parámetro `-u` vincula la rama `main` local con la remota para futuros comandos.

---

## 🔄 Paso 2: Actualizaciones Posteriores y Añadir Nuevos Temas

Cuando agregues nuevos contenidos, modifiques temas existentes o añadas nuevas imágenes, utiliza el siguiente flujo de trabajo simplificado:

### 1. Comprobar el estado del repositorio
```bash
git status
```
* **Explicación:** Muestra qué archivos se han modificado, cuáles son nuevos o están pendientes de incluir.

### 2. Añadir los cambios
```bash
git add .
```
* **Explicación:** Prepara todos los cambios recientes. Si solo quieres añadir un tema específico, puedes usar `git add Tema-01/`.

### 3. Crear el commit de actualización
```bash
git commit -m "Actualización: Añadido nuevo apartado práctico en Tema 1"
```
* **Explicación:** Registra los nuevos cambios con un mensaje claro.

### 4. Subir las actualizaciones a GitHub
```bash
git push
```
* **Explicación:** Envía los nuevos commits a la rama `main` de GitHub sin necesidad de repetir los parámetros de configuración inicial.

---

## 🖼️ Paso 3: Gestión de Imágenes y Recursos Multimedia

Para mantener las imágenes sincronizadas y visibles correctamente en GitHub:

1. **Guardar las imágenes** en la carpeta correspondiente (`Tema-01/img/`).
2. **Referenciarlas en Markdown** con rutas relativas:
   ```markdown
   ![Descripción de la imagen](./img/nombre-imagen.png)
   ```
3. **Añadir las imágenes a Git** mediante:
   ```bash
   git add Tema-01/img/
   git commit -m "Añadidas imágenes explicativas del Tema 1"
   git push
   ```

---

## ⚠️ Recomendaciones de Seguridad
* **No subir credenciales ni claves:** Asegúrate de no incluir contraseñas ni datos sensibles.
* **Confirmación de comandos:** No ejecutes comandos de borrado masivo ni `git push --force` sin verificar previamente el estado de tu trabajo.
