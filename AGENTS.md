# Reglas y Órdenes Mandatarias del Agente: Pokémon Chirl Mythos Bot

Directrices perpetuas y obligatorias para el desarrollo del bot autónomo de testing y navegación para Pokémon Chirl Mythos.

---

## 1. Saludo Obligatorio
* **SIEMPRE**, sin ninguna excepción, toda respuesta del agente debe comenzar con `Carlos, ` (ejemplo: `Carlos, he actualizado...` o `Carlos, a continuación te muestro...`).

---

## 2. Protocolo de Flujo de Trabajo y Comandos

### A. Comando "siguiente paso"
Cuando Carlos escriba `"siguiente paso"`:
1. **NO ejecutar ninguna acción de código ni modificar archivos.**
2. Mostrar la tabla completa y actualizada del `PLAN_DE_ACCION.md`.
3. Indicar el cambio de versión (ejemplo: transición de versión `0.1.0` a `0.2.0`).
4. Describir detalladamente justo debajo de la tabla el paso exacto que se va a realizar (objetivo, módulos/scripts involucrados y resultado esperado).
5. Preguntar explícitamente a Carlos si desea proceder.
6. Detener la ejecución a la espera de la confirmación expresa de Carlos.

### B. Comando "paso finalizado"
Cuando Carlos escriba `"paso finalizado"`:
1. Dar por terminado el punto actual, cambiando su estado a `implementado` en `PLAN_DE_ACCION.md`.
2. Registrar cualquier solución técnica comprobada o técnica validada en `LECCIONES_APRENDIDAS.md`.
3. Actualizar la versión en `version.json`.
4. Mostrar a Carlos la tabla del plan de acción actualizada con el nuevo estado.

---

## 3. Instrucciones de Verificación, Pruebas y Visualización en Vivo
* **Guía de Pruebas Obligatoria:**
  - En cada funcionalidad o módulo comprobable del bot, detallar a Carlos la guía paso a paso (comandos de lanzamiento, emulador mGBA, scripts Lua/Python y resultado exacto observable).
* **Visualización en Pantalla:**
  - Mostrar por pantalla todo elemento visual disponible tan pronto como exista: mapas renderizados, matrices de colisión/transitabilidad y rutas trazadas por el algoritmo.
  - Cuando el bot interactúe con el juego, abrir la ventana del emulador mGBA en directo con su script para que Carlos pueda observar la ejecución en tiempo real en su monitor.

---

## 4. Principios Mandatarios de Navegación y Control del Bot
* **Comportamiento Tipo GPS (Autónomo e Inteligente):**
  - El bot debe comportarse exactamente como un GPS: saber siempre en qué mapa/banco y coordenadas exactas ($X, Y$) está ubicado en tiempo real en la RAM de mGBA y calcular de forma dinámica las rutas hacia el destino.
  - **Queda terminantemente prohibido** parametrizar o 'hardcodear' secuencias fijas de pulsaciones de botones o sticks para desplazarse. Todo movimiento debe ser calculado dinámicamente sobre la matriz de transitabilidad del juego.
* **Conmutación Inmediata a Modo Manual (Botón de Desactivación en Caliente):**
  - Debe existir siempre una tecla/botón asignado que permita desactivar el bot al instante para devolver el control manual total a Carlos, y reactivarlo cuando se desee sin reiniciar el proceso.
* **Resolución Autónoma de Diálogos y Menús Complejos:**
  - El bot debe ser capaz de procesar y resolver de forma autónoma el avance de texto, elecciones de Sí/No, menús multiopción y pantallas de introducción de texto, garantizando una navegación 100% fluida sin atascos.

---

## 5. Estructura de la Tabla del Plan (`PLAN_DE_ACCION.md`)
La tabla debe mantener estrictamente las 4 columnas:
`| número de punto | punto | breve descripción | estado (implementado, en curso, pendiente) |`
* Estados válidos: `implementado`, `en curso`, `pendiente`.

---

## 6. Registro Perpetuo de Lecciones Aprendidas (`LECCIONES_APRENDIDAS.md`)
* Si durante la investigación o pruebas se descartan vías o se prueba más de una alternativa, se registra de inmediato en `LECCIONES_APRENDIDAS.md`.
* En cualquier tarea posterior similar, el agente debe acudir directamente a la vía comprobada sin repetir intentos fallidos previos.
