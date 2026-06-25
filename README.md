# AluTech S.A. — Panel de Indicadores de Mejora

> Plataforma web empresarial UX/UI para el monitoreo de KPIs del proceso de gestión de venta de aberturas de **AluTech S.A.**, diseñada como herramienta de control y mejora continua.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5\&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3\&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript\&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## Descripción

Dashboard gerencial y operativo construido en un único archivo `index.html` —sin frameworks ni dependencias externas— que centraliza los **26 indicadores** definidos para medir los resultados de la mejora del proceso comercial de AluTech: desde diseño técnico y atención por chatbot IA, hasta logística, reclamos, ventas digitales, RRHH, capacitación y expansión nacional.

La interfaz comunica que la empresa cuenta con un sistema integrado para:

* Centralizar información de múltiples fuentes: ERP, CRM, Chatbot, Ruteo y App Móvil de Choferes.
* Medir resultados con indicadores claros y trazables.
* Comparar desempeño real contra metas.
* Detectar desvíos y priorizar acciones correctivas.
* Evaluar el impacto del chatbot IA, CRM, e-commerce, ruteo, capacitación y seguimiento logístico.
* Tomar decisiones gerenciales basadas en datos.

---

## Características

* **Sidebar fijo** de 240 px con navegación entre 10 módulos de la plataforma.
* **5 tarjetas KPI ejecutivas** con contadores animados y variación vs. período anterior.
* **Biblioteca de 26 indicadores** filtrables por categoría + buscador en tiempo real.
* **Modal de detalle** por KPI con objetivo, fórmula, fuente, responsable y gráfico histórico animado.
* **3 bloques de análisis inferior**: Operativo diario · Táctico semanal · Gerencial mensual.
* **App Móvil para Choferes** incluida como módulo complementario dentro del repositorio.
* **Animaciones profesionales**: entrada escalonada, dibujo progresivo de sparklines (`stroke-dashoffset`), hover lifts, modal con backdrop blur y micro-interacciones en cada componente.
* Paleta corporativa, tipografía **Inter** desde Google Fonts e iconografía SVG lineal consistente.

---

## Módulo adicional: App Móvil para Choferes

El repositorio incluye una carpeta adicional con la **App Móvil para Choferes de AluTech S.A.**, pensada como prototipo funcional para acompañar la mejora logística del proceso.

La app permite representar cómo los choferes podrían consultar y actualizar información de entregas en tiempo real, conectando la operación en ruta con el sistema central de la empresa.

### Objetivo de la app

La App Móvil para Choferes busca mejorar la trazabilidad logística, reducir errores en la hoja de ruta y permitir que el estado del pedido se actualice desde la ruta.

Este módulo se relaciona directamente con la propuesta de mejora, ya que permite:

* Consultar la hoja de ruta diaria.
* Visualizar entregas asignadas.
* Ver estado de cada pedido.
* Confirmar entregas realizadas.
* Reportar demoras o novedades.
* Registrar entregas fallidas.
* Sincronizar información con ERP, CRM y sistema de ruteo.
* Mejorar el seguimiento operativo y la experiencia del cliente.

### Funcionalidades principales

* Vista móvil responsive.
* Pantalla de inicio para chofer.
* Resumen de ruta del día.
* Listado de entregas asignadas.
* Estado de cada entrega:

  * Pendiente.
  * En camino.
  * Entregada.
  * Con novedad.
* Mapa o representación visual simulada de recorrido.
* Botones de acción para:

  * Iniciar recorrido.
  * Confirmar entrega.
  * Reportar novedad.
  * Ver detalle del pedido.
* Sección de sincronización con sistemas internos.
* Estética visual alineada al dashboard principal de AluTech.

### Uso desde el celular

Como la app está desarrollada en HTML, CSS y JavaScript, puede utilizarse directamente desde un navegador móvil.

Opciones recomendadas:

1. Subir la carpeta de la app a Netlify, Vercel o GitHub Pages.
2. Abrir el link generado desde el celular.
3. Agregar el sitio a la pantalla principal del teléfono.

En Android:

```text
Chrome → Menú de tres puntos → Agregar a pantalla principal
```

En iPhone:

```text
Safari → Compartir → Agregar a pantalla de inicio
```

De esta forma, la app se puede presentar como una aplicación móvil durante la exposición, aunque técnicamente sea un prototipo web responsive.

---

## Stack tecnológico

| Tecnología               | Uso                                                                   |
| ------------------------ | --------------------------------------------------------------------- |
| **HTML5**                | Estructura y marcado semántico                                        |
| **CSS3 (inline)**        | Variables CSS, layout flex/grid, animaciones `@keyframes`             |
| **JavaScript vanilla**   | Renderizado dinámico, lógica de tabs, búsqueda, modal e interacciones |
| **SVG nativo**           | Sparklines, minibars, gauges, donuts, progress bars e iconografía     |
| **Google Fonts (Inter)** | Tipografía corporativa cargada desde CDN                              |

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

