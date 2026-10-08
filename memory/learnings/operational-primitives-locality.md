# Ubicación de las primitivas operativas

## Aprendizaje

Las primitivas operativas que definen el comportamiento mecánico de una skill deben permanecer dentro de su `SKILL.md`, salvo que exista un caso concreto de reutilización externa o un límite de mantenimiento independiente que justifique extraerlas.

Así, la doctrina y el comportamiento se mantienen alineados, se evita una segunda capa de autoridad y se reduce la desviación entre las reglas declaradas y el modelo real de ejecución.

## Evidencia

Este aprendizaje surgió al definir `ato-skill-governance`. Un artefacto separado para las 10 acciones operativas no era necesario una vez que estas se expresaron como doctrina interna con una forma de ejecución fija.

## Notas de gobernanza

- Compatible con el orden requerido: Preguntar (Question), Eliminar (Eliminate), Simplificar (Simplify), Acelerar (Accelerate) y Automatizar (Automate).
- Reduce duplicación sin añadir comportamiento en runtime, estado oculto ni orquestación.
- Solo aplica cuando el objetivo es un comportamiento operativo reutilizable, no un catálogo de documentación.
