# Plan de Acción: Pokémon Chirl Mythos Bot (mGBA Suite)

| número de punto | punto | breve descripción | estado (implementado, en curso, pendiente) |
| :---: | :--- | :--- | :---: |
| **1.0** | Entorno mGBA Scripting y Puente de Control | Configuración del entorno de scripting en mGBA (Lua / IPC Socket Python) con hook de teclado para botón de pánico (desactivación en caliente). | pendiente |
| **2.0** | Mapeo de Direcciones RAM GBA | Lectura en tiempo real de coordenadas ($X, Y$), ID de Banco/Mapa, estado de juego (overworld, diálogo, combate) y equipo en RAM. | pendiente |
| **3.0** | Parser de Mapas y Transitabilidad GBA | Extracción y lectura de las matrices de colisiones y elevación de los mapas de Johto/Kanto desde los layouts del juego. | pendiente |
| **4.0** | Motor de Pathfinding A* (Navegación GPS) | Cálculo dinámico de rutas baldosa a baldosa evitando obstáculos sin secuencias de botones hardcodeadas. | pendiente |
| **5.0** | Controlador de Diálogos y Menús | Avance autónomo de diálogos, resolución de preguntas Sí/No y manejo de menús para evitar bloqueos del jugador. | pendiente |
| **6.0** | Conmutador y Alerta de Combates | Detección inmediata de inicio de combates, pausa del movimiento y aviso en pantalla para cambio a control manual o motor de batalla. | pendiente |
| **7.0** | Suite de Pruebas Automatizadas de Regresión | Scripts automáticos de testeo de eventos (testear inicio de partida, testear evolución con Marcha Espectral, testear tiendas). | pendiente |