Abrir `http://localhost:8080` —o el puerto que indique tu servidor— en el navegador.

---

## Uso de la App Móvil para Choferes

Si la carpeta de la app está dentro del repositorio, ingresar a:

```bash
alutech_choferes_app/
```

Y abrir:

```bash
index.html
```

También puede servirse localmente:

```bash
cd alutech_choferes_app
python -m http.server 8081
```

Luego abrir:

```bash
http://localhost:8081
```

Para probarla desde el teléfono, se recomienda desplegar esa carpeta en Netlify, Vercel o GitHub Pages.

---

## Paleta de colores

| Token                   | Hex       | Uso                                                |
| ----------------------- | --------- | -------------------------------------------------- |
| Azul oscuro corporativo | `#0B2D5C` | Sidebar, títulos, bloque gerencial                 |
| Azul medio              | `#1E63B6` | Acentos, ítem activo, links                        |
| Verde éxito             | `#2E7D32` | Estado "En meta", deltas positivas                 |
| Naranja alerta          | `#F26A21` | Estado "En seguimiento", franja activa del sidebar |
| Rojo riesgo             | `#C62828` | Estado "Riesgo"                                    |
| Gris texto              | `#2B2B2B` | Texto principal                                    |
| Gris secundario         | `#6B7280` | Texto auxiliar y metadatos                         |
| Gris bordes             | `#D9DEE7` | Bordes y separadores                               |
| Fondo claro             | `#F5F7FA` | Fondo general del dashboard                        |

---

## KPIs implementados

El dashboard centraliza **26 indicadores** distribuidos en 8 categorías.

| Categoría                               | Indicadores |
| --------------------------------------- | ----------- |
| **A.** Diseño técnico y presupuestación | 3           |
| **B.** Atención online y chatbot IA     | 4           |
| **C.** Logística y distribución         | 3           |
| **D.** Reclamos y CRM                   | 6           |
| **E.** Ventas digitales y e-commerce    | 3           |
| **F.** RRHH y retención de talento      | 2           |
| **G.** Capacitación y calidad técnica   | 3           |
| **H.** Expansión nacional               | 2           |
| **Total**                               | **26**      |

Cada KPI incluye:

* Nombre.
* Categoría.
* Valor actual.
* Meta.
* Frecuencia de medición.
* Fuente de datos.
* Estado tipo semáforo.
* Mini gráfico de tendencia.

---

## Estructura del proyecto

```text
alutech-uxui-design/
├── index.html                  # Dashboard principal de indicadores
├── README.md                   # Documentación general del proyecto
└── alutech_choferes_app/        # App móvil para choferes
    ├── index.html              # Prototipo mobile responsive
    └── README.md               # Documentación específica de la app
```

El dashboard principal vive en `index.html`, organizado en tres bloques:

1. `<style>` — Variables CSS, componentes, layout y animaciones.
2. `<body>` — Sidebar, header y contenido renderizado por JS.
3. `<script>` — Datos (`KPIS`, `SUMMARY`, `BLOCKS`), utilidades SVG y funciones de render.

La app de choferes se encuentra dentro de la carpeta:

```text
alutech_choferes_app/
```

---

## Personalización

### Cambiar el usuario logueado

En `index.html`, dentro del `<header>`, buscar el bloque `.user`:

```html
<div class="user">
  <img class="avatar" src="URL_DE_LA_FOTO" alt="Nombre del usuario" style="object-fit:cover;border:none;background:none;" />
  <div class="user-meta">
    <div class="name">Nombre Apellido</div>
    <div class="role">Rol del usuario</div>
  </div>
</div>
```

---

### Agregar o editar KPIs

El array `KPIS`, ubicado en el `<script>`, define todos los indicadores.

Cada entrada incluye:

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

---

### Cambiar la paleta

Todas las variables de color están definidas en `:root` al inicio del `<style>`.

---

## Contexto del proyecto

Trabajo académico desarrollado en el marco de la carrera de **Ingeniería en Sistemas de Información** en la **UTN Facultad Regional Córdoba**, como parte de la solución IT de soporte al plan de mejora del proceso comercial de **AluTech S.A.**, empresa de aberturas con proyección de expansión nacional.

El dashboard principal se incluye como **anexo visual** de la propuesta de solución, mostrando cómo se materializaría el sistema de medición y control de los indicadores definidos en el trabajo.

La App Móvil para Choferes complementa la solución IT, representando cómo la empresa podría mejorar la trazabilidad de entregas, la comunicación con logística y la actualización en tiempo real del estado de los pedidos.

---

## Licencia

MIT License — Proyecto académico de uso libre con atribución.

---

## Autores

**Agustín Maretto** · **Pedro Torcivia**

Proyecto desarrollado en el marco de la carrera de Ingeniería en Sistemas de Información de la **Universidad Tecnológica Nacional (UTN) - Facultad Regional Córdoba**.
