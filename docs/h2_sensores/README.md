# Hito 2 – Selección de Componentes

## Sensores seleccionados
| Sensor | Variable | Tipo de señal | Justificación |
|------|----------|---------------|---------------|
|Sensor magnético de proximidad FESTO SME-8M-DS-24V-K-2,5-OE|Campo magnético (posición de la cortina)|Digital 24 VDC|Utilizaremos este sensor para detectar las posiciones (superior, media e inferior) de la cortina  industrial. Funciona mediante un imán, el cual está instalado en el mecanismo móvil; así podemos saber cuándo la cortina está abierta, en posición intermedia o completamente cerrada.|
|Sensor de proximidad capacitivo LJC18A3-B-Z/BX (NPN-NO)|Variación de capacitancia (presencia de material)|Digital NPN – Normalmente Abierto|Este sensor nos permite detectar materiales metálicos y no metálicos, como plástico, madera o incluso líquidos. Puede utilizarse para detectar la presencia de objetos y materiales en el área de operación.|
|Sensor de proximidad inductivo LJ12A3-4-Z/BX (NPN-NO)|Campo electromagnético (detección de metal)|Digital NPN – Normalmente Abierto |Se utiliza para detectar únicamente partes metálicas del sistema. También se puede utilizar como un botón de inicio sin contacto, acercando una pieza metálica al sensor para activar el sistema; esto nos da una mayor seguridad.|
|Sensor de proximidad infrarrojo E3F-DS30P1 (PNP-NO)|Radiación infrarroja reflejada (presencia de objeto)|Digital PNP – Normalmente Abierto|Se utilizará como sensor de seguridad para detectar si hay personas u objetos en el área de operación.|

## Diagrama de conexiones


## Riesgos y consideraciones
¿Qué podría fallar y cómo se mitiga?

1) Fallos en el sensor magnético de proximidad:Falla por separación del imán del mecanismo móvil, corrosión en entornos húmedos o cableado dañado en movimientos repetidos. Daño: Detección errónea de posiciones (ej: cree cortina cerrada cuando está abierta), causando atascos o colisiones.
2) Fallos en el sensor de proximidad capacitivo:Falla por acumulación de polvo/humedad alterando capacitancia, interferencias de materiales cercanos o polaridad inversa. Daño: Falsas detecciones de objetos, cierre prematuro, riesgo de aplastamiento o daños.
3) Fallos en el sensor de proximidad inductivo:Falla por corrientes en metales, vibraciones o sobrecarga eléctrica por demasiado Amperaje. Daño: Activaciones inesperadas como botón de inicio falso, arranque no autorizado de cortina o fallos en detección metálica, exponiendo usuarios.
4) Fallos en el sensor de proximidad infrarojo:Falla por suciedad en lente bloqueando IR, cambios de temperatura/humedad o reflexión por superficies brillantes. Daño: No detectar personas/objetos, permitiendo que cierre sobre ellos. Riesgo de accidentes graves como atrapamientos o lesiones.

¿Cómo se mitiga cada problema?

1.1) Sensor magnético de proximidad:Fijar imán con adhesivos resistentes y cables flexibles y limpiar corrosión periódicamente. Tambien desconectar antes de mantenimiento.
1.2) Sensor de proximidad capacitivo:Limpiar superficie de detección regularmente para evitar polvo/humedad y verificar polaridad .
1.3) Sensor de proximidad inductivo:Alejar metales no deseados.
1.4) Sensor de proximidad infrarojo:Limpiar lente óptico frecuentemente. Monitorear diagnóstico en tiempo real y evitar reflexiones falsas con calibración.


## MR2022 -- Registro Experimental de Pruebas de Sensores de Proximidad
## Identificación del Sensor



---

## 1. Sensor de Proximidad Inductivo

| Característica | Descripción |
|---|---|
| Tipo de sensor | Inductivo |
| Modelo | LJ12A3-4-Z/BX |
| Tipo de salida | NPN – Normalmente Abierto |
| Alimentación | 6 – 36 VDC |
| Distancia nominal | 4 mm |
| Tipo de conexión al LOGO | Digital |
| Observaciones iniciales | Detecta únicamente objetos metálicos mediante la generación de un campo electromagnético. |

