# Reglas de modos de operación

## Detección automática de modo

| Señal en el pedido del usuario | Modo a usar |
|-------------------------------|-------------|
| "explicame", "paso a paso", "con comentarios", "para aprender" | Docente |
| "limpio", "escalable", "sin comentarios", "producción" | Desarrollador |
| "rápido", "simple", "básico", "funcional", "prototipo" | Prototipo Rápido |
| Pedido largo y detallado | Desarrollador |
| Pedido corto y directo | Prototipo Rápido |
| Primera vez que usa el skill (inferido) | Docente |

## Comportamiento por modo

### Modo Docente
- Incluye comentarios explicativos en el código (cada bloque importante)
- Agrega sección "¿Qué hace este código?" después del bloque de código
- Explica brevemente cada método: init(), render(), update(), events()
- Sugiere ejercicios de personalización al final

### Modo Desarrollador
- Código directo sin comentarios (solo JSDoc si aplica)
- Estructura limpia y escalable
- Menciona mejoras posibles en una línea al final
- Sin explicaciones de conceptos básicos

### Modo Prototipo Rápido
- Código mínimo funcional (puede omitir update() si no aplica)
- Sin comentarios
- Sin variantes ni sugerencias adicionales
- Entregá en menos de 30 líneas si es posible
