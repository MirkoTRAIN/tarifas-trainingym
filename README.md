# Wizard de Tarifas · Trainingym

Configurador público de tarifas para clientes de Trainingym. Calcula tu propuesta personalizada en segundos.

> 🌐 Wizard standalone diseñado para recibir leads desde un formulario de HubSpot vía redirect.

---

## 🎯 Cómo funciona el flujo completo

```
┌──────────────────────┐    Submit    ┌──────────────────────┐
│   FORMULARIO         │ ───────────> │   WIZARD TARIFAS     │
│   en HubSpot         │  redirect    │   (esta web pública) │
│   con datos cliente  │  con params  │                      │
│                      │              │  - Lee URL params    │
│  - nombre            │              │  - Personaliza       │
│  - empresa           │              │  - Pre-configura     │
│  - modelo negocio    │              │  - Genera PNG con    │
│  - email             │              │    nombre + negocio  │
│  - teléfono          │              │                      │
└──────────────────────┘              └──────────────────────┘
```

El usuario rellena el formulario en una landing de HubSpot → al enviarlo, HubSpot lo **redirige** al wizard pasándole los datos por URL → el wizard lee esos datos y se personaliza automáticamente.

---

## ⚙️ Cómo configurar la redirección en HubSpot

En tu formulario de HubSpot:

1. Ve a **Forms → tu formulario → Settings → What should happen after a visitor submits this form?**
2. Selecciona **Redirect to another page**
3. Pega la URL del wizard con los parámetros que quieres pasarle. HubSpot soporta tokens como `{{contact.firstname}}`:

```
https://tuusuario.github.io/wizard-tarifas-trainingym/?firstname={{contact.firstname}}&lastname={{contact.lastname}}&company={{contact.company}}&modelo={{contact.modelo_de_negocio}}&email={{contact.email}}
```

El wizard detecta automáticamente los siguientes parámetros (case-insensitive, busca por palabra clave):

| Parámetro | Para qué sirve |
|---|---|
| `firstname`, `first_name`, `nombre` | Nombre del cliente (aparece en banner y PNG) |
| `lastname`, `last_name` | Apellido del cliente |
| `company`, `empresa`, `negocio`, `business` | Nombre del negocio (aparece destacado en PNG) |
| `modelo`, `tipo_de_negocio` | Pre-configura wizard (gimnasio→TG, estudio/box→Easy) |

---

## 🚀 Cómo usarlo

### Online (recomendado)
Despliega en GitHub Pages → la URL pública la pones en el redirect del form de HubSpot.

### Local / pruebas
Abre `index.html` en el navegador.

Para probar la personalización con datos de cliente, añade los parámetros a la URL manualmente:

```
file:///ruta/al/index.html?firstname=Juan&company=Gimnasio%20La%20Vega&modelo=gimnasio
```

---

## 🌐 Cómo desplegar en GitHub Pages

1. Crea un repo público en [github.com/new](https://github.com/new) → nombre: `wizard-tarifas-trainingym`
2. **Sin terminal**: arrastra los archivos `index.html`, `README.md`, `.gitignore` al repo
3. **Settings → Pages**: Source `Deploy from a branch` → Branch `main` `/` (root) → **Save**
4. Espera 1–2 min → tu URL pública estará lista
5. Copia esa URL y úsala en la redirección del form de HubSpot (ver sección anterior)

---

## 🧰 Lo que hace el wizard

Configurador de:
- Tipo de negocio (Easy o Trainingym)
- Número de clientes activos (slider)
- Sedes
- Personalización de la app móvil (Starter / Pro / Premium)
- Plan de puesta en marcha (Básico / Avanzado / Completo)
- Control de accesos (tornos, lectores, Face-ID)
- Báscula adicional
- Modalidad de pago (mensual / anual −20%)

Devuelve un **resumen visual personalizado** con:
- Pago inicial y cuota mensual/anual
- Desglose detallado de cada concepto
- Regalos incluidos (báscula Balance Pro)
- Avisos sobre IVA, instalación, transporte
- **Botón ⬇ Descargar resumen** que genera una imagen PNG con:
  - Banda "PREPARADO PARA [nombre del negocio + nombre del cliente]"
  - Logo oficial Trainingym
  - Todos los conceptos detallados
  - Tipografía y colores de marca

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

- **HTML/CSS/JS vanilla** — sin frameworks, sin dependencias
- **Tipografía**: Host Grotesk (Google Fonts)
- **Identidad de marca**: oficial Trainingym ([trainingym.com/brand](https://trainingym.com/brand))

Todo en un solo archivo `index.html`. No requiere build, ni servidor, ni base de datos.

---

*Trainingym · La tecnología que hace crecer tu negocio fitness · [trainingym.com](https://trainingym.com)*
