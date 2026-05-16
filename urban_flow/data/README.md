## Conclusiones del Análisis de Infracciones - Proyecto Urban Flow

1. Impacto de la Imputación de Datos (Sesgo Técnico).

    Es fundamental notar que los picos observados en Enero (Mes) y 00:00 hs (Hora) no necesariamente representan la realidad del tráfico, sino que son consecuencia directa del proceso de limpieza solicitado:

    * Concentración en Medianoche: El 20% de las infracciones acumuladas a las 00:00 hs se debe a que este valor fue utilizado para normalizar registros con horas inválidas. En un análisis real de seguridad vial, esto podría llevar a una conclusión errónea sobre el comportamiento nocturno si no se aclara este punto.

    * Efecto Enero: Del mismo modo, el hecho de que Enero sea el mes con más multas responde a la asignación de este mes para todas las fechas que originalmente eran nulas o inválidas.

2.  Comportamiento de Reincidencia (Patentes).

    Al observar el Top 10 de Patentes, vemos que la reincidencia es significativa:

    * Existen vehículos específicos (como la patente WEFLYN) que superan las 35 infracciones.

    * Esto sugiere que una pequeña proporción de conductores es responsable de una gran cantidad de infracciones. Para una política pública, esto indica que sería más efectivo realizar controles dirigidos a estos reincidentes en lugar de medidas generales.

3. Distribución Temporal (Fuera de los valores imputados).

    Si ignoramos el pico de las 00:00 hs y de Enero, observamos:

    * Una distribución relativamente uniforme en meses como Febrero, Diciembre y Julio.

    * Picos de actividad real durante la tarde (14hs a 15hs y 18hs a 20hs), lo que coincide con los horarios de salida laboral y mayor flujo vehicular en zonas urbanas.


**En síntesis:**

El dataset de infracciones de velocidad urbana presenta una calidad de datos inicial deficiente. Respecto a los conductores, existe un grupo reducido de patentes altamente reincidentes, lo que indica que las multas no están funcionando como elemento disuasivo para estos casos. Finalmente, el exceso de velocidad promedio es significativo, superando ampliamente el margen de tolerancia del 5% establecido, lo que refleja un patrón de conducción
irresponsable en las vías analizadas.
 la integración y el análisis de datos visuales y tabulares fue crucial. Las imágenes de matrículas fueron preprocesadas mediante conversión a escala de grises, suavizado Gaussiano y detección de bordes Canny para optimizar la extracción de texto. 
 Luego, EasyOCR se utilizó para obtener las patentes, que se vincularon al dataset de multas con una coincidencia del 80%. Este proceso reveló que 1106 multas carecen de imagen, 625 tienen imágenes asociadas, 83 imágenes no encontraron una multa correspondiente, y 146 de las 433 multas impagas tienen evidencia visual, lo que permite priorizar su gestión
 la integración y el análisis de datos visuales y tabulares fue crucial. Las imágenes de matrículas fueron preprocesadas mediante conversión a escala de grises, suavizado Gaussiano y detección de bordes Canny para optimizar la extracción de texto. 
 Luego, EasyOCR se utilizó para obtener las patentes, que se vincularon al dataset de multas con una coincidencia del 80%. Este proceso reveló que 1106 multas carecen de imagen, 625 tienen imágenes asociadas, 83 imágenes no encontraron una multa correspondiente, y 146 de las 433 multas impagas tienen evidencia visual, lo que permite priorizar su gestión