**Datasheet:**  
https://lorentzzi.com/es/products/proximity-sensor/inductive-proximity-sensor/lj12a3-4-z-bx-3-wire-inductive-proximity-sensor/

---

## 2. Sensor de Proximidad Capacitivo

| Característica | Descripción |
|---|---|
| Tipo de sensor | Capacitivo |
| Modelo | LJC18A3-B-Z/BX |
| Tipo de salida | NPN – Normalmente Abierto |
| Alimentación | 6 – 36 VDC |
| Distancia nominal | 10 mm |
| Tipo de conexión al LOGO | Digital |
| Observaciones iniciales | Detecta materiales metálicos y no metálicos mediante variación de la capacitancia producida por cambios en la constante dieléctrica del entorno. |

**Datasheet:**  
https://www.finglai.com/products/sensors/capacitive-proximity-sensors/LJC18A3-B/

---

## 3. Sensor de Proximidad Óptico Infrarrojo

| Característica | Descripción |
|---|---|
| Tipo de sensor | Óptico Infrarrojo |
| Modelo | E3F-DS30P1 |
| Tipo de salida | PNP – Normalmente Abierto |
| Alimentación | 6 – 36 VDC |
| Distancia nominal | 5 – 30 cm |
| Tipo de conexión al LOGO | Digital |
| Observaciones iniciales | Detecta presencia de objetos mediante emisión y recepción de radiación infrarroja reflejada. |

**Datasheet:**  
https://www.finglai.com/products/sensors/cylinder-amplifier-photoelectric-sensors/E3F-DS30/E3F-DS30P1.html

---

## 4. Sensor Magnético de Proximidad

| Característica | Descripción |
|---|---|
| Tipo de sensor | Magnético |
| Modelo | FESTO SME-8M-DS-24V-K-2,5-OE |
| Tipo de salida | PNP – Normalmente Abierto |
| Alimentación | 5 – 30 VDC |
| Distancia nominal | No especifica distancia en mm |
| Tipo de conexión al LOGO | Digital |
| Observaciones iniciales | Detecta la posición del cilindro neumático mediante un imán instalado en el émbolo, enviando una señal cuando pasa frente al sensor. |

**Datasheet:**  
https://serproindu.cl/wp-content/uploads/2024/09/FICHA-TECNICA-SME-8M-DS-24V-K-25-OE.pdf


------------------------------------------------------------------------

## Resultados por Material Evaluado

| Sensor | Material | ¿Detecta? | Distancia mínima (cm) | Distancia máxima (cm) | Promedio (cm) | Zona inestable | Observaciones técnicas |
|--------|----------|-----------|-----------------------|-----------------------|---------------|----------------|------------------------|
| Capacitivo | Metal | Sí | 0 | 0.3 | 0.15 | > 0.3 cm | Detección estable |
| Capacitivo | Piel | Sí | 0 | 0.5 | 0.25 | > 0.5 cm | Respuesta estable |
| Capacitivo | Madera | Sí | 0 | 0.3 | 0.15 | > 0.3 cm | Variación de capacitancia |
| Capacitivo | Agua | Sí | 0 | 0.3 | 0.15 | > 0.3 cm | Alta constante dieléctrica |
| Capacitivo | Imán | Sí | 0 | 0.5 | 0.25 | > 0.5 cm | Detecta como objeto material |
| Capacitivo | Plástico | No | — | — | — | — | No presentó activación |
| Inductivo | Metal | Sí | 0 | 0.1 | 0.05 | > 0.1 cm | Detecta material conductor |
| Inductivo | Imán | Sí | 0 | 1.3 | 0.65 | > 1.3 cm | Detecta por núcleo metálico |
| Inductivo | Otros materiales | No | — | — | — | — | No conductores |
| Infrarrojo | Metal | Sí | 0 | 30 | 15 | > 30 cm | Reflexión IR estable |
| Infrarrojo | Piel | Sí | 0 | 30 | 15 | > 30 cm | Detección correcta |
| Infrarrojo | Madera | Sí | 0 | 30 | 15 | > 30 cm | Respuesta adecuada |
| Infrarrojo | Agua | Sí | 0 | 30 | 15 | > 30 cm | Detecta superficie reflectiva |
| Infrarrojo | Plástico transparente | No | — | — | — | — | No refleja IR |
| Magnético | Imán | Sí | 0 | 4.6 | 2.3 | > 4.6 cm | Activación por campo magnético |
| Magnético | Otros materiales | No | — | — | — | — | No generan campo magnético |

  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## Prueba de Distancia Incremental

