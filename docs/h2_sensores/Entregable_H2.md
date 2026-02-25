# Hito 2 – Selección de Componentes

## Sensores seleccionados
| Sensor | Variable | Tipo de señal | Justificación |
|------|----------|---------------|---------------|
|Sensor magnético de proximidad FESTO SME-8M-DS-24V-K-2,5-OE|Campo magnético (posición de la cortina)|Digital 24 VDC|Utilizaremos este sensor para detectar las posiciones (superior, media e inferior) de la cortina  industrial. Funciona mediante un imán, el cual está instalado en el mecanismo móvil; así podemos saber cuándo la cortina está abierta, en posición intermedia o completamente cerrada.|
|Sensor de proximidad capacitivo LJC18A3-B-Z/BX (NPNO-N)|Variación de capacitancia (presencia de material)|Digital NPN – Normalmente Abierto|Este sensor nos permite detectar materiales metálicos y no metálicos, como plástico, madera o incluso líquidos. Puede utilizarse para detectar la presencia de objetos y materiales en el área de operación.|
|Sensor de proximidad inductivo LJ12A3-4-Z/BX (NPN-NO)|Campo electromagnético (detección de metal)|Digital NPN – Normalmente Abierto |Se utiliza para detectar únicamente partes metálicas del sistema. También se puede utilizar como un botón de inicio sin contacto, acercando una pieza metálica al sensor para activar el sistema; esto nos da una mayor seguridad.|
|Sensor de proximidad infrarrojo E3F-DS30P1 (PNP-NO)|Radiación infrarroja reflejada (presencia de objeto)|Digital PNP – Normalmente Abierto|Se utilizará como sensor de seguridad para detectar si hay personas u objetos en el área de operación.|


## Actuadores seleccionados
| Actuador | Función | Tipo | Justificación |
|--------|---------|------|---------------|

## Riesgos y consideraciones
¿Qué podría fallar y cómo se mitiga?

1) Fallos en el sensor magnético de proximidad:Falla por separación del imán del mecanismo móvil, corrosión en entornos húmedos o cableado dañado en movimientos repetidos. Daño: Detección errónea de posiciones (ej: cree cortina cerrada cuando está abierta), causando atascos o colisiones.
2) Fallos en el sensor de proximidad capacitivo:Falla por acumulación de polvo/humedad alterando capacitancia, interferencias de materiales cercanos o polaridad inversa. Daño: Falsas detecciones de objetos, cierre prematuro, riesgo de aplastamiento o daños.
3) Fallos en el sensor de proximidad inductivo:Falla por corrientes en metales, vibraciones o sobrecarga eléctrica por demasiado Amperaje. Daño: Activaciones inesperadas como botón de inicio falso, arranque no autorizado de cortina o fallos en detección metálica, exponiendo usuarios.
4) Fallos en el sensor de proximidad infrarojo:Falla por suciedad en lente bloqueando IR, cambios de temperatura/humedad o reflexión por superficies brillantes. Daño: No detectar personas/objetos, permitiendo que cierre sobre ellos. Riesgo de accidentes graves como atrapamientos o lesiones.

Como se mitiga cada problema?

1.1) Sensor magnético de proximidad:Fijar imán con adhesivos resistentes y cables flexibles y limpiar corrosión periódicamente. Tambien desconectar antes de mantenimiento.
1.2) Sensor de proximidad capacitivo:Limpiar superficie de detección regularmente para evitar polvo/humedad y verificar polaridad .
1.3) Sensor de proximidad inductivo:Alejar metales no deseados.
1.4) Sensor de proximidad infrarojo:Limpiar lente óptico frecuentemente. Monitorear diagnóstico en tiempo real y evitar reflexiones falsas con calibración.
