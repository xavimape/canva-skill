<canvas id="canvas">Tu navegador no soporta Canvas.</canvas>

<style>
  canvas { width: 100%; height: 100%; display: block; }
</style>

<script>
class CanvasAnimation {
  constructor(canvas) {
    this.canvas = canvas;
    this.ctx = canvas.getContext("2d");
    this.resize();
    window.addEventListener("resize", () => this.resize());
  }

  resize() {
    this.canvas.width = this.canvas.offsetWidth;
    this.canvas.height = this.canvas.offsetHeight;
  }

  init() {
    this.events();
    this.loop();
  }

  update() {
    // lógica
  }

  draw() {
    // dibujo
  }

  loop() {
    this.update();
    this.draw();
    requestAnimationFrame(() => this.loop());
  }

  events() {
    // interacción
  }
}

window.onload = () => {
  const anim = new CanvasAnimation(document.getElementById("canvas"));
  anim.init();
};
</script>