> Mover el objeto en incrementos regulares y registrar comportamiento
> del LED y del LOGO.

---

# Sensor Magnético

| Distancia (mm) | LED del sensor | Entrada en LOGO (1/0) | ¿Detección consistente? | Comentarios |
|---|---|---|---|---|
| 0 | ON | 1 | Sí | N/A |
| 2 | ON | 1 | Sí | N/A |
| 4 | ON | 1 | Sí | N/A |
| 6 | ON | 1 | Sí | N/A |
| 8 | ON | 1 | Sí | N/A |
| 10 | ON | 1 | Sí | N/A |
| 12 | ON | 1 | Sí | N/A |
| 14 | ON | 1 | Sí | N/A |
| 16 | ON | 1 | Sí | N/A |

---

# Sensor de Proximidad Capacitivo

| Distancia (mm) | LED del sensor | Entrada en LOGO (1/0) | ¿Detección consistente? | Comentarios |
|---|---|---|---|---|
| 0 | ON | 1 | Sí | N/A |
| 2 | ON | 1 | Sí | N/A |
| 4 | ON | 1 | Sí | N/A |
| 6 | OFF | 0 | Sí | N/A |
| 8 | OFF | 0 | Sí | N/A |
| 10 | OFF | 0 | Sí | N/A |
| 12 | OFF | 0 | Sí | N/A |
| 14 | OFF | 0 | Sí | N/A |
| 16 | OFF | 0 | Sí | N/A |

---

# Sensor de Proximidad Inductivo

| Distancia (mm) | LED del sensor | Entrada en LOGO (1/0) | ¿Detección consistente? | Comentarios |
|---|---|---|---|---|
| 0 | ON | 0 | Sí | N/A |
| 2 | ON | 0 | Sí | N/A |
| 4 | ON | 0 | Sí | N/A |
| 6 | ON | 0 | Sí | N/A |
| 8 | ON | 0 | Sí | N/A |
| 10 | ON | 0 | Sí | N/A |
| 12 | OFF | 1 | No | N/A |
| 14 | OFF | 1 | No | N/A |
| 16 | OFF | 1 | No | N/A |

---

# Sensor de Proximidad Infrarrojo

| Distancia (mm) | LED del sensor | Entrada en LOGO (1/0) | ¿Detección consistente? | Comentarios |
|---|---|---|---|---|
| 0 | ON | 1 | Sí | N/A |
| 2 | ON | 1 | Sí | N/A |
| 4 | ON | 1 | Sí | N/A |
| 6 | ON | 1 | Sí | N/A |
| 8 | ON | 1 | Sí | N/A |
| 10 | ON | 1 | Sí | N/A |
| 12 | ON | 1 | Sí | N/A |
| 14 | ON | 1 | Sí | N/A |
| 16 | ON | 1 | Sí | N/A |

---

# Conclusión

Durante las pruebas, los sensores magnético, capacitivo e infrarrojo mostraron un funcionamiento consistente, enviando correctamente la señal al PLC LOGO según la presencia del objeto dentro de su rango de detección.

El sensor inductivo presentó inconsistencias a partir de los 12 mm, lo cual coincide con su distancia nominal de detección de 4 mm, indicando que fuera de su rango de operación ya no detecta correctamente el objeto.

Estos resultados confirman el correcto funcionamiento de los sensores dentro de sus rangos especificados en el datasheet.

