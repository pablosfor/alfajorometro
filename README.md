# 🍫 Alfajorómetro

El sistema democrático del dulce de leche.

## 🚀 Cómo publicar en GitHub Pages (paso a paso)

### Requisitos previos
- Una cuenta en [github.com](https://github.com) (gratis)
- [Node.js](https://nodejs.org) instalado (versión 18 o superior)
- Git instalado

---

### Paso 1 — Crear el repositorio en GitHub

1. Entrá a [github.com/new](https://github.com/new)
2. En **Repository name** escribí: `alfajorometro`
3. Dejalo en **Public**
4. **No** tildés ninguna opción extra (sin README, sin .gitignore)
5. Hacé click en **Create repository**

---

### Paso 2 — Configurar el nombre del repo en el proyecto

Abrí el archivo `vite.config.js` y verificá que `REPO_NAME` coincida exactamente con el nombre de tu repositorio:

```js
const REPO_NAME = 'alfajorometro'  // ← cambiá esto si usaste otro nombre
```

---

### Paso 3 — Instalar dependencias y configurar Git

Abrí una terminal en la carpeta del proyecto y ejecutá:

```bash
# Instalar dependencias
npm install

# Inicializar git
git init
git add .
git commit -m "🍫 Initial commit - Alfajorómetro"

# Conectar con GitHub (reemplazá TU_USUARIO con tu usuario de GitHub)
git remote add origin https://github.com/TU_USUARIO/alfajorometro.git
git branch -M main
git push -u origin main
```

---

### Paso 4 — Deployar a GitHub Pages

```bash
npm run deploy
```

Esto va a:
1. Buildear la app (`npm run build`)
2. Publicar la carpeta `dist/` en la rama `gh-pages`

Esperá 1-2 minutos y tu app va a estar disponible en:

```
https://TU_USUARIO.github.io/alfajorometro/
```

---

### Paso 5 — Activar GitHub Pages (solo la primera vez)

Si la URL no funciona todavía:

1. Andá a tu repo en GitHub
2. Click en **Settings** → **Pages**
3. En **Source** seleccioná la rama **gh-pages**
4. Guardá y esperá un par de minutos

---

## 🔄 Actualizar la app en el futuro

Si modificás el código:

```bash
git add .
git commit -m "actualización"
git push
npm run deploy
```

---

## ⚠️ Nota importante sobre los datos

Los votos se guardan en el **localStorage del navegador de cada participante**. Esto significa:

- ✅ Funciona perfectamente para una sola sesión de votación
- ✅ No requiere servidor ni base de datos
- ⚠️ Los votos son locales al dispositivo donde se vota (cada participante ve sus propios votos)
- ⚠️ El host debe tener la pestaña abierta para ver los votos en tiempo real

> **Para una experiencia completa multi-usuario** (donde todos los votos se sincronizan en un servidor central), se necesitaría un backend como Firebase, Supabase o similar. ¡Pedíselo a Claude!

---

## 🛠️ Correr en local (para testear)

```bash
npm run dev
```

La app abrirá en `http://localhost:5173`
