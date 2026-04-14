# Canva Interactive UI Framework

![GitHub last commit](https://img.shields.io/github/last-commit/xavimape/canva-skill)
![License](https://img.shields.io/badge/license-MIT-green)
![Canva](https://img.shields.io/badge/Canva-Compatible-blueviolet)
![No dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)

Framework profesional para generar componentes interactivos embebibles en **Canva**, LMS y entornos web usando **HTML, CSS, JavaScript y Canvas API**, sin dependencias externas.

Este repositorio contiene:
- El skill principal (`SKILL.md`)
- Prompts especializados
- Plantillas reutilizables
- Utilidades de validación
- Logo y banner oficiales
- Estructura modular estilo SDK

El objetivo es permitir que un modelo genere **widgets, animaciones, simuladores y micro‑apps** listas para producción.

---

## Tabla de contenidos

- [Características principales](#características-principales)
- [Estructura del proyecto](#estructura-del-proyecto)
- [¿Cómo funciona?](#cómo-funciona)
- [Cómo usar este skill](#-cómo-usar-este-skill)
- [Integración con Claude](#-integración-con-claude)
- [Ejemplos de uso](#ejemplos-de-uso)
- [Plantillas incluidas](#plantillas-incluidas)
- [Validación automática](#validación-automática)
- [Extensiones futuras](#extensiones-futuras)
- [Licencia](#licencia)
- [Autor](#autor)

---

## Características principales

- **Código autocontenido** (HTML + CSS + JS)
- **Modos automáticos**: Docente, Desarrollador, Prototipo Rápido
- **Canvas API** para animaciones avanzadas
- **Encapsulación obligatoria** (clases o módulos)
- **Compatibilidad total con Canva Code**
- **Responsive + accesible**
- **Validación interna antes de generar código**
- **Sin dependencias externas**

---

## Estructura del proyecto

```text
/canva-skill/
│
├── README.md
├── SKILL.md
│
├── prompts/
│   ├── contador.md
│   ├── fondo-particulas.md
│   ├── calculadora.md
│   ├── barra-progreso.md
│   └── widget-generico.md
│
├── templates/
│   ├── base-html-css-js.md
│   ├── base-canvas.md
│   ├── base-widget.md
│   └── base-simulador.md
│
├── utils/
│   ├── checklist-validacion.md
│   ├── reglas-modos.md
│   └── prompts-maestros.md
│
└── assets/
    ├── logo.svg
    └── banner.svg
```

---

## ¿Cómo funciona?

El framework guía al modelo para:

1. Interpretar el requerimiento del usuario  
2. Seleccionar automáticamente la tecnología adecuada  
3. Elegir el modo correcto (Docente / Dev / Prototipo)  
4. Generar código limpio, encapsulado y autocontenido  
5. Validarlo antes de entregarlo  
6. Optimizarlo para Canva y embeds web  

---

## Cómo usar este skill

1. Abrí tu herramienta de IA compatible con skills/prompts personalizados
2. Cargá el contenido de `SKILL.md` como prompt de sistema o instrucción personalizada
3. Usá los prompts de la carpeta `prompts/` como puntos de partida
4. El modelo generará código listo para pegar en **Canva Code**

> **Tip:** Para mejores resultados, especificá el modo deseado: *Docente*, *Desarrollador* o *Prototipo Rápido*.

---

## Integración con Claude

### Opción A — Claude.ai Projects (recomendado)
1. Creá un Project en Claude.ai
2. En "Project Instructions", pegá el contenido completo de `SKILL.md`
3. Subí como archivos del proyecto los `.md` de `templates/` y `utils/`
4. Desde ese project, usá directamente los prompts de la carpeta `prompts/`

### Opción B — Claude Code en VS Code
1. Cloná este repositorio en tu proyecto
2. El archivo `CLAUDE.md` se carga automáticamente como contexto
3. Podés referenciar templates con: "usá la template base-canvas.md"

### Opción C — Cualquier interfaz compatible con system prompts
1. Copiá el contenido de `SKILL.md` como instrucción de sistema
2. Iniciá la conversación con el prompt de ejemplo del componente que necesitás

### Tips para mejores resultados con Claude
- Especificá el modo al inicio: `[MODO: Docente]` o `[MODO: Dev]`
- Si el resultado no está bien encapsulado, agregá: "recordá usar la estructura init/render/update/events"
- Para proyectos complejos, pedí primero el esqueleto y luego los métodos por separado

---

## Ejemplos de uso

### 1. Contador interactivo

> **Prompt de ejemplo:**
> ```
> Generá un contador interactivo para Canva.
> ```

Resultado esperado:
- HTML + CSS + JS
- Clase `CounterWidget`
- Botones + estado dinámico
- Animación simple

---

### 2. Fondo de partículas animado

> **Prompt de ejemplo:**
> ```
> Fondo de partículas animado para Canva Code.
> ```

Resultado esperado:
- Canvas
- requestAnimationFrame
- Interacción con mouse
- Clase `ParticleBackground`

---

### 3. Calculadora de interés simple

> **Prompt de ejemplo:**
> ```
> Calculadora de interés simple.
> ```

Resultado esperado:
- Inputs
- Validación
- Resultado en vivo
- Clase `SimpleCalculator`

---

## Plantillas incluidas

El repositorio incluye plantillas base para:

- Widgets interactivos  
- Animaciones Canvas  
- Simuladores  
- Componentes HTML/CSS/JS  

Estas plantillas garantizan consistencia y calidad en cada generación.

---

## Validación automática

Antes de entregar código, el modelo verifica:

- [ ] ¿Es autocontenido?  
- [ ] ¿Sin dependencias externas?  
- [ ] ¿Sin variables globales?  
- [ ] ¿Encapsulado en clase?  
- [ ] ¿Incluye init/render/update/events?  
- [ ] ¿Es responsive?  
- [ ] ¿Canvas tiene fallback?  
- [ ] ¿Compatible con Canva embed?  
- [ ] ¿Cumple el modo (Docente/Dev/Prototipo)?  

---

## Extensiones futuras

- Micro‑apps educativas exportables  
- Dashboards interactivos  
- Gráficos tipo charts  
- Simuladores avanzados  
- Integración con datos simulados  

---

## Licencia

Este proyecto está bajo la licencia **MIT**. Podés usarlo libremente para proyectos educativos, prototipado, investigación y desarrollo frontend.

Ver archivo [LICENSE](LICENSE) para más detalles.

---

## Autor

**xavimape** — [@xavimape](https://github.com/xavimape)

Framework diseñado para potenciar la creación de UI interactiva embebible en Canva, con enfoque en:

- Educación
- Prototipado rápido
- Desarrollo frontend
- Visualizaciones dinámicas
