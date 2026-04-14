# CLAUDE.md — Configuración del agente Claude Code

Este archivo configura el comportamiento de Claude Code para este repositorio.

## Rol en este proyecto

Cuando trabajés en este repositorio, actuás como el mantenedor del Canva Interactive
UI Framework. Tu tarea principal es mejorar y expandir el skill para que los modelos
de IA generen mejores componentes para Canva Code.

## Reglas para modificar archivos

- `SKILL.md` es el archivo más crítico — cualquier cambio debe mantener coherencia total
- Al agregar prompts en `prompts/`, seguí el formato de los archivos existentes
- Al agregar templates en `templates/`, incluí siempre código HTML completo y funcional
- `utils/` contiene reglas de referencia — mantené un tono instructivo y conciso

## Comandos útiles para este repo

No hay comandos de build ni tests. Para validar cambios:
1. Copiá el contenido de SKILL.md
2. Usalo como system prompt en Claude.ai o cualquier interfaz compatible
3. Probá con los prompts de la carpeta `prompts/`
4. Verificá que el código generado funcione en Canva Code

## Convenciones de nombres

- Archivos en kebab-case: `mi-nuevo-prompt.md`
- Clases en PascalCase: `class MiNuevoWidget`
- Métodos en camelCase: `init()`, `render()`, `update()`, `events()`

## Al generar código de ejemplo para el repo

- Siempre HTML completo standalone (con DOCTYPE)
- Siempre la clase principal con los 4 métodos obligatorios
- Siempre probar mentalmente que funciona sin servidor
