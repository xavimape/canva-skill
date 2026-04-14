Estructura base para componentes HTML + CSS + JS:

<div id="app"></div>

<style>
  /* Estilos responsivos */
</style>

<script>
class Component {
  constructor(root) {
    this.root = root;
  }

  init() {
    this.render();
    this.events();
  }

  render() {
    this.root.innerHTML = `
      <!-- UI -->
    `;
  }

  update() {
    // lógica reactiva
  }

  events() {
    // listeners
  }
}

window.onload = () => {
  const app = new Component(document.getElementById("app"));
  app.init();
};
</script>