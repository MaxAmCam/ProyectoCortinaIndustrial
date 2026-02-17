# Hito 1 – Análisis y Requerimientos

## Descripción del problema
El problema consiste en diseñar un programa básico en Siemens LOGO que controle tres salidas digitales de forma secuencial y cíclica, donde cada salida permanece activa durante un tiempo definido y posteriormente se apaga, repitiendo el ciclo de manera indefinida.

Situación problema 

En esta situación problema se busca automatizar una cortina de uso industrial utilizada en un lugar donde circulan personas y vehículos de carga. La cortina puede tener diferentes dimensiones de ancho y altura, además de estar fabricada con hule termoformado y barras metálicas en la parte inferior para mantener la tensión, todo esto hace que la cortina tenga un peso elevado. Debido a esto, el sistema debe ser capaz de mover la cortina de forma controlada y segura.

La automatización debe permitir que la cortina se enrolle hasta una altura determinada y en un tiempo específico, el cual se debe poder ajustarse desde una interfaz de operación dentro de un rango de 3 a 5 segundos. También se necesita que la altura máxima de la cortina y los tiempos de espera se puedan configurarse desde la interfaz. El sistema tiene que ser capaz de operar tanto en modo manual como en modo automático, además se debe considerar que existen diferentes tipos de usuarios con permisos distintos. Algo fundamental es la seguridad, ya que durante el movimiento de bajada se debe detectar la presencia de personas u objetos para evitar accidentes y garantizar que su funcionamiento sea seguro.

## Requerimientos del sistema
### Funcionales
- El sistema deberá encender la primera salida durante 5 segundos y posteriormente apagarla.
- El sistema deberá encender la segunda salida durante 1 segundo y posteriormente apagarla.
- El sistema deberá encender la tercera salida durante 4 segundos y posteriormente apagarla.
- El sistema deberá ejecutar las salidas de manera secuencial.
- El sistema deberá repetir el ciclo de forma indefinida.

Situación problema 
- El sistema debe permitir operar la cortina en modo manual y en modo automático
- El sistema debe permitir configurar la altura máxima a la que sube la cortina desde la interfaz de operación
- El sistema debe permitir ajustar el tiempo en que sube la cortina en un rango de 3 a 5 segundos
- El sistema debe operar con dos velocidades de movimiento: una velocidad alta al inicio de la subida y una velocidad baja antes de detenerse
- En modo automático, el sistema debe ejecutar un ciclo completo que incluya la subida de la cortina, un tiempo de espera en la posición superior y la bajada a velocidad lenta
- El sistema debe permitir activar el movimiento desde botones físicos y también desde la interfaz de operación
- El sistema debe mostrar en la interfaz información como la posición de la cortina y el número de ciclos realizados

### Técnicos
Situación problema
- El sistema debe contar con un actuador capaz de levantar y bajar la cortina considerando su peso y dimensiones
- El sistema debe utilizar sensores para definir y detectar los límites superior e inferior del movimiento de la cortina
- El sistema debe permitir la configuración de parámetros como tiempos, alturas y velocidades desde la interfaz del usuario
- El sistema de control debe ser capaz de gestionar el cambio de velocidades durante el movimiento de la cortina
- El sistema debe estar diseñado para operar de manera confiable y segura en un entorno industrial

### Seguridad
Situación problema
- El sistema debe detener el movimiento de bajada cuando se detecte la presencia de un objeto o de una persona
- Al detectar un obstáculo durante el cierre el sistema debe invertir el movimiento y subir la cortina nuevamente
- El sistema no debe permitir que la cortina se mueva fuera de los límites establecidos para evitar daños mecánicos
- El sistema debe generar y mostrar alarmas cuando se detecten situaciones de riesgo, como la detección de obstáculos
- El acceso a configuraciones críticas del sistema debe estar restringido a usuarios autorizados

## Diagrama de bloques
<img width="704" height="185" alt="image" src="https://github.com/user-attachments/assets/c6ffc489-9f33-42f8-b465-ff9f63d50de0" />

## Conclusiones del análisis
A partir del análisis de la situación problema, podemos concluir que la automatización de la cortina industrial requiere una integración adecuada de elementos mecánicos, eléctricos y de control. El punto más importante del sistema es la seguridad durante su operación, sobre todo en el movimiento de bajada. Definir claramente los requerimientos desde esta etapa nos permite establecer una base sólida para el diseño del sistema y para las siguientes fases del proyecto.
