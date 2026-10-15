# 📑 Changelog - Bitácora de Versionado SemVer (Actividad 7)

Todos los cambios notables realizados en este software se registrarán de manera rigurosa en este archivo bajo las especificaciones del estándar de buenas prácticas de control de versiones.

**Proyecto:** Mini Juego "Piedra, Papel o Tijera" con Persistencia de Datos (struct + fstream)  
**Institución:** E.E.S.T. N° 1 "Eduardo Ader" — Vicente López  
**Asignatura:** Laboratorio de Programación (LPR) — 5° Año  
**Curso:** 5° Año 5° 3° (Grupos A-B)  
**Profesor:** Mansilla Muñoz York Elías  
**Desarrolladores:** Gabriel Zacarías, Sofía Mojica, Leonel De Armas, Mateo Roberts (Grupo N.º 3)  

---

## - 2026-10-15
### Aprobado
- **Baseline Aprobado:** Estructura de persistencia física de datos unificada para el resguardo de partidas en el almacenamiento secundario.

### Añadido
- **Modelado con Struct:** Encapsulación de variables heterogéneas mediante la estructura `Partida` (`int idPartida`, `string jugador`, `string eleccionJugador`, `string eleccionIA`, `string resultado`).
- **Persistencia de Escritura (ofstream):** Implementación de la subrutina `void guardarEnDisco(const Partida& p)` configurada en modo Append (`ios::app`) para registrar de forma no volátil cada jugada sin sobrescribir las partidas previas en formato CSV.
- **Persistencia de Lectura (ifstream):** Implementación de la subrutina `void leerHistorialDisco()` encargada de recuperar de forma secuencial y delimitada por comas el historial completo almacenado en el disco para desplegarlo en la consola.
- **Inteligencia Artificial de Consola:** Integración de la biblioteca `<ctime>` y la función `srand(time(0))` para aleatorizar la selección de la IA (Piedra, Papel o Tijera) en cada iteración del menú.
- **Normalización de Historiales:** Inclusión del archivo `.gitattributes` para forzar finales de línea estilo Linux (`LF`) en los archivos fuente (`.cpp`, `.md`) y en el archivo de persistencia física generado (`.txt`).

### Solucionado
- **Control del Buffer de Hardware:** Inclusión de la directiva `cin.ignore()` antes de invocar la instrucción de lectura de caracteres `getline(cin, p.jugador)`, solucionando el desbordamiento del salto de línea (`\n`) que salteaba la pregunta del nombre en la terminal.
- **Conflictos de Compilación Local:** Corrección de fallas por bloqueo de procesos en la memoria RAM (*Permission denied*) parametrizando el nombre único de compilación (`-o src/piedrapapelotijera.exe`) bajo el estándar global de compatibilidad `C++11`.

---

## - 2026-10-01
### Añadido
- **Esqueleto del Repositorio:** Arquitectura y carpetas iniciales del proyecto (`src/`, `docs/`, `capturas/`) preparadas para el control de versiones ramificado.
