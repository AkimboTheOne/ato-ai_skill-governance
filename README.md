# ATO Skill Governance

Repositorio base para la gobernanza de skills de IA, las restricciones de planificación, las políticas de runtime y los principios de gobernanza cognitiva.

---

## Propósito

Este repositorio define una base de gobernanza, centrada en la documentación, para diseñar, crear, revisar y evolucionar skills de IA.

Ayuda a agentes y operadores humanos a:

- definir los límites de las skills;
- preservar la claridad arquitectónica;
- evitar complejidad innecesaria;
- establecer heurísticas de planificación;
- limitar el comportamiento en runtime;
- evaluar si la automatización está preparada;
- y evolucionar las skills sin desviaciones de gobernanza.

---

## Qué es este repositorio

Este repositorio es:

- una base de gobernanza de skills;
- una guía cognitiva para agentes;
- una fuente de restricciones de planificación y runtime;
- un repositorio de artefactos reutilizables de ingeniería de skills;
- y un modelo operativo, centrado en documentación, para la evolución de skills.

---

## Qué no es este repositorio

Actualmente, este repositorio no es:

- un CLI;
- un motor de runtime;
- un framework de orquestación;
- un paquete de Python;
- un generador de código;
- un sistema multiagente;
- ni una plataforma de ejecución autónoma.

Solo se debería incorporar código si el modelo operativo basado en documentación demuestra suficiente estabilidad para justificar su automatización.

---

## Doctrina central

> No automatices, distribuyas, abstraigas, optimices ni orquestes algo que antes no se haya cuestionado, eliminado, simplificado y comprendido.

La complejidad no es valor.

La complejidad es un costo operativo mientras no se justifique de forma continua.

---

## Orden de ingeniería

Todo diseño, planificación, revisión y evolución debería seguir este orden:

1. Preguntar (Question)
2. Eliminar (Eliminate)
3. Simplificar (Simplify)
4. Acelerar (Accelerate)
5. Automatizar (Automate)

No optimices antes de simplificar.

No automatices antes de alcanzar estabilidad.

---

## Influencias intelectuales

Este repositorio se inspira en varias tradiciones de ingeniería y operaciones:

- [Algoritmo de ingeniería de cinco pasos de Elon Musk](https://insideevs.com/news/526954/elon-musk-5-steps-success/): cuestionar requisitos, eliminar, simplificar, acelerar y automatizar.
- [Sistema de Producción Toyota](https://global.toyota/en/company/vision-and-philosophy/production-system/index.html): reducción de desperdicio, flujo, jidoka, just-in-time y kaizen.
- [Lean Thinking](https://www.lean.org/lexicon-terms/lean-thinking-and-practice/): valor, cadena de valor, flujo, pull y mejora continua.
- [Teoría de las Restricciones](https://www.tocinstitute.org/five-focusing-steps.html): enfocar la mejora en la restricción del sistema antes de optimizar localmente.
- [Pensamiento sistémico](https://donellameadows.org/archives/leverage-points-places-to-intervene-in-a-system/): preservar la visibilidad de los ciclos de retroalimentación, los puntos de intervención y las consecuencias no previstas.

Estas influencias no se consideran una doctrina rígida. Orientan la postura de gobernanza del repositorio: cuestionar primero, eliminar la complejidad innecesaria, simplificar lo que quede, acelerar solo sistemas estables y automatizar al final.

---

## Estructura del repositorio

Estructura canónica:

```text
ato-skill-governance/
├── README.md
├── SKILL.md
├── FOUNDATION.md
├── AGENTS.md
├── skill-charter.md
│
├── governance/
│   ├── planner-rules.yaml
│   ├── runtime-policy.yaml
│   └── activation-policy.yaml
│
├── reviews/
│   └── checklist.md
│
├── skills/
│   └── templates/
│       └── skill-charter.template.md
│
├── memory/
│   ├── README.md
│   └── learnings/
│       └── doctrine-projection.md
│
└── references/
    └── README.md
```

La estructura debe seguir siendo pequeña hasta que nuevos artefactos justifiquen su existencia.

Se evitan deliberadamente duplicados en la raíz como `planner-rules.yaml`, `runtime-policy.yaml` o `checklist.md`. Las rutas canónicas son los subdirectorios gobernados que se muestran arriba.

---

## Familias de artefactos

| Artefacto | Propósito |
|---|---|
| [SKILL.md](SKILL.md) | Define la identidad operativa, el contrato de activación y los límites de esta skill. |
| [FOUNDATION.md](FOUNDATION.md) | Define la doctrina de ingeniería reutilizable. |
| [AGENTS.md](AGENTS.md) | Define las restricciones operativas para agentes. |
| [skill-charter.md](skill-charter.md) | Define el charter concreto de la skill de este repositorio. |
| [governance/planner-rules.yaml](governance/planner-rules.yaml) | Define heurísticas de planificación y gobernanza de complejidad. |
| [governance/runtime-policy.yaml](governance/runtime-policy.yaml) | Define los límites de ejecución en runtime. |
| [governance/activation-policy.yaml](governance/activation-policy.yaml) | Define cuándo y cómo se activa la gobernanza. |
| [reviews/checklist.md](reviews/checklist.md) | Define criterios de revisión antes de implementar o automatizar. |
| [skills/templates/skill-charter.template.md](skills/templates/skill-charter.template.md) | Define el charter estándar para futuras skills. |
| [memory/README.md](memory/README.md) | Define límites y precedencia de memoria, y el manejo de propuestas de promoción doctrinal. |
| [references/README.md](references/README.md) | Define cómo agregar referencias estables sin crear contexto descontrolado. |

---

## Relaciones entre artefactos

`FOUNDATION.md` define la doctrina compartida. `SKILL.md`, `governance/*.yaml`, `reviews/checklist.md` y `memory/README.md` son proyecciones contextuales de esa doctrina. No deben introducir doctrinas en competencia.

`SKILL.md` es el punto de entrada operativo para Codex. Define cómo se usa la skill, cuándo se activa y qué límites preserva. Debe ser conciso y delegar los detalles a los artefactos canónicos.

`AGENTS.md` define la referencia operativa local del repositorio. Gobierna el mantenimiento y las restricciones de uso específicas del proyecto, sin ser un requisito para interpretar `SKILL.md`.

`SKILL.md` y `AGENTS.md` comparten la misma base, pero cumplen funciones distintas. `SKILL.md` permanece autocontenido como interfaz de la skill; `AGENTS.md` sigue siendo la referencia local autoritativa del proyecto.

`skill-charter.md` define el charter concreto de la skill de este repositorio.

Los archivos de `governance/` definen las políticas de planificación, runtime y activación derivadas de la doctrina compartida.

Los directorios `reviews/`, `skills/templates/`, `memory/` y `references/` respaldan la revisión, la creación futura de skills, los límites de memoria, la precedencia, la promoción doctrinal y las referencias gobernadas.

---

## Política de evolución

Este repositorio debería evolucionar en el siguiente orden:

1. estabilizar la doctrina;
2. estabilizar la identidad de la skill;
3. definir las restricciones para agentes;
4. definir las reglas de planificación;
5. definir la política de runtime;
6. definir la semántica de activación;
7. definir el proceso de revisión;
8. y después evaluar si la automatización está justificada.

El código prematuro es deuda arquitectónica.

---

## Principio final

> Una skill debe reducir la complejidad operativa más rápido de lo que crea complejidad arquitectónica.
