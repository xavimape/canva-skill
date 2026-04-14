# Canva Interactive UI Framework
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

## Ejemplos de uso

### 1. Contador interactivo

Generá un contador interactivo para Canva.


Resultado esperado:
- HTML + CSS + JS
- Clase `CounterWidget`
- Botones + estado dinámico
- Animación simple

---

### 2. Fondo de partículas animado

Fondo de partículas animado para Canva Code.


Resultado esperado:
- Canvas
- requestAnimationFrame
- Interacción con mouse
- Clase `ParticleBackground`

---

### 3. Calculadora de interés simple

Calculadora de interés simple.


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

Este framework puede usarse libremente para proyectos educativos, prototipado, investigación y desarrollo frontend.

---

## Autor

Framework diseñado para potenciar la creación de UI interactiva embebible en Canva, con enfoque en:

- Educación  
- Prototipado rápido  
- Desarrollo frontend  
- Visualizaciones dinámicas  