*(Ajustar rango según especificación del sensor)*


------------------------------------------------------------------------

## Comparación vs Especificación del Fabricante

## Sensor Magnético

| Parámetro                          | Valor Datasheet    | Valor Experimental | Error (%) |
|------------------------------------|--------------------|--------------------|-----------|
| Distancia nominal                  | No especificado    | 4.6cm              | N/A       |
| Tiempo de respuesta (si aplica)    | No especificado    | Inmediato          | N/A       |
| Tipo de material recomendado       | Magnético          | Imán               | -         |

---

## Sensor Capacitivo

| Parámetro                          | Valor Datasheet | Valor Experimental | Error (%) |
|------------------------------------|-----------------|--------------------|-----------|
| Distancia nominal                  |      1cm           |    0.5cm           |     50%      |
| Tiempo de respuesta (si aplica)    |        N/A         |        N/A            |     N/A      |
| Tipo de material recomendado       |    materiales metálicos y no metálicos   |     materiales metálicos y no metálicos               |      -     |

---
## Sensor Inductivo

| Parámetro                          | Valor Datasheet | Valor Experimental | Error (%) |
|------------------------------------|-----------------|--------------------|-----------|
| Distancia nominal                  |                 |                    |           |
| Tiempo de respuesta (si aplica)    |                 |                    |           |
| Tipo de material recomendado       |                 |                    |           |

---

## Sensor Infrarrojo

| Parámetro                          | Valor Datasheet | Valor Experimental | Error (%) |
|------------------------------------|-----------------|--------------------|-----------|
| Distancia nominal                  |                 |                    |           |
| Tiempo de respuesta (si aplica)    |                 |                    |           |
| Tipo de material recomendado       |                 |                    |           |

## Análisis Técnico del Equipo

## 5.1 ¿Coincide la distancia real con la nominal?

Respuesta:

------------------------------------------------------------------------

## 5.2 ¿Qué fenómeno físico explica el comportamiento observado?

(Ejemplo: corrientes de Foucault, constante dieléctrica, reflexión
óptica, campo magnético)

Respuesta:

------------------------------------------------------------------------

## 5.3 ¿Qué materiales generan mejor desempeño? ¿Por qué?

Respuesta:

------------------------------------------------------------------------

## 5.4 ¿Detectaron zonas muertas o inestabilidad?

Respuesta:

------------------------------------------------------------------------

## 5.5 ¿Este sensor sería adecuado para la situación problema del curso?

Justificar técnica y económicamente.

Respuesta:

------------------------------------------------------------------------

## Matriz de Decisión Técnica

  ----------------------------------------------------------------------------
  Criterio      Peso (1--5)  Evaluación del sensor (1--5) Resultado ponderado
  ------------- ------------ ---------------------------- --------------------
  Precisión                                               

  Distancia                                               
  útil                                                    

  Robustez                                                
  industrial                                              

  Inmunidad a                                             
  ruido                                                   

  Costo                                                   

  Facilidad de                                            
  integración                                             
  con LOGO                                                

  **TOTAL**                                               
  ----------------------------------------------------------------------------

------------------------------------------------------------------------

## Conclusión Ingenieril

Redactar una conclusión técnica defendible:

-   ¿Recomendarían este sensor?
-   ¿En qué condiciones sí?
-   ¿En qué condiciones no?
-   ¿Qué riesgos industriales identifican?

Conclusión:

------------------------------------------------------------------------

## Evidencia

![Capacitivo](../GIFTS/Sensor1.gif)

-   Fotografías del montaje:
-   Capturas del programa en LOGO:
-   Video corto de funcionamiento:
-   Datasheet utilizado (link o archivo en repositorio):

------------------------------------------------------------------------

## Bitácora de Aprendizaje

¿Qué aprendieron técnicamente sobre sensores de proximidad que no sabían
antes?

Respuesta:

------------------------------------------------------------------------

> ⚙️ Este documento forma parte del proceso de validación experimental
> para la selección de sensores dentro del proyecto integrador MR2022.
