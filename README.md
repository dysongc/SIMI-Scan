[README.md](https://github.com/user-attachments/files/27608235/README.md)
# SIMI Scanner — Instrucciones de instalación

## Archivos incluidos
- `index.html` — App principal
- `manifest.json` — Configuración PWA
- `sw.js` — Service worker (funciona offline)

---

## OPCIÓN A: Abrir directo en Chrome (más rápido, piloto)

1. Copia la carpeta `simi_scanner` al dispositivo Android
2. Abre Chrome y escribe en la barra:
   `file:///sdcard/Download/simi_scanner/index.html`
3. Menú (⋮) → **"Añadir a pantalla de inicio"**
4. Se instala como ícono. Abre sin barra de Chrome.

---

## OPCIÓN B: Convertir a APK con PWABuilder (recomendado para distribución)

1. Sube la carpeta a un servidor web o usa GitHub Pages (gratis)
2. Ve a https://www.pwabuilder.com
3. Pega la URL del sitio → genera APK firmado
4. Descarga el APK e instálalo en el dispositivo

---

## Cómo cargar la maestra de productos

La maestra debe ser un archivo **CSV** con al menos estas columnas:
- `codigo` (o `sku`, `id`)
- `nombre` (o `name`, `descripcion`)
- `precio` (opcional)

Ejemplo:
```
codigo,nombre,precio
7891234567890,Paracetamol 500mg x20,1990
7891234567891,Ibuprofeno 400mg x10,2490
```

El separador puede ser coma (`,`) o punto y coma (`;`).

---

## Flujo de uso

1. Pantalla inicio → selecciona tipo (Recepción, Inventario, etc.)
2. Escribe nombre del archivo → carga maestra (opcional) → **Comenzar**
3. Presiona el botón físico del escáner → registra automáticamente
4. Botón "Omitir último" si escaneaste mal
5. "Exportar CSV" al terminar → archivo listo para importar a SIMI
