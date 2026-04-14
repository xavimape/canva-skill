# Template: Widget HTML/CSS/JS

Template base para widgets interactivos autocontenidos. Completá los comentarios
con la lógica específica del componente pedido.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Widget</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { display: flex; justify-content: center; align-items: center;
           min-height: 100vh; font-family: sans-serif; background: #f5f5f5; }
    #app { width: 100%; max-width: 480px; padding: 1.5rem; }
    /* Estilos del componente aquí */
  </style>
</head>
<body>
  <div id="app"></div>
  <script>
    class NombreWidget {
      constructor(root) {
        this.root = root;
        this.state = {}; // estado inicial
      }
      init() { this.render(); this.events(); }
      render() { this.root.innerHTML = `<!-- HTML del componente -->`; }
      update() { /* lógica reactiva */ }
      events() { /* event listeners */ }
    }
    window.addEventListener('DOMContentLoaded', () => {
      const widget = new NombreWidget(document.getElementById('app'));
      widget.init();
    });
  </script>
</body>
</html>
```

## Notas de uso

- Renombrá `NombreWidget` con el nombre del componente en PascalCase
- `this.state` debe contener solo datos primitivos o arrays planos
- `render()` reconstruye el DOM desde el estado; no manipulés el DOM directamente fuera de render
- `events()` se llama una sola vez en `init()`; usá delegación de eventos en el root
- El max-width de `#app` es 480px por defecto; ajustá según el diseño en Canva
