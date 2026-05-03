# 💰 Finanzas Personales — PWA

App de registro de gastos para Android (y cualquier navegador moderno).

## 📱 Instalación en Android

### Opción 1: GitHub Pages (recomendado, gratis)
1. Creá una cuenta en https://github.com
2. Creá un nuevo repositorio (ej: `finanzas-app`)
3. Subí todos los archivos de esta carpeta al repositorio
4. En Settings → Pages → Source: seleccioná `main` y `/root`
5. Tu app queda en: `https://TU_USUARIO.github.io/finanzas-app`
6. Abrí esa URL en Chrome de Android
7. Chrome mostrará un banner "Agregar a pantalla de inicio" → tocalo
8. ¡La app queda instalada como si fuera nativa!

### Opción 2: Netlify (drag & drop, sin cuenta de GitHub)
1. Andá a https://netlify.com
2. Arrastrá la carpeta completa al panel de Netlify
3. Obtenés una URL pública inmediatamente
4. Abrí esa URL en Chrome Android → instalá desde el banner

### Opción 3: Local en la red Wi-Fi
Si tenés Python instalado en tu PC:
```bash
cd finanzas-pwa
python -m http.server 8080
```
Luego abrí `http://IP_DE_TU_PC:8080` en Chrome de Android.

## 📁 Archivos incluidos

| Archivo | Descripción |
|---------|-------------|
| `index.html` | App completa (sin dependencias externas de build) |
| `manifest.json` | Configuración PWA (nombre, ícono, colores) |
| `sw.js` | Service Worker para funcionamiento offline |
| `icon-192.png` | Ícono de la app (192×192) |
| `icon-512.png` | Ícono splash screen (512×512) |

## ✨ Funcionalidades

- **Registrar gastos** con todos los campos de tu planilla:
  - Clasificación (Necesidad / Calidad de Vida / Disfrute / Contribución)
  - Concepto y Subconcepto (menús encadenados)
  - Detalle, Monto, Fecha, Origen, Gasto x, Mes Cash Out, Observaciones
- **Listar gastos** con filtros por mes y clasificación
- **Análisis** con totales, barras por clasificación y tabla pivot
- **Exportar a .xlsx** compatible con tu planilla:
  - Hoja "Base de datos" → formato idéntico al original
  - Hoja "Gastos Mes" → tabla pivot clasificación × subconcepto
- **Offline** → funciona sin internet después de la primera carga
- **Datos guardados** localmente en el dispositivo (localStorage)

## 🔄 Actualizar la planilla Excel

1. Descargá el `.xlsx` desde la pestaña Exportar de la app
2. Abrí `Finanzas_Personales_y_Templates.xlsx`
3. Copiá los datos de la hoja "Base de datos" del archivo exportado
4. Pegalos en la hoja "Base de datos" de tu planilla (fila 2 en adelante)
5. Clic derecho sobre la tabla dinámica → **Actualizar**
