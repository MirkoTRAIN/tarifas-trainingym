# Wizard de Tarifas · Trainingym

Configurador de tarifas online para clientes de Trainingym. Calcula tu propuesta personalizada en segundos.

> 🌐 Proyecto público e independiente. Listo para desplegar en GitHub Pages.

---

## 🎯 Qué hace

El wizard guía al usuario por unos pasos para configurar su solución Trainingym:

1. Tipo de negocio (Easy o Trainingym)
2. Número de clientes activos (slider)
3. Sedes
4. Personalización de la app móvil
5. Plan de puesta en marcha
6. Control de accesos (opcional)
7. Báscula adicional (opcional)
8. Modalidad de pago (mensual / anual −20%)

Y devuelve un **resumen personalizado** con:
- Pago inicial y cuota mensual/anual
- Desglose detallado de cada concepto
- Regalos incluidos
- Avisos sobre IVA, instalación, transporte
- **Botón de descarga** que genera una imagen PNG con el resumen para enviar al cliente

---

## 🚪 Pantalla de entrada (gate)

Antes de acceder al configurador, el usuario rellena un **formulario de HubSpot** con sus datos:
- Nombre
- Nombre del negocio fitness
- Modelo de negocio
- Email
- Teléfono / WhatsApp
- Qué necesita mejorar

Una vez enviado, el wizard se **pre-configura automáticamente** según el modelo de negocio que indicó (gimnasio → Trainingym, estudio/box → Easy Trainingym).

---

## 🚀 Cómo usarlo

### Online
Una vez desplegado en GitHub Pages: `https://tuusuario.github.io/wizard-tarifas-trainingym/`

### Local
1. Descarga el ZIP o clona el repo
2. Abre `index.html` con doble click en el navegador
3. Funciona offline (excepto el form de HubSpot, que requiere internet)

---

## 🌐 Cómo desplegarlo en GitHub Pages

### Opción 1 — Sin terminal

1. Crea un repo público en [github.com/new](https://github.com/new) llamado `wizard-tarifas-trainingym` (o el nombre que prefieras)
2. Sube todo el contenido del proyecto (arrastra y suelta los archivos en GitHub)
3. **Settings → Pages**:
   - **Source**: Deploy from a branch
   - **Branch**: `main` · `/` (root)
   - **Save**
4. Espera 1–2 min → tu URL pública estará lista

### Opción 2 — Con terminal

```bash
git init
git add .
git commit -m "Initial commit · Wizard de Tarifas Trainingym"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/wizard-tarifas-trainingym.git
git push -u origin main
```

Después activa GitHub Pages como en la opción 1.

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

## ⚙️ Stack técnico

- **HTML/CSS/JS vanilla** — sin frameworks
- **Tipografía**: Host Grotesk (Google Fonts)
- **Forms**: HubSpot Forms Embed v2
- **Identidad de marca**: oficial Trainingym ([trainingym.com/brand](https://trainingym.com/brand))

Todo en un solo archivo `index.html` — sin build, sin dependencias, sin servidor.

---

## 🐛 Problemas comunes

**El formulario inicial no carga**
Comprueba la conexión a internet. El form usa el script `https://js.hsforms.net/forms/embed/v2.js`. Si tras 6 segundos no carga, aparece un fallback con botón "Continuar al wizard".

**Aparece error de reCAPTCHA "el dominio no es válido"**
Esto ocurre cuando se abre el archivo en un dominio no autorizado en HubSpot. La solución oficial es:
- Subir el wizard a un dominio que esté en la lista blanca de HubSpot, o
- Pedir al admin de HubSpot que añada el nuevo dominio

El error está oculto visualmente pero sigue apareciendo en consola en algunos navegadores.

**El logo no aparece**
Si no hay conexión a internet, los logos oficiales de Trainingym (servidos desde el CDN de HubSpot) no cargan. El wizard cae a un fallback de texto/iniciales.

---

*Trainingym · La tecnología que hace crecer tu negocio fitness · [trainingym.com](https://trainingym.com)*
