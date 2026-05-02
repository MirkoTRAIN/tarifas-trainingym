# Proceso Comercial · Trainingym

Guía interactiva del proceso de venta para el equipo comercial de Trainingym. Cubre todo el flujo: descubrimiento, diagnóstico, presentación de la solución, tarifas y cierre.

> 🌐 **Versión web pública** para acceso rápido del equipo desde cualquier dispositivo.

---

## 🚀 Cómo se usa

### Opción A — Online (recomendado)
Una vez subido a GitHub Pages, basta con abrir la URL pública (por ejemplo `https://tuusuario.github.io/proceso-comercial/`) desde el navegador. Funciona en escritorio, tablet y móvil.

### Opción B — Local
1. Descarga el repositorio (Code → Download ZIP) o clónalo con `git`.
2. Abre `index.html` con doble click. Funciona 100 % offline.

> ⚠️ **Importante:** los archivos `index.html`, `wizard-tarifas.html` y la carpeta `imgs/` deben estar **en la misma carpeta**.

---

## 📋 Estructura del proceso comercial

11 pasos que siguen el flujo natural de una conversación comercial:

| # | Paso | Para qué sirve |
|---|------|----------------|
| 1 | Perfil del comercial | Identidad, rol, tono y principios |
| 2 | Descubrimiento | Preguntas para conocer al cliente |
| 3 | Diagnóstico | Identificar pains y necesidades |
| 4 | Posicionamiento Trainingym | Argumentario de marca |
| 5 | Captación · Fidelización · Optimización | 3 pilares de valor |
| 6 | Producto en detalle | Funcionalidades por módulo |
| 7 | Validación con el cliente | Scripts de demo Easy / TG |
| 8 | **Presentación de tarifas** | Esquema de precios + Wizard |
| 9 | **Cierre** | Preguntas IUDB, Next step, CTA, Seguimiento |
| 10 | Catálogo de productos | Fichas técnicas de hardware |
| 11 | Wizard de tarifas (full screen) | Configurador de tarifa a pantalla completa |

---

## 🛠 Funcionalidades destacadas

### Paso 8 · Esquema básico de precios
- **Toggle Mensual / Anual** con cambio en vivo de los precios.
- Tablas de Easy Trainingym y Trainingym (gimnasios y cadenas).
- Cards de App e Implantación con popup *"Ver qué incluye"*.
- Sección de **Control de accesos** colapsable con fichas técnicas de cada componente.

### Paso 8 · Wizard de tarifas
- Configurador completo con todas las opciones (tier, sedes, App, Implantación, control de accesos).
- **Botón ⬇ Descargar resumen** → genera una imagen PNG con la tarifa lista para enviar al cliente.

### Paso 9 · Cierre · 4 sub-pestañas
1. **Preguntas de cierre** — esquema IUDB (Interés, Urgencia, Decisor, Budget) + 7 mejores preguntas
2. **Next step** — 5 escenarios (evaluar, negociar, firmar, nurturing, perdido) con botones de acción
3. **CTA** — 6 scripts de cierre por escenario + 4 acciones rápidas
4. **Seguimiento** — playbook de follow-up por canal y plazo

---

## 🌐 Cómo subirlo a GitHub Pages

### Opción 1 — Desde la web de GitHub (sin terminal)

