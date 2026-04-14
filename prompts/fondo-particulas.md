# Prompt: Fondo de Partículas Animado

## Prompt de usuario

```
Fondo de partículas animado para Canva Code.
```

## Modo detectado
Prototipo Rápido (pedido directo y conciso)

## Clase generada
`ParticleBackground`

## Métodos implementados
- `init()` → verifica soporte canvas, llama resize/spawn/events/render
- `resize()` → ajusta canvas.width/height a window
- `spawn()` → genera array de partículas con color/posición/velocidad aleatorios
- `createParticle()` → factory de partículas
- `update()` → mueve partículas, rebote en bordes, repulsión con mouse
- `drawConnections()` → líneas entre partículas cercanas con opacidad dinámica
- `render()` → loop con requestAnimationFrame + fondo degradado radial
- `events()` → resize, mousemove, mouseleave

## Features validados en test real

- ✅ Interacción mouse (repulsión radio 120px)
- ✅ Líneas de conexión entre partículas (<120px)
- ✅ Fallback accesible (aria-label + role="img" + div#fallback)
- ✅ Colores: cian, violeta, magenta, blanco, verde menta
- ✅ Fondo degradado radial animado
- ✅ 120 partículas por defecto

## Resultado de referencia validado

Componente probado en Claude Sonnet 4.6 (Abril 2026). El skill detectó
correctamente el modo Prototipo Rápido, generó `ParticleBackground` con
los 8 métodos, pasó la validación interna y entregó código funcional en
Canva Code sin modificaciones.
