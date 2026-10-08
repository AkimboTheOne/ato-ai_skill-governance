# Lista de revisión de ingeniería

## Orden central de revisión

Evalúa siempre en este orden:

1. Preguntar (Question)
2. Eliminar (Eliminate)
3. Simplificar (Simplify)
4. Acelerar (Accelerate)
5. Automatizar (Automate)

No omitas pasos.

No optimices antes de simplificar.

No automatices antes de alcanzar estabilidad.

---

## 1. Validación del requisito

### Propósito

Valida si el requisito debería existir.

### Lista de comprobación

- [ ] ¿El requisito resuelve un problema real?
- [ ] ¿Sigue siendo pertinente?
- [ ] ¿Tiene una persona responsable claramente identificada?
- [ ] ¿Se puede medir su valor operativo?
- [ ] ¿Alguien puede explicar por qué existe?
- [ ] ¿Se heredó sin validación?
- [ ] ¿La arquitectura responde a una necesidad real y no a una moda?
- [ ] ¿Introduce complejidad por apariencia en vez de aportar valor?

### Rechazar si

- nadie puede justificar el requisito;
- existe solo porque siempre se ha hecho así;
- existe solo para imitar otra arquitectura;
- genera carga operativa sin un beneficio medible.

---

## 2. Revisión de eliminación

### Propósito

Elimina la complejidad innecesaria antes de mejorar cualquier cosa.

### Lista de comprobación

- [ ] ¿Se puede eliminar por completo?
- [ ] ¿Se puede integrar en una capacidad existente?
- [ ] ¿Se pueden reducir las dependencias?
- [ ] ¿Se puede reducir la orquestación?
- [ ] ¿Se puede reducir la carga de contexto?
- [ ] ¿Se pueden reducir las partes móviles?
- [ ] ¿Se puede reducir la carga cognitiva?
- [ ] ¿Duplica un sistema o flujo de trabajo existente?

### Rechazar si

- la solución añade capas sin reducir el costo operativo;
- aumenta la proliferación de dependencias;
- crea orquestación sin necesidad;
- conserva complejidad obsoleta.

---

## 3. Revisión de simplificación

### Propósito

Prioriza sistemas explícitos, comprensibles y fáciles de mantener.

### Lista de comprobación

- [ ] ¿El comportamiento es explícito?
- [ ] ¿Las personas pueden comprender fácilmente el flujo de trabajo?
- [ ] ¿Pueden auditar el sistema?
- [ ] ¿Se entiende el modelo de estado?
- [ ] ¿Se entiende la arquitectura sin diagramas?
- [ ] ¿El sistema es determinista cuando resulta posible?
- [ ] ¿La solución es más sencilla que el problema que resuelve?
- [ ] ¿Las abstracciones están justificadas desde el punto de vista operativo?

### Preferir

- monolitos modulares;
- razonamiento local;
- Markdown y texto sin formato;
- contratos explícitos;
- flujos deterministas;
- memoria legible por personas.

### Rechazar si

- la arquitectura es más difícil de entender que el problema;
- el sistema depende de comportamiento oculto;
- la abstracción oculta la realidad operativa;
- la capa de orquestación se convierte en la principal fuente de complejidad.

---

## 4. Revisión de aceleración

### Propósito

Optimiza solo sistemas estables y validados.

### Lista de comprobación

- [ ] ¿El flujo de trabajo ya es estable?
- [ ] ¿Se conocen los modos de fallo?
- [ ] ¿La responsabilidad está clara?
- [ ] ¿El proceso es coherente en la operación?
- [ ] ¿La optimización se dirige a un cuello de botella real?
- [ ] ¿Reduce la fricción operativa?
- [ ] ¿Reduce la latencia del ciclo de retroalimentación?
- [ ] ¿Mejora el rendimiento sin aumentar el caos?

### Rechazar si

- la optimización se dirige a una solución temporal;
- la aceleración oculta inestabilidad;
- se escala antes de simplificar;
- la velocidad de despliegue supera la comprensión operativa.

---

## 5. Revisión de automatización

### Propósito

Automatiza solo sistemas que ya son válidos operativamente.

### Lista de comprobación

- [ ] ¿El proceso es estable?
- [ ] ¿Las entradas están bien definidas?
- [ ] ¿Se pueden verificar las salidas?
- [ ] ¿Es posible revertir los cambios?
- [ ] ¿Se preserva la auditabilidad?
- [ ] ¿Hay capacidad de anulación humana?
- [ ] ¿La automatización tiene límites claros?
- [ ] ¿Se controlan los efectos secundarios?
- [ ] ¿La automatización preserva la claridad operativa?

### Rechazar si

- la automatización oculta un diseño de proceso defectuoso;
- el flujo de trabajo es ambiguo;
- es imposible revertir los cambios;
- la responsabilidad no está clara;
- la automatización amplifica la confusión operativa;
- la IA compensa la falta de disciplina de ingeniería.

---

## Revisión específica de IA

### Gestión del contexto

- [ ] ¿La carga de contexto es mínima y pertinente?
- [ ] ¿Se evita la memoria innecesaria?
- [ ] ¿El contexto es trazable y auditable?
- [ ] ¿Se minimiza la superficie de alucinación?

### Revisión de herramientas

- [ ] ¿El uso de herramientas es mínimo y está justificado?
- [ ] ¿Es necesario encadenar herramientas?
- [ ] ¿Los efectos secundarios de las herramientas son explícitos?
- [ ] ¿Se evita la orquestación recursiva?

### Revisión de memoria

- [ ] ¿La memoria es legible por personas?
- [ ] ¿La mutación de memoria es explícita?
- [ ] ¿El alcance de la memoria está acotado?
- [ ] ¿El estado persistente está justificado operativamente?
- [ ] ¿La memoria local del repositorio prevalece sobre la memoria global del usuario?
- [ ] ¿La promoción de memoria canónica requiere aprobación humana explícita?
- [ ] ¿Se evita convertir una preferencia local en doctrina general?

---

## Gobernanza de la complejidad

### Preguntas finales

- [ ] ¿Esto reduce o aumenta la complejidad operativa?
- [ ] ¿Reduce o aumenta la carga cognitiva?
- [ ] ¿Las personas todavía pueden gobernar el sistema?
- [ ] ¿La arquitectura se puede mantener bajo presión?
- [ ] ¿La complejidad es proporcional al problema?
- [ ] ¿Se puede revertir?
- [ ] ¿Es observable?
- [ ] ¿Introduce sofisticación sin necesidad?

---

## Principio final

> La complejidad debe justificarse de forma continua.

La mejor arquitectura no es la más sofisticada.

Es la que sigue siendo comprensible, mantenible, gobernable y estable en la operación bajo presión real.
