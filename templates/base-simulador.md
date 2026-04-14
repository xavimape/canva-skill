# Template: Simulador

Template base para simuladores con inputs, validación y resultado dinámico.
Reemplazá los comentarios y campos con la lógica del simulador pedido.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simulador</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: sans-serif; display: flex; justify-content: center;
           align-items: center; min-height: 100vh; background: #f0f4f8; }
    .simulador { background: white; padding: 2rem; border-radius: 12px;
                 box-shadow: 0 4px 20px rgba(0,0,0,0.1); width: 100%; max-width: 420px; }
    .simulador h2 { margin-bottom: 1.5rem; color: #333; }
    .campo { margin-bottom: 1rem; }
    .campo label { display: block; font-size: 0.85rem; color: #666; margin-bottom: 0.3rem; }
    .campo input { width: 100%; padding: 0.6rem; border: 1px solid #ddd;
                   border-radius: 6px; font-size: 1rem; }
    .btn { width: 100%; padding: 0.8rem; background: #6c63ff; color: white;
           border: none; border-radius: 8px; font-size: 1rem; cursor: pointer; margin-top: 1rem; }
    .btn:hover { background: #5a52d5; }
    .resultado { margin-top: 1.5rem; padding: 1rem; background: #f0edff;
                 border-radius: 8px; text-align: center; font-size: 1.2rem;
                 display: none; color: #6c63ff; font-weight: bold; }
    .error { color: #e53e3e; font-size: 0.8rem; display: none; margin-top: 0.2rem; }
  </style>
</head>
<body>
  <div id="app"></div>
  <script>
    class SimuladorBase {
      constructor(root) {
        this.root = root;
        this.state = { resultado: null, error: null };
      }
      init() { this.render(); this.events(); }
      render() {
        this.root.innerHTML = `
          <div class="simulador">
            <h2>Título del Simulador</h2>
            <div class="campo">
              <label>Campo 1</label>
              <input type="number" id="campo1" placeholder="0">
              <span class="error" id="err1">Valor inválido</span>
            </div>
            <button class="btn" id="calcular">Calcular</button>
            <div class="resultado" id="resultado"></div>
          </div>`;
      }
      validate() {
        const val = parseFloat(document.getElementById('campo1').value);
        if (isNaN(val) || val <= 0) {
          document.getElementById('err1').style.display = 'block';
          return false;
        }
        document.getElementById('err1').style.display = 'none';
        return true;
      }
      calculate() { return 0; /* lógica de cálculo */ }
      update() {
        if (!this.validate()) return;
        const res = this.calculate();
        const el = document.getElementById('resultado');
        el.textContent = `Resultado: ${res}`;
        el.style.display = 'block';
      }
      events() {
        document.getElementById('calcular').addEventListener('click', () => this.update());
      }
    }
    window.addEventListener('DOMContentLoaded', () => {
      const sim = new SimuladorBase(document.getElementById('app'));
      sim.init();
    });
  </script>
</body>
</html>
```

## Notas de uso

- Renombrá `SimuladorBase` con el nombre del simulador en PascalCase
- Agregá tantos campos (`.campo`) como variables necesite el cálculo
- `validate()` debe retornar `false` y mostrar el error correspondiente si algún input es inválido
- `calculate()` contiene toda la lógica matemática; debe retornar el valor final
- Para resultados complejos (tabla, gráfico), expandí `update()` para renderizar HTML adicional
