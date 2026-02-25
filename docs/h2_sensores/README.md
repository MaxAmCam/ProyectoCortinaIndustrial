# Hito 2 – Selección de Componentes

## Sensores seleccionados
| Sensor | Variable | Tipo de señal | Justificación |
|------|----------|---------------|---------------|
|Sensor magnético de proximidad FESTO SME-8M-DS-24V-K-2,5-OE|Campo magnético (posición de la cortina)|Digital 24 VDC|Utilizaremos este sensor para detectar las posiciones (superior, media e inferior) de la cortina  industrial. Funciona mediante un imán, el cual está instalado en el mecanismo móvil; así podemos saber cuándo la cortina está abierta, en posición intermedia o completamente cerrada.|
|Sensor de proximidad capacitivo LJC18A3-B-Z/BX (NPN-NO)|Variación de capacitancia (presencia de material)|Digital NPN – Normalmente Abierto|Este sensor nos permite detectar materiales metálicos y no metálicos, como plástico, madera o incluso líquidos. Puede utilizarse para detectar la presencia de objetos y materiales en el área de operación.|
|Sensor de proximidad inductivo LJ12A3-4-Z/BX (NPN-NO)|Campo electromagnético (detección de metal)|Digital NPN – Normalmente Abierto |Se utiliza para detectar únicamente partes metálicas del sistema. También se puede utilizar como un botón de inicio sin contacto, acercando una pieza metálica al sensor para activar el sistema; esto nos da una mayor seguridad.|
|Sensor de proximidad infrarrojo E3F-DS30P1 (PNP-NO)|Radiación infrarroja reflejada (presencia de objeto)|Digital PNP – Normalmente Abierto|Se utilizará como sensor de seguridad para detectar si hay personas u objetos en el área de operación.|


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




# MR2022 -- Registro Experimental de Pruebas de Sensores de Proximidad

## Curso: Análisis de Elementos de Mecatrónica

## Práctica: Conexión y validación de sensores con Siemens LOGO

## Equipo: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Integrantes: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Fecha: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

------------------------------------------------------------------------

# 1️⃣ Identificación del Sensor

  Parámetro                             Información
  ------------------------------------- ---------------------------------------------
  Tipo de sensor                        Inductivo / Capacitivo / Óptico / Magnético
  Marca / Modelo                        
  Tipo de salida                        PNP / NPN / Relé
  Alimentación                          
  Distancia nominal (según datasheet)   
  Tipo de conexión al LOGO              Digital / Analógica
  Observaciones iniciales               

------------------------------------------------------------------------

# 2️⃣ Resultados por Material Evaluado

> Registrar comportamiento REAL medido en laboratorio.

  ------------------------------------------------------------------------------------------------------
  Material   ¿Detecta?   Distancia   Distancia   Distancia     Zona        Falsas        Observaciones
             (Sí/No)     mínima      máxima      promedio      inestable   detecciones   técnicas
                         estable     estable     efectiva (mm) (mm)                      
                         (mm)        (mm)                                                
  ---------- ----------- ----------- ----------- ------------- ----------- ------------- ---------------
  Acero                                                                                  

  Aluminio                                                                               

  Cobre                                                                                  

  Plástico                                                                               

  Madera                                                                                 

  Vidrio                                                                                 

  Agua                                                                                   

  Imán                                                                                   
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

# 3️⃣ Prueba de Distancia Incremental

> Mover el objeto en incrementos regulares y registrar comportamiento
> del LED y del LOGO.

  -------------------------------------------------------------------------------
  Distancia   LED del sensor   Entrada en     ¿Detección            Comentarios
  (mm)        (ON/OFF)         LOGO (1/0)     consistente? (Sí/No)  
  ----------- ---------------- -------------- --------------------- -------------
  0                                                                 

  2                                                                 

  4                                                                 

  6                                                                 

  8                                                                 

  10                                                                

  12                                                                

  14                                                                

  16                                                                
  -------------------------------------------------------------------------------

*(Ajustar rango según especificación del sensor)*

------------------------------------------------------------------------

# 4️⃣ Comparación vs Especificación del Fabricante

  Parámetro                         Valor Datasheet   Valor Experimental   Error (%)
  --------------------------------- ----------------- -------------------- -----------
  Distancia nominal                                                        
  Tiempo de respuesta (si aplica)                                          
  Tipo de material recomendado                                             

------------------------------------------------------------------------

# 5️⃣ Análisis Técnico del Equipo

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

# 6️⃣ Matriz de Decisión Técnica

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

# 7️⃣ Conclusión Ingenieril

Redactar una conclusión técnica defendible:

-   ¿Recomendarían este sensor?
-   ¿En qué condiciones sí?
-   ¿En qué condiciones no?
-   ¿Qué riesgos industriales identifican?

Conclusión:

------------------------------------------------------------------------

# 8️⃣ Evidencia

-   Fotografías del montaje:
-   Capturas del programa en LOGO:
-   Video corto de funcionamiento:
-   Datasheet utilizado (link o archivo en repositorio):

------------------------------------------------------------------------

# 9️⃣ Bitácora de Aprendizaje

¿Qué aprendieron técnicamente sobre sensores de proximidad que no sabían
antes?

Respuesta:

------------------------------------------------------------------------

> ⚙️ Este documento forma parte del proceso de validación experimental
> para la selección de sensores dentro del proyecto integrador MR2022.
