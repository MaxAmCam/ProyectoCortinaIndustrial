# Hito 1 – Análisis y Requerimientos

## Descripción del problema
En esta situación problema se busca automatizar una cortina de uso industrial utilizada en un lugar donde circulan personas y vehículos de carga. La cortina puede tener diferentes dimensiones de ancho y altura, además de estar fabricada con hule termoformado y barras metálicas en la parte inferior para mantener la tensión, todo esto hace que la cortina tenga un peso elevado. Debido a esto, el sistema debe ser capaz de mover la cortina de forma controlada y segura.

La automatización debe permitir que la cortina se enrolle hasta una altura determinada y en un tiempo específico, el cual se debe poder ajustarse desde una interfaz de operación dentro de un rango de 3 a 5 segundos. También se necesita que la altura máxima de la cortina y los tiempos de espera se puedan configurarse desde la interfaz. El sistema tiene que ser capaz de operar tanto en modo manual como en modo automático, además se debe considerar que existen diferentes tipos de usuarios con permisos distintos. Algo fundamental es la seguridad, ya que durante el movimiento de bajada se debe detectar la presencia de personas u objetos para evitar accidentes y garantizar que su funcionamiento sea seguro.

## Requerimientos del sistema
### Funcionales
- El sistema debe permitir operar la cortina en modo manual y en modo automático
- El sistema debe permitir configurar la altura máxima a la que sube la cortina desde la interfaz de operación
- El sistema debe permitir ajustar el tiempo en que sube la cortina en un rango de 3 a 5 segundos
- El sistema debe funcionar con dos velocidades de movimiento: una alta al inicio de la subida y una velocidad baja antes de detenerse
- En modo automático el sistema debe ejecutar un ciclo completo que incluya la subida de la cortina, un tiempo de espera en la posición superior y la bajada a velocidad lenta
- El sistema debe permitir activar el movimiento desde botones físicos y también desde la interfaz de operación
- El sistema debe mostrar en la interfaz información como la posición de la cortina y el número de ciclos realizados
- El sistema debe permitir el acceso a distintas funciones según el tipo de usuario

### Técnicos
- El sistema debe contar con un actuador capaz de levantar y bajar la cortina considerando su peso y dimensiones
- El sistema debe utilizar sensores para detectar y definir  los límites superior e inferior del movimiento de la cortina
- El sistema debe permitir que se configuren parámetros como tiempos, alturas y velocidades desde la interfaz del usuario
- El sistema de control debe ser capaz de gestionar el cambio de velocidades durante el movimiento de la cortina
- El sistema debe estar diseñado para operar de manera confiable y segura en un entorno industrial

### Seguridad
- El sistema debe detener el movimiento de bajada cuando se detecte la presencia de un objeto o de una persona
- Al detectar un obstáculo durante el cierre el sistema debe de subir la cortina nuevamente
- El sistema no debe permitir que la cortina se mueva fuera de los límites para evitar daños mecánicos
- El sistema debe mostrar alarmas cuando se detecten situaciones de riesgo, como que se detecte un obstáculo
- El acceso a configuraciones importantes del sistema debe estar restringido a usuarios autorizados

## Diagrama de bloques
<img width="704" height="185" alt="image" src="https://github.com/user-attachments/assets/c6ffc489-9f33-42f8-b465-ff9f63d50de0" />
El funcionamiento del sistema sigue el flujo: sensores y botones (medición y entrada de señales) → sistema de control LOGO (procesamiento y toma de decisiones) → actuador/motor (actuación) → sistema mecánico (movimiento de la cortina), mientras que la interfaz de operación permite la supervisión y configuración por parte del usuario.

## Tabla I/O v1 (Entradas / Salidas)
| Tipo | Nombre | Descripción | Condición de activación / uso | Notas de seguridad / estado |
|-----|-------|-------------|-------------------------------|-----------------------------|
| DI | Botón Subir | Botón físico para subir la cortina | Se activa cuando el usuario presiona el botón | Uso en modo manual |
| DI | Botón Bajar | Botón físico para bajar la cortina | Se activa mientras el botón esté presionado | Uso en modo manual |
| DI | Botón Paro | Botón de paro del sistema | Se activa al presionar el botón | Señal crítica de seguridad |
| DI | Sensor límite superior | Detecta que la cortina llegó a la posición máxima | Se activa al alcanzar la altura configurada | Evita sobre recorrido |
| DI | Sensor límite inferior | Detecta que la cortina llegó a la posición mínima | Se activa al llegar al fondo | Evita daños mecánicos |
| DI | Sensor de obstáculo | Detecta presencia de personas u objetos | Se activa durante el cierre | Señal crítica de seguridad |
| DO | Motor subir | Activa el motor para subir la cortina | Se activa cuando el sistema ordena subir | Controlado por el sistema |
| DO | Motor bajar | Activa el motor para bajar la cortina | Se activa cuando el sistema ordena bajar | Se bloquea si hay obstáculo |
| DO | Alarma | Señal visual o sonora de alerta | Se activa al detectar un obstáculo o error | Estado de advertencia |
| DO | Indicador de estado | Indica el estado del sistema | Activo durante la operación | Información al usuario |

## Conclusiones del análisis
A partir del análisis de la situación problema, podemos concluir que la automatización de la cortina industrial requiere una integración adecuada de elementos mecánicos, eléctricos y de control. El punto más importante del sistema es la seguridad durante su operación, sobre todo en el movimiento de bajada. Definir claramente los requerimientos desde esta etapa nos permite establecer una base sólida para el diseño del sistema y para las siguientes fases del proyecto.
