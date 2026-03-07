```markdown
# Bitácora de Uso de Inteligencia Artificial (IA)

## Información general
- **Equipo: 2**  
- **Integrantes: Joel Soto. Claudio Gómez. Sara Díaz. Max Amezcua**  
- **Semana / Hito:** (H3)  
- **Fecha: 06/03/2026**  

---

## 1️⃣ Uso de IA en esta etapa
Marca una opción:

- ⬜ No se utilizó IA en esta etapa  
- 🟪 Sí se utilizó IA de forma puntual  
- ⬜ Sí se utilizó IA de forma recurrente  

> ⚠️ Si marcas “No se utilizó IA”, completa únicamente las secciones 7, 8 y 9.

---

## 2️⃣ Objetivo del uso de IA
**Descripción del objetivo:**
```
La IA se utilizó como apoyo para entender mejor cómo funciona la lógica de control del sistema que estamos implementando en el PLC LOGO para la cortina industrial.

Se utilizó para:
- Comprender mejor el concepto de interlock de seguridad en sistemas automatizados.
- Tener una idea de qué condiciones prohibidas se deben considerar, por ejemplo evitar que el motor reciba la orden de subir y bajar al mismo tiempo.
- Apoyo en la redacción y organización de la tabla de interlocks y de la explicación de la lógica de control.

```

---

## 3️⃣ Herramienta(s) de IA utilizada(s)
Marca las que apliquen:

- 🟪 ChatGPT  
- ⬜ Copilot  
- ⬜ Otra (especificar): ______________________  

---

## 4️⃣ Prompts relevantes utilizados
Copia **solo los prompts más importantes** (no todos).

> Regla: si no puedes mostrar el prompt, no lo declares como uso válido.

**Prompt 1:**
```

¿Qué es un interlock en sistemas de control industrial y para qué se utiliza?

```

**Prompt 2:**
```

En un sistema con un motor controlado por PLC, ¿cómo se puede evitar que el motor reciba la orden de subir y bajar al mismo tiempo?

```
**Prompt 3:**
```

Ayudame a redactar una explicación sencilla de la lógica de control de una cortina automatizada controlada con PLC LOGO, motor DC y torre de luz

```
---

## 5️⃣ Respuesta(s) obtenida(s) de la IA
Resume o copia los fragmentos **relevantes** de la respuesta.

```
Chatgpt nos explicó que un interlock es una condición de seguridad que se utiliza en sistemas de control para evitar que ocurran acciones que puedan causar fallas o riesgos en el sistema. En nuestro caso, nos dio que se puede implementar un interlock para evitar que el sistema active al mismo tiempo las señales de subir y bajar el motor, ya que esto podría causar problemas eléctricos o mecánicos.

También ayudó a entender cómo se pueden definir condiciones prohibidas dentro de la lógica del sistema y cómo estas pueden bloquearse mediante la programación del PLC. Además se utilizó para apoyar en la redacción de la explicación del funcionamiento general del sistema y la lógica de control.

```

---

## 6️⃣ Evaluación crítica del equipo (OBLIGATORIA)

### 6.1 ¿Qué parte fue útil?
```

Fue útil la explicación del concepto de interlock y su aplicación en sistemas de control, ya que nos ayudó a comprender cómo evitar que ocurran acciones contradictorias dentro del sistema, como activar al mismo tiempo las señales de subir y bajar del motor.

También fue útil saber cómo identificar condiciones prohibidas y la acción de bloqueo, esto nos ayudó a estructurar mejor la tabla de interlocks y a entender cómo describir la lógica de seguridad del sistema en el reporte.

```

### 6.2 ¿Qué parte fue incorrecta, incompleta o no aplicable?
```

Algunas explicaciones fueron muy generales y no estaban adaptadas específicamente al sistema que estamos usando con PLC LOGO y relevadores. Por lo que fue necesario investigar más y ajustar la información al funcionamiento real de nuestra cortina.

```

### 6.3 Decisión final del equipo
Marca y explica:

- ⬜ Se utilizó tal como lo propuso la IA  
- 🟪 Se utilizó parcialmente (adaptado)  
- ⬜ Se rechazó  

**Justificación técnica de la decisión:**
```

La IA se utilizó como apoyo para entender los conceptos y mejorar la redacción del documento, pero la lógica del sistema, las conexiones y las pruebas fueron realizadas por nosotros.

```

---

## 7️⃣ Verificación humana (OBLIGATORIA)
Indica **cómo se verificó** la información antes de usarla:

- ⬜ Comparación con apuntes/clase  
- 🟪 Prueba en el sistema real  
- 🟪 Discusión en equipo  
- 🟪 Consulta con el profesor  
- ⬜ Otra: ______________________  

**Evidencia o explicación breve de la verificación:**
```

La lógica del interlock se probó directamente en el sistema utilizando el PLC LOGO y el motor. El resto de las decisiones sobre la lógica de control y las condiciones prohibidas las fuimos discutiendo y analizando en equipo para asegurarnos de que el funcionamiento fuera correcto.

```

---

## 8️⃣ Impacto del uso de IA en el proyecto
Reflexiona brevemente:

- ¿La IA ahorró tiempo?
- ¿Mejoró la comprensión del problema?
- ¿Introdujo confusión?
- ¿Mejoró la calidad del resultado?

```

La IA nos ayudó a ahorrar tiempo y también a entender mejor algunos conceptos relacionados con los interlocks y la lógica del sistema. Además, fue útil para mejorar la redacción de algunas partes del reporte.

```

---

## 9️⃣ Aprendizaje del equipo sobre el uso de IA
¿Qué aprendieron sobre **cómo usar (o no usar)** IA en un proyecto de ingeniería?

```

Aprendimos que la IA puede servir como una herramienta para aclarar conceptos o ayudar con la redacción de un documento, pero no sustituye las pruebas reales ni el análisis que se tiene que hacer en el proyecto.

```

---

## 🔚 Declaración de honestidad
Declaramos que:
- El uso de IA aquí documentado es **veraz y completo**.
- Las decisiones finales fueron tomadas por el equipo.
- La IA fue utilizada como **apoyo**, no como sustituto del criterio ingenieril.

**Firma del equipo (nombres):**
```
Max Amezcua

Joel Soto

Claudio Gomez

Sara Díaz

