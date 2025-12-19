# Guía de Sincronización con Netlify

## Opción 1: Netlify CLI (Más rápida desde Cursor)

### Instalación:
```bash
npm install -g netlify-cli
```

### Configuración inicial:
1. En Cursor, abre la terminal (Ctrl + `)
2. Ejecuta: `netlify login`
3. Se abrirá el navegador para autenticarte

### Desplegar por primera vez:
```bash
netlify init
```
- Te preguntará el directorio de publicación: presiona Enter (usa el actual)
- Te preguntará si quieres configurar un sitio nuevo o existente: elige "Create & configure a new site"
- Te pedirá un nombre para el sitio (opcional)

### Desplegar después de cambios:
```bash
netlify deploy
```
Esto crea una URL de "preview". Para producción:
```bash
netlify deploy --prod
```

## Opción 2: Git + GitHub (Sincronización automática) - RECOMENDADO

### Pasos:
1. Crea un repositorio en GitHub (desde github.com)
2. Inicializa Git en tu proyecto:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin TU_URL_DEL_REPOSITORIO
git push -u origin main
```

3. En Netlify:
   - Ve a tu panel
   - "Add new site" → "Import an existing project"
   - Conecta GitHub y selecciona el repositorio
   - Netlify detectará automáticamente el proyecto
   - Cada vez que hagas `git push`, Netlify actualizará automáticamente

4. Desde Cursor, cada vez que hagas cambios:
```bash
git add .
git commit -m "Descripción de los cambios"
git push
```

## Opción 3: Drag & Drop Manual
1. Ve a netlify.com
2. "Add new site" → "Deploy manually"
3. Arrastra la carpeta del proyecto
4. Repite cada vez que hagas cambios

---

**Recomendación:** Usa la Opción 2 (Git + GitHub) porque:
- Se actualiza automáticamente cuando haces cambios
- Tienes historial de versiones
- Puedes trabajar desde cualquier lugar
- Es gratis y fácil de configurar


