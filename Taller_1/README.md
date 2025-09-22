# Talleres-Ciencia-de-Datos Análisis de Reservas Hoteleras

## Integrantes del equipo

-  Lina Ojeda - 202112324 - l.ojedaa@uniandes.edu.co
-  William Toro - 201112526 - wy.toro993@uniandes.edu.co

## Estructura del repositorio

La carpeta principal (Taller1) contiene todos los recursos necesarios para ejecutar y documentar el proyecto:
- **Taller1.ipynb**: notebook principal, ejecutable en Google Colab, que contiene el análisis exploratorio, multivariado y pruebas de hipótesis.  
- **hotel_bookings_modified.csv**: dataset base de reservas hoteleras usado para el análisis.  
- **hotel_dict.csv / hotel_dictionary.csv**: diccionarios de variables con información detallada sobre los campos del dataset.  
- **Resumen_Ejecutivo.pdf**: documento con el planteamiento del problema, solución, valor generado, insights estratégicos y próximos pasos.  
- **README.md**: documentación general del proyecto con objetivo, alcance, conclusiones, instrucciones de ejecución y dependencias.  

## Resumen

El presente proyecto analiza datos de reservas hoteleras con el fin de identificar patrones que permitan reducir cancelaciones y mejorar la ocupación.  
Se detectó que:
- Las reservas con alta anticipación presentan una probabilidad de cancelación mucho mayor.  
- Enero se confirma como un mes de baja demanda, representando un reto en la estrategia de ocupación.  
- Las estadías más largas se concentran en hoteles tipo resort, mientras que los city hotels tienen menor volumen de reservas, incluso en temporada alta.  
- Existe dependencia entre el canal de distribución y las cancelaciones, aunque la magnitud del efecto es moderada.  

Este análisis proporciona una base sólida para definir estrategias comerciales basadas en datos, como políticas diferenciadas de cancelación, promociones para meses de baja ocupación y segmentación por tipo de cliente y canal de distribución.

## Resumen Ejecutivo

El resumen ejecutivo con el detalle de problema, solución, valor y conclusiones estratégicas se encuentra disponible en el siguiente documento:  

falta agregar el link 

## Objetivo
El objetivo principal de este proyecto es **analizar el comportamiento de las reservas en hoteles de tipo ciudad y resort** con el fin de identificar patrones que permitan a la cadena hotelera:
- **Reducir el nivel de cancelaciones**
- **Mejorar la ocupación**
- **Optimizar la estrategia comercial** en función de factores como la anticipación de la reserva (*lead time*), duración de la estadía, tipo de hotel, tipo de cliente y canal de distribución.

---

## Alcance
El proyecto incluye:
1. **Análisis exploratorio de datos (EDA):**
   - Distribuciones univariadas (categóricas y numéricas) con histogramas, boxplots y gráficas de barras.
   - Evolución temporal de las reservas y análisis de estacionalidad.
   - Identificación de outliers y variables críticas.

2. **Análisis multivariado:**
   - Cruce entre tipo de hotel, tipo de cliente, canal de distribución y estado de cancelación.
   - Comparación de ocupación entre hoteles tipo resort y ciudad.
   - Impacto del *lead time* en la probabilidad de cancelación.

3. **Pruebas de hipótesis estadísticas:**
   - Diferencia de medias (t-test de Welch) en variables como ADR (tarifa diaria promedio) y *lead time* entre reservas canceladas y no canceladas.
   - Chi-cuadrado para medir dependencia entre canal de distribución y cancelaciones.
   - Análisis de estacionalidad con prueba de hipótesis en meses de baja demanda (ejemplo: Enero).

4. **Generación de insights accionables** para la toma de decisiones estratégicas en la cadena hotelera.

---

## Conclusiones e Insights
1. **Duración de la estadía y tipo de hotel:**  
   Las estadías más largas se concentran en hoteles tipo resort, mientras que las estadías cortas predominan en hoteles de ciudad.

2. **Estacionalidad en las reservas:**  
   Enero presenta un número significativamente menor de reservas en ambos tipos de hoteles, lo que lo convierte en un mes de baja ocupación.

3. **Comparación entre tipos de hotel:**  
   La cantidad de reservas en hoteles de ciudad es considerablemente más baja que en resorts, especialmente en temporada alta.

4. **Lead time y cancelaciones:**  
   Las reservas hechas con mayor anticipación tienden a mostrar una tasa de cancelación más alta. Un *lead time* superior a 6 meses presenta probabilidades de cancelación cercanas al 75%.

5. **ADR (Average Daily Rate):**  
   Existe una diferencia estadísticamente significativa en la tarifa diaria promedio (ADR) entre reservas canceladas y no canceladas, aunque el tamaño del efecto es pequeño.

6. **Canal de distribución y cancelaciones:**  
   Se encontró dependencia estadísticamente significativa entre el canal de distribución y la probabilidad de cancelación. Sin embargo, la magnitud del efecto (Cramér's V ≈ 0.2) indica que la asociación es débil.

---

## Instrucciones de ejecución
1. Abrir la carpeta Taller1 hacer click en el notebook denominado Taller1.ipynb una vez dentro del noteboock hacer clic en el botón **"Abrir en Colab"** que aparece en la parte superior del notebook en este repositorio.  
  
2. Una vez en Google Colab, no es necesario cargar manualmente los datos.  
   El notebook ya está configurado para acceder directamente a los archivos desde este repositorio de GitHub mediante URL.

3. Ejecutar todas las celdas del notebook (`Runtime > Run all` o `Entorno de ejecución > Ejecutar todo`).

---

## Dependencias
El proyecto fue desarrollado en **Python 3.9+** y es completamente compatible con **Google Colab**.  
Las librerías principales son:
- pandas
- numpy
- matplotlib
- seaborn
- scipy

En Colab estas librerías ya están preinstaladas, por lo que no requiere instalación adicional.


