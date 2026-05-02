ANÁLISIS EXPLORATORIO DE DATOS — CONNECTATEL
OBJETIVO
Realizar un análisis exploratorio completo sobre la base de clientes y registros de uso de ConnectaTel, una empresa de telecomunicaciones, con el fin de identificar problemas de calidad en los datos, segmentar a los usuarios y generar insights accionables para el negocio.

DATASETS UTILIZADOS
users — 4,000 registros con información demográfica de clientes: edad, ciudad, fecha de registro, plan contratado y fecha de cancelación.
usage — 40,000 registros de eventos de uso: tipo de evento (llamada o mensaje), duración, longitud y fecha.

ETAPAS DEL ANÁLISIS
Exploración inicial — revisión de tipos de datos, dimensiones y primeras filas de cada dataset.
Diagnóstico de nulos — identificación de valores faltantes por columna y cálculo de proporciones.
Corrección de sentinels y anomalías — tratamiento del valor -999 en age, los registros ? en city y fechas imposibles en reg_date.
Verificación MAR — análisis de nulos en duration y length cruzados con la columna type para confirmar que son nulos estructurales.
Revisión y estandarización de fechas — conversión a formato datetime e identificación de años fuera de rango.
Visualización de distribuciones — histogramas por tipo de plan para age, cant_mensajes, cant_llamadas y cant_minutos_llamada.
Identificación de outliers — boxplots y cálculo de límites con método IQR para las variables numéricas clave.
Segmentación de clientes — creación de columnas grupo_uso (Bajo, Medio, Alto) y grupo_edad (Joven, Adulto, Adulto Mayor).
Insight ejecutivo — conclusiones orientadas al negocio con recomendaciones accionables.

CÓMO EJECUTAR EL NOTEBOOK
Abre Google Colab
Sube el archivo .ipynb desde tu computadora o ábrelo desde Google Drive
Sube los archivos users.csv y usage.csv al entorno de Colab
Ejecuta las celdas en orden con Shift + Enter o usa Entorno de ejecución → Ejecutar todo

GUÍA DE REPRODUCCIÓN
1. Clonar o descargar el repositorio
2. Asegurarse de tener instaladas: pandas, numpy, matplotlib, seaborn
3. Colocar los datasets en la misma carpeta que el notebook
4. Ejecutar el notebook completo de arriba hacia abajo
5. Los resultados de cada celda se generan en orden secuencial
