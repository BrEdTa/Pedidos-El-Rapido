# Guía de Sincronización con GitHub y Netlify

## Paso 1: Crear el repositorio en GitHub
✅ Ya lo estás haciendo - solo asegúrate de NO marcar "Add README" (ya tienes uno)

## Paso 2: Conectar tu proyecto local con GitHub

Una vez creado el repositorio en GitHub, ejecuta estos comandos en la terminal de Cursor:

```bash
# 1. Inicializar Git (si aún no lo has hecho)
git init

# 2. Agregar todos los archivos
git add .

# 3. Hacer el primer commit
git commit -m "Initial commit: Pedidos El Rapido con logo y tema oscuro"

# 4. Conectar con GitHub (reemplaza TU_USUARIO con tu usuario de GitHub)
git remote add origin https://github.com/TU_USUARIO/Pedidos-El-Rapido.git

# 5. Cambiar a la rama main
git branch -M main

# 6. Subir el código a GitHub
git push -u origin main
```

**Nota**: Reemplaza `TU_USUARIO` con tu nombre de usuario de GitHub (veo que es "BrEdTa" en la imagen).

## Paso 3: Conectar GitHub con Netlify

1. Ve a [netlify.com](https://www.netlify.com) e inicia sesión
2. En el panel, haz clic en "Add new site" → "Import an existing project"
3. Selecciona "GitHub" y autoriza Netlify
4. Busca y selecciona el repositorio "Pedidos-El-Rapido"
5. Netlify detectará automáticamente que es un sitio estático
6. En "Publish directory" deja vacío (o pon `.` si te lo pide)
7. Haz clic en "Deploy site"

## Paso 4: Actualizaciones automáticas

Cada vez que hagas cambios:

```bash
git add .
git commit -m "Descripción de los cambios"
git push
```

Netlify actualizará automáticamente tu sitio en unos segundos. ✅


