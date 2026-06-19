# AluTech S.A. — Panel de Indicadores de Mejora

> Plataforma web empresarial UX/UI para el monitoreo de KPIs del proceso de gestión de venta de aberturas de **AluTech S.A.**, diseñada como una herramienta SaaS corporativa real.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-38B2AC?logo=tailwind-css&logoColor=white)
![Lucide](https://img.shields.io/badge/Lucide-Icons-000000?logo=lucide&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 📋 Descripción

Dashboard gerencial y operativo que centraliza los **26 indicadores** definidos para medir los resultados de la mejora del proceso comercial de AluTech: desde diseño técnico y atención por chatbot IA, hasta logística, reclamos, ventas digitales, RRHH, capacitación y expansión nacional.

La interfaz comunica que la empresa cuenta con un sistema integrado para:

- Centralizar información de múltiples fuentes (ERP, CRM, Chatbot, Ruteo)
- Medir resultados con indicadores claros y trazables
- Comparar desempeño real contra metas
- Detectar desvíos y priorizar acciones correctivas
- Evaluar el impacto del chatbot IA, CRM, e-commerce, ruteo y capacitación
- Tomar decisiones gerenciales basadas en datos

---

## ✨ Características

- **Sidebar fijo** de 240 px con navegación entre los 10 módulos de la plataforma
- **5 tarjetas KPI ejecutivas** con contadores animados y variación vs. período anterior
- **Biblioteca de 26 indicadores** filtrables por categoría + buscador en tiempo real
- **Modal de detalle** por KPI con objetivo, fórmula, fuente, responsable y gráfico histórico animado
- **3 bloques de análisis inferior**: Operativo diario · Táctico semanal · Gerencial mensual
- **Animaciones profesionales**: entrada escalonada, dibujo progresivo de sparklines (`stroke-dashoffset`), hover lifts, modal con backdrop blur, micro-interacciones en cada componente
- Paleta corporativa, tipografía **Inter**, iconografía lineal consistente

---

## 🛠️ Stack tecnológico

| Tecnología | Uso |
|------------|-----|
| **React 18** | Componentes funcionales, hooks (`useState`, `useEffect`, `useRef`, `useMemo`) |
| **Tailwind CSS** | Utilidades de layout, spacing y tipografía |
| **Lucide React** | Iconografía lineal (LayoutDashboard, BarChart3, etc.) |
| **SVG nativo** | Sparklines y gráficos históricos con animaciones custom |
| **Vite** | Build tool y dev server |

---

## 🚀 Instalación

```bash
# Clonar el repositorio
git clone https://github.com/agustinmtto/alutech-uxui-design.git
cd alutech-uxui-design

# Instalar dependencias
npm install

# Levantar el servidor de desarrollo
npm run dev

# Build de producción
npm run build
npm run preview
```

Abrí `http://localhost:5173` (o el puerto que indique Vite) en el navegador.

---

## 🎨 Paleta de colores

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

## 📊 KPIs implementados (26 indicadores en 8 categorías)

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

## 📂 Estructura del proyecto

```
alutech-uxui-design/
├── src/
│   ├── components/
│   │   └── AluTechDashboard.jsx   # Componente principal del dashboard
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css                  # Tailwind directives
├── public/
├── index.html
├── package.json
├── tailwind.config.js
├── vite.config.js
└── README.md
```

---

## 🧩 Personalización

### Cambiar el usuario logueado
En `AluTechDashboard.jsx`, dentro del `<header>`, modificá el bloque del avatar:

```jsx
<img
  src="URL_DE_LA_FOTO"
  alt="Nombre del usuario"
  className="w-9 h-9 rounded-lg object-cover"
/>
<div>
  <div className="text-xs font-semibold leading-tight">Nombre Apellido</div>
  <div className="text-[10px]">Rol del usuario</div>
</div>
```

### Agregar o editar KPIs
El array `kpis` define todos los indicadores. Cada entrada incluye:

```js
{
  id, name, cat, value, target, freq, source,
  status,    // 'good' | 'tracking' | 'risk'
  trend,     // array de 7 valores para el sparkline
  obj, formula, resp, horizon, desc   // datos del modal
}
```

### Cambiar la paleta
El objeto `C` al inicio del componente concentra todos los colores en un solo lugar.

---

## 👤 Contexto del proyecto

Trabajo académico desarrollado en el marco de la carrera de **Ingeniería en Sistemas de Información** en la **UTN Facultad Regional Córdoba**, como parte de la solución IT de soporte al plan de mejora del proceso comercial de **AluTech S.A.**, empresa de aberturas con proyección de expansión nacional.

El dashboard se incluye como **anexo visual** de la propuesta de solución, mostrando cómo se materializaría el sistema de medición y control de los indicadores definidos en el trabajo.

---

## 📝 Licencia

MIT License — Proyecto académico de uso libre con atribución.

---

## ✍️ Autor

**Gerónimo "Momo" Benavides**  
UTN Facultad Regional Córdoba