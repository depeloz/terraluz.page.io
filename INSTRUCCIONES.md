# TerraLuz — Instrucciones de despliegue

## Archivos del proyecto
```
terraluz/
├── index.html      ← Página principal (hero, nosotros, valores, productos preview, QR)
├── productos.html  ← Catálogo completo de productos
└── INSTRUCCIONES.md
```

---

## OPCIÓN 1 — GitHub Pages (RECOMENDADA, gratis, sin dominio)

1. Crea una cuenta en https://github.com si no tienes una.
2. Crea un repositorio nuevo (ej: `terraluz`), que sea **público**.
3. Sube los dos archivos HTML:
   - En el repositorio, haz clic en "Add file" → "Upload files"
   - Arrastra `index.html` y `productos.html`
   - Haz clic en "Commit changes"
4. Ve a **Settings → Pages → Branch: main → Save**
5. En ~1 minuto tu sitio estará en:
   ```
   https://TU-USUARIO.github.io/terraluz/
   ```
6. Copia esa URL y pégala en el campo "Generar QR" de la página.
7. Descarga el QR con el botón "⬇ Descargar QR" para usarlo en tu presentación.

---

## OPCIÓN 2 — Red WiFi local (misma red, para presentación en sala)

### Requisitos: Python instalado

1. Abre una terminal/PowerShell en la carpeta `terraluz`
2. Ejecuta:
   ```bash
   python -m http.server 8080
   ```
3. Encuentra tu IP local:
   - Windows: `ipconfig` → "Dirección IPv4" (ej: 192.168.1.5)
   - Mac/Linux: `ifconfig` o `ip a`
4. En el celular (misma WiFi) ve a:
   ```
   http://192.168.1.5:8080
   ```
5. En la sección QR del sitio, escribe esa URL en el campo y genera el QR.

---

## OPCIÓN 3 — Netlify Drop (gratis, sin cuenta)

1. Ve a https://app.netlify.com/drop
2. Arrastra la carpeta `terraluz` completa
3. Obtienes una URL del tipo `https://algo-random.netlify.app`
4. ¡Listo! Úsala para generar el QR.

---

## Notas
- El QR se genera automáticamente con la URL actual de la página.
- Si abres el HTML directamente (doble clic), el QR mostrará una ruta local que no funciona en celular.
- Para que el QR funcione en celular, necesitas una URL HTTP (opciones 1, 2 o 3).
- Puedes agregar fotos reales de los productos reemplazando los emojis en el HTML.
