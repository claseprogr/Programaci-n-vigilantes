# Programación de Vigilantes

App web para resolver ejercicios de programación de turnos y rotación de personal, típicos de cursos de Investigación de Operaciones o Métodos Cuantitativos.

Un solo archivo HTML, sin dependencias, sin build, sin servidor.

## Qué hace

Calcula cuántos vigilantes se necesitan para cubrir una instalación con turnos rotativos, y genera la tabla de asignación.

Fórmula: **N = P × (T + D) / T**
- P: puestos totales por día
- T: días de trabajo consecutivos
- D: días de descanso consecutivos

## Presets incluidos

**Planta industrial.** 2 turnos de 12h, 1 portero + 2 ronderos por turno. Trabajan 3 días, descansan 2. Resultado: 10 vigilantes. Reproduce exactamente el tablero del profesor.

**Conjunto cerrado.** 2 turnos de 12h, 1 portero + 1 rondero por turno. Esquema 3x2. Resultado: 7 vigilantes.

**Fábrica.** 4 puestos (Torno, Fresa, Corte, Soldadura) × 3 turnos de 8h. Trabajan 4 días, descansan 2. Resultado: 18 vigilantes (A-R). Reproduce exactamente la solución del profesor de la imagen.

## Modo colocar letra (la clave para replicar al profesor)

Cada profesor tiene su propio criterio para asignar las letras iniciales. La app trae un patrón estándar, pero si el profesor pone las letras en posiciones distintas, no hay problema:

1. Pulsa el botón rojo "Modo colocar letra".
2. Haz clic en cualquier celda de la tabla.
3. Escribe la letra que el profesor pone ahí.
4. La app recalcula toda la fila desde ese punto, manteniendo la rotación.

Así puedes reproducir exactamente la solución del profesor sin tener que pensar en offsets ni cálculos manuales. También puedes editar las letras iniciales directamente en el campo rojo del panel izquierdo si prefieres.

## Qué se puede modificar

- Días de trabajo y descanso (3x2, 4x2, 5x2, etc)
- Horas de inicio y fin de cada turno
- Cuántos turnos al día y sus nombres
- Cuántos puestos por turno (porteros, ronderos, torno, fresa, etc)
- Cantidad de días a mostrar
- Día de inicio
- Letra inicial de cada puesto

## Exportar

- Imprimir o guardar como PDF
- Copiar la tabla como texto tabulado
- Descargar CSV

## Cómo subirla a GitHub

1. Crear repo nuevo en GitHub
2. Subir `index.html` y `README.md`
3. En Settings → Pages activar GitHub Pages con la rama main, carpeta root
4. Queda disponible en `https://tu-usuario.github.io/nombre-repo/`

## Limitaciones

- Si N no es entero, la app avisa y redondea hacia arriba.
- Soporta hasta 702 vigilantes (A a ZZ).
- No guarda datos entre sesiones.

## Licencia

MIT.
