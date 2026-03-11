# Hito 4 – Validación Funcional y HMI
## Objetivo del hito
Validar el funcionamiento integrado del sistema mecatrónico y la interacción con el
usuario mediante HMI.

## Estado general del sistema
Marca el estado actual del sistema:
- No funcional ⬜
- Parcialmente funcional ⬜
- Funcional con fallas ⬜
- Funcional estable ☑️
---
## Secuencia de operación validada
## Secuencia de operación validada
1. El sistema inicia en estado de reposo con la cortina en la posición superior, detectada por el sensor magnético superior.

2. El usuario acerca un objeto metálico al sensor inductivo, lo cual envía la señal de activación al PLC.

3. El PLC verifica que el sensor magnético superior esté activo, confirmando que la cortina se encuentra en su posición inicial antes de iniciar el ciclo.

4. Una vez validada esta condición, el controlador activa el motor en sentido de bajada para comenzar el movimiento de la cortina.

5. Durante el recorrido, los sensores magnéticos permiten al sistema conocer la posición de la cortina. Cuando se detecta la posición intermedia junto con el sensor superior, se activa la luz roja de la torre de señalización indicando estado de operación.

6. Mientras la cortina se encuentra en movimiento, el sistema monitorea continuamente el sensor óptico y el sensor capacitivo como condiciones de seguridad.

7. Si el sensor óptico detecta una persona u objeto, o si se activa el sensor capacitivo, el PLC detiene inmediatamente el motor.

8. Si no ocurre ninguna condición de seguridad, la cortina continúa descendiendo hasta que el sensor magnético inferior detecta el final del recorrido.

9. Al activarse el sensor inferior, el PLC detiene el motor, enciende la luz verde y activa un temporizador de 10 segundos.

10. Una vez finalizado el temporizador, el PLC activa el motor en sentido de subida hasta que el sensor magnético superior vuelve a detectarse, regresando el sistema a su estado inicial.
---
## Validación de sensores
| Sensor | Condición probada | Resultado esperado | Resultado obtenido |
|------|------------------|------------------|------------------|
---
## Validación de actuadores
| Actuador | Acción | Resultado esperado | Resultado obtenido |
|--------|--------|------------------|------------------|
---
## Validación del controlador (LOGO)
Describe:
- Temporizaciones
- Condiciones lógicas
- Interlocks o seguridades implementadas
---
## Fallas detectadas
Describe **máximo 3** fallas relevantes encontradas durante la validación.
---
## Ajustes realizados
| Falla | Ajuste realizado | Resultado |
|-------|------------------|-----------|
| Atascamiento en la cortina | Volteamos la cortina y corregimos fallas en la impresión 3D | La cortina funcionó correctamente |
| El LOGO! no encendía | Cambiamos el fusible | El LOGO! se encendió sin problemas |
| El HMI no cargó correctamente en el LOGO! | Volvimos a realizar la instalación | El programa funcionó de manera correcta |

---
## Preparación para demostración final
Indica qué está listo y qué falta por afinar:
- Lógica de control☑️
- HMI☑️
- Cableado☑️
- Seguridad☑️
- Evidencias (video/fotos)☑️
---
## Reflexión breve del equipo
¿Qué fue lo más crítico de esta etapa?