1. Ve a [github.com/new](https://github.com/new) y crea un repositorio nuevo:
   - **Nombre del repositorio**: `proceso-comercial` (o el que prefieras)
   - **Visibilidad**: pública (necesario para GitHub Pages gratuito)
   - **No** marques "Add a README" (ya viene uno en el zip)

2. En la pantalla del repo recién creado, pulsa **"uploading an existing file"**.

3. **Arrastra todos los archivos del proyecto** al área de subida:
   - `index.html`
   - `wizard-tarifas.html`
   - `README.md`
   - La carpeta entera `imgs/` (arrástrala completa)

4. Pulsa **"Commit changes"**.

5. Activa GitHub Pages: ve a **Settings** → **Pages** (en el menú lateral).

6. En la sección "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: `main` · `/` (root)
   - Pulsa **Save**.

7. Espera 1–2 minutos. La URL aparecerá arriba: `https://tuusuario.github.io/proceso-comercial/`

8. **Comparte esa URL** con el equipo. Listo.

### Opción 2 — Desde terminal (si usas git)

```bash
# Inicializar repo en la carpeta del proyecto
cd ruta/al/proyecto
git init
git add .
git commit -m "Initial commit · Proceso Comercial Trainingym"

# Conectar al repo remoto (sustituye la URL)
git branch -M main
git remote add origin https://github.com/TU-USUARIO/proceso-comercial.git
git push -u origin main
```

Después activa GitHub Pages desde Settings → Pages como en el paso 5–7 de la opción 1.

### Actualizaciones futuras

Cada vez que hagas cambios:

```bash
git add .
git commit -m "Descripción del cambio"
git push
```

GitHub Pages se actualiza solo en 1–2 minutos.

---

## 📝 Datos de tarifas oficiales

| Producto | Precio |
|----------|--------|
| Easy Start (≤50 socios) | 99,90 €/mes |
| Easy Enterprise (51–150) | 169,90 €/mes |
| Easy Bronce (>150) | 189,90 €/mes |
| Trainingym Bronze (≤300) | 189,99 €/mes |
| Trainingym Silver (301–500) | 209,99 €/mes |
| Trainingym Gold (501–1000) | 239,99 €/mes |
| Trainingym Platinum (>1000) | 299,99 €/mes |
| App Pro | 49,99 €/mes |
| App Premium | 199,99 €/mes (+ 350 € setup) |
| Implantación Básico | 99 € |
| Implantación Avanzado | 265 € (+ 1 báscula 🎁) |
| Implantación Completo | 580 € (+ 3 básculas 🎁) |
| Torno de aspas | 1.330 € |
| Torno de pasillo | 3.300 € |
| Torno de pasillo premium | 5.199 € |
| Portillo SBT2000S | 1.400 € |
| Cerradura eléctrica | 50,90 € |
| Lector RFID/QR | 268,90 € |
| Controladora | 223,95 € |
| Pulsadores (salida / emergencia) | 28 € |
| Lector Face-ID | 696 € |
| Soporte Face-ID | 80 € |

**Pago anual**: −20 % sobre licencia + app.
**Multisede**: licencia × nº de sedes (≥6 sedes a medida).
**IVA**: solo aplica en España peninsular y Baleares.
**Instalación, transporte y obras** del hardware: a calcular por separado.

---

## 🔗 Pendiente de configurar

Algunos botones tienen un mensaje "🚧 Pendiente" porque aún no se han configurado los enlaces externos:

- **Enlace de free-trial de Trainingym** (paso 9 → Next step → "Quiere evaluar")
- **Enlace de calendario** del comercial real (paso 9 → Next step → "Quiere negociar")
- **Número de WhatsApp** del comercial (paso 9 → Next step → "Listo para firmar")

Cuando estén configurados, los botones llevarán directamente al recurso correspondiente.

---

## 🐛 Problemas comunes

**Q: El wizard no aparece dentro del paso 8**
A: Comprueba que `wizard-tarifas.html` está en la misma carpeta que `index.html`.

**Q: Los precios no cambian al pulsar Mensual / Anual**
A: Recarga con `Cmd + Shift + R` (Mac) o `Ctrl + F5` (Win) para limpiar caché.

**Q: El sidebar de pasos no aparece en móvil**
A: Pulsa el icono de menú (≡) arriba a la izquierda.

**Q: El botón "Descargar resumen" no funciona**
A: Asegúrate de tener un navegador moderno (Chrome, Edge, Safari, Firefox actualizados).

---

*Trainingym · Equipo comercial · Uso interno*
