# Mi Primer Dashboard

Este repositorio contiene un dashboard construido con [Quarto](https://quarto.org/) y Python, configurado para desplegarse automáticamente en GitHub Pages usando GitHub Actions.

## Prerrequisitos
- Quarto (para desarrollo local)
- Python 3.10+
- Dependencias definidas en `requirements.txt` (`pandas`, `numpy`, `plotly`, `jupyter`)

---

## 🚀 Cómo iniciar tu repositorio y hacer el Deploy

Sigue estos pasos detallados para subir tu código a GitHub y que se publique automáticamente tu Dashboard.

### 1. Iniciar el repositorio localmente

Abre tu terminal en la carpeta principal del proyecto (`mi-primer-dashboard`) y ejecuta los siguientes comandos:

```bash
# 1. Iniciar git en esta carpeta
git init

# 2. Agregar todos los archivos para el primer guardado
git add .

# 3. Crear el primer commit con un mensaje descriptivo
git commit -m "feat: configuración inicial, dashboard y deploy de github actions"

# 4. Asegurarse de que la rama principal se llama 'main'
git branch -M main
```

### 2. Crear el repositorio en GitHub y enlazarlo

1. Ve a [GitHub](https://github.com/) e inicia sesión en tu cuenta.
2. Crea un **Nuevo Repositorio** pulsando el botón de **+** en la esquina superior derecha o ve a [Crear Repositorio](https://github.com/new).
3. Ponle un nombre (ej. `mi-primer-dashboard`), déjalo como **Público** y **NO marques** la opción de agregar README (ya que ya tenemos uno).
4. Copia el enlace de tu nuevo repositorio y ejecuta en tu terminal:

```bash
# Conectar tu carpeta local con el repositorio de GitHub (reemplaza con tu enlace)
git remote add origin https://github.com/TU-USUARIO/mi-primer-dashboard.git

# Subir tu código a GitHub
git push -u origin main
```

### 3. Configurar GitHub Pages (El Deploy Automático)

Una vez que subas (hagas `push`) de tu código, **GitHub Actions** (gracias al archivo que creamos en `.github/workflows/deploy.yml`) comenzará a instalar Python, descargar tus librerías y renderizar tu Dashboard automáticamente. 

Para que tu sitio web sea visible en internet, configura **GitHub Pages**:

1. Ve a la pestaña **Settings** (Configuración) de tu repositorio en GitHub.
2. En el menú lateral izquierdo, haz clic en **Pages**.
3. En la sección **Build and deployment**, asegúrate de que **Source** esté configurado como **Deploy from a branch**.
4. En **Branch**, selecciona la rama llamada `gh-pages` (si no aparece al instante, espera un par de minutos a que termine la acción en la pestaña "Actions", recarga la página y aparecerá) y luego el folder `/ (root)`. Haz clic en **Save**.
5. ¡Listo! En la parte superior de esa misma sección de Pages, aparecerá el enlace a tu dashboard publicado (por ejemplo: `https://TU-USUARIO.github.io/mi-primer-dashboard/`).

---

## Desarrollo Local (Opcional)

Si quieres agregar gráficos o ver el dashboard localmente en tu computadora mientras haces cambios antes de subirlos a GitHub:

```bash
# Instalar las librerías necesarias de Python
pip install -r requirements.txt

# Renderizar y previsualizar tu dashboard con Quarto
quarto preview mi-primer-dashboard.qmd
```
