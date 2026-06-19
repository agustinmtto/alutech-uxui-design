# AluTech S.A. — Panel de Indicadores de Mejora

> Plataforma web empresarial UX/UI para el monitoreo de KPIs del proceso de gestión de venta de aberturas de **AluTech S.A.**, diseñada como herramienta de control y mejora continua.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## Descripción

Dashboard gerencial y operativo construido en un único archivo `index.html` (sin frameworks ni dependencias externas) que centraliza los **26 indicadores** definidos para medir los resultados de la mejora del proceso comercial de AluTech: desde diseño técnico y atención por chatbot IA, hasta logística, reclamos, ventas digitales, RRHH, capacitación y expansión nacional.

La interfaz comunica que la empresa cuenta con un sistema integrado para:

- Centralizar información de múltiples fuentes (ERP, CRM, Chatbot, Ruteo)
- Medir resultados con indicadores claros y trazables
- Comparar desempeño real contra metas
- Detectar desvíos y priorizar acciones correctivas
- Evaluar el impacto del chatbot IA, CRM, e-commerce, ruteo y capacitación
- Tomar decisiones gerenciales basadas en datos

---

## Características

- **Sidebar fijo** de 240 px con navegación entre 10 módulos de la plataforma
- **5 tarjetas KPI ejecutivas** con contadores animados y variación vs. período anterior
- **Biblioteca de 26 indicadores** filtrables por categoría + buscador en tiempo real
- **Modal de detalle** por KPI con objetivo, fórmula, fuente, responsable y gráfico histórico animado
- **3 bloques de análisis inferior**: Operativo diario · Táctico semanal · Gerencial mensual
- **Animaciones profesionales**: entrada escalonada, dibujo progresivo de sparklines (`stroke-dashoffset`), hover lifts, modal con backdrop blur, micro-interacciones en cada componente
- Paleta corporativa, tipografía **Inter** (Google Fonts), iconografía SVG lineal consistente

---

## Stack tecnológico

| Tecnología | Uso |
|------------|-----|
| **HTML5** | Estructura y marcado semántico |
| **CSS3 (inline)** | Variables CSS, layout flex/grid, animaciones `@keyframes` |
| **JavaScript vanilla** | Renderizado dinámico, lógica de tabs, búsqueda, modal |
| **SVG nativo** | Sparklines, minibars, gauges, donuts, progress bars con animaciones custom |
| **Google Fonts (Inter)** | Tipografía corporativa cargada desde CDN |

No requiere Node.js, npm ni build tool. Se abre directamente en el navegador.

---

## Uso

```bash
# Opción 1: abrir directamente en el navegador
# Hacer doble clic en index.html

# Opción 2: servir con cualquier servidor estático
npx serve .
# o
python -m http.server 8080
```

Abrir `http://localhost:8080` (o el puerto que indique tu servidor) en el navegador.

---

## Paleta de colores

| Token | Hex | Uso |
|-------|------|-----|
| Azul oscuro corporativo | `#0B2D5C` | Sidebar, títulos, bloque gerencial |
| Azul medio | `#1E63B6` | Acentos, ítem activo, links |
| Verde éxito | `#2E7D32` | Estado "En meta", deltas positivas |
| Naranja alerta | `#F26A21` | Estado "En seguimiento", franja activa del sidebar |
| Rojo riesgo | `#C62828` | Estado "Riesgo" |
| Gris texto | `#2B2B2B` | Texto principal |
| Gris secundario | `#6B7280` | Texto auxiliar y metadatos |
| Gris bordes | `#D9DEE7` | Bordes y separadores |
| Fondo claro | `#F5F7FA` | Fondo general del dashboard |

---

## KPIs implementados (26 indicadores en 8 categorías)

| Categoría | Indicadores |
|-----------|-------------|
| **A.** Diseño técnico y presupuestación | 3 |
| **B.** Atención online y chatbot IA | 4 |
| **C.** Logística y distribución | 3 |
| **D.** Reclamos y CRM | 6 |
| **E.** Ventas digitales y e-commerce | 3 |
| **F.** RRHH y retención de talento | 2 |
| **G.** Capacitación y calidad técnica | 3 |
| **H.** Expansión nacional | 2 |
| **Total** | **26** |

Cada KPI incluye: nombre, categoría, valor actual, meta, frecuencia de medición, fuente de datos, estado (semáforo) y mini gráfico de tendencia.

---

## Estructura del proyecto

```
alutech-uxui-design/
├── index.html     # Dashboard completo (HTML + CSS + JS en un solo archivo)
└── README.md
```

Todo el código vive en `index.html`, organizado en tres bloques:

1. `<style>` — Variables CSS, componentes, animaciones
2. `<body>` — Sidebar, header, contenido (renderizado por JS)
3. `<script>` — Datos (`KPIS`, `SUMMARY`, `BLOCKS`), utilidades SVG, funciones de render

---

## Personalización

### Cambiar el usuario logueado

En `index.html`, dentro del `<header>`, buscá el bloque `.user`:

```html
<div class="user">
  <img class="avatar" src="URL_DE_LA_FOTO" alt="Nombre del usuario" style="object-fit:cover;border:none;background:none;" />
  <div class="user-meta">
    <div class="name">Nombre Apellido</div>
    <div class="role">Rol del usuario</div>
  </div>
</div>
```

### Agregar o editar KPIs

El array `KPIS` (en el `<script>`) define todos los indicadores. Cada entrada incluye:

```js
{
  id, cat, name, catLabel,
  val, valNum, meta, freq, fuente,
  estado,     // 'good' | 'warn' | 'risk'
  viz,        // 'line' | 'bar' | 'gauge' | 'scale' | 'progress' | 'donut' | 'compare' | 'rank'
  trend,      // array de 8 valores para el gráfico histórico
  dir, good,  // dirección esperada de mejora ('up' | 'down')
  objG, objE, formula, horizonte, responsable, actualizado, obs
}
```

### Cambiar la paleta

Todas las variables de color están definidas en `:root` al inicio del `<style>`.

---

## Contexto del proyecto

Trabajo académico desarrollado en el marco de la carrera de **Ingeniería en Sistemas de Información** en la **UTN Facultad Regional Córdoba**, como parte de la solución IT de soporte al plan de mejora del proceso comercial de **AluTech S.A.**, empresa de aberturas con proyección de expansión nacional.

El dashboard se incluye como **anexo visual** de la propuesta de solución, mostrando cómo se materializaría el sistema de medición y control de los indicadores definidos en el trabajo.

---

## Licencia

MIT License — Proyecto académico de uso libre con atribución.

---

## Autor

**Gerónimo "Momo" Benavides**  
UTN Facultad Regional Córdoba
