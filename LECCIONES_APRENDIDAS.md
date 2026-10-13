# Base de Conocimiento y Lecciones Aprendidas: Pokémon Chirl Mythos Bot

Este documento registra los hallazgos técnicos, arquitecturas validadas, direcciones RAM comprobadas y patrones de scripting para el bot de mGBA.

> **Principio Fundamental:**
> Si para una tarea se intentan múltiples soluciones, la que resulte exitosa se registra aquí. Ante tareas similares posteriores, se acude directamente a la solución probada.

---

## 1. Arquitectura de Scripting en mGBA
* **Compatibilidad de Plataforma:**
  - mGBA dispone de una API nativa de Lua muy ligera y directa para acceder a memoria RAM (`emu:read8`, `emu:read16`, `emu:read32`).
  - La RAM de GBA tiene direcciones estándar (`0x02000000` para EWRAM y `0x03000000` para IWRAM).
* **Botón de Desactivación en Caliente:**
  - La conmutación manual debe implementarse directamente interceptando teclas del teclado antes de inyectar inputs al emulador.
