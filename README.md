# Optimizador-de-distancias-log-sticas-OSMR-y-geod-sica-
Este repositorio compila una suite de herramientas y scripts en Python desarrollados para la resolución de problemas complejos de logística, ruteo y optimización de cadenas de suministro. El núcleo del proyecto combina el cálculo de distancias geométricas tradicionales con el ruteo real sobre infraestructura vial mediante OpenStreetMap (OSM).

🚀 Descripción General
El objetivo principal de este ecosistema es transicionar de un análisis puramente geométrico (línea recta) a un análisis de fricción espacial real (redes viales). Esto permite calcular con precisión tiempos de traslado, matrices de origen-destino (OD) y optimizar rutas de distribución (como el problema de rutas de vehículos o CVRP).

🛠️ Tecnologías y Librerías Clave
Python 3.x como lenguaje principal.

OSMnx & NetworkX: Para la descarga, modelado y análisis de redes viales e infraestructura de OpenStreetMap.

Geopy: Utilizado para el cálculo rápido de distancias geodésicas (Fórmula de Haversine y modelo de Vincenty).

Shapely & GeoPandas: Para la manipulación, proyección y análisis de datos geoespaciales a gran escala.

Scikit-Learn: Implementación de algoritmos de clustering espacial (DBSCAN) para la zonificación de clientes.

📁 Estructura del Repositorio y Módulos
1. Cálculo de Distancias Geodésicas (/geodesic_distance)
Módulo enfocado en el cálculo de distancias sobre la curvatura terrestre sin considerar la red de caminos. Ideal para filtrados rápidos previos o cuando no se dispone de conectividad a servidores OSM.

Haversine vs. Vincenty: Scripts comparativos de precisión y rendimiento computacional.

Matrices Origen-Destino (OD): Procesamiento masivo de coordenadas para emparejamiento de nodos de distribución con clientes.

2. Enrutamiento con OpenStreetMap y OSMnx (/osm_routing)
Implementación de ruteo real utilizando grafos de infraestructura vial.

Descarga de Grafos de Red: Scripts automatizados para extraer redes de conducción (drive) por ciudades o regiones específicas.

Ruta Más Corta (Shortest Path): Implementación de algoritmos de Dijkstra y A* sobre la red vial para obtener la distancia y el tiempo estimado de viaje (ETA) real entre centros de distribución y puntos de entrega.

3. Clustering Logístico y Zonificación (/logistics_clustering)
Algoritmos aplicados a la segmentación inteligente de mercados y rutas de entrega de última milla.

Segmentación Geográfica: Uso de DBSCAN para agrupar alta densidad de clientes (por ejemplo, datasets de más de 10,000 puntos) y delimitar zonas operativas eficientes.

Modelos de Ruteo (CVRP): Base lógica para la asignación de flotas basada en las distancias reales calculadas en los módulos anteriores.

📈 Casos de Uso e Impacto
Optimización de Rutas Interestatales: Simulación y evaluación de rutas críticas de suministro (ej. corredores logísticos complejos y análisis de tiempos de entrega).

Última Milla Eficiente: Transición de cálculos teóricos "en línea recta" a distancias reales por calle, reduciendo el margen de error en la planeación del combustible y ventanas de entrega de operadores.

Análisis de Productividad: Integración de matrices de distancia con tableros de analítica (Power BI) para evaluar el rendimiento real de las rutas de distribución.

🔧 Configuración e Instalación
Para replicar estos proyectos localmente, asegúrate de instalar las dependencias geoespaciales correctas (se recomienda usar un entorno de conda para evitar conflictos con GDAL y Fiona):

🧑‍💻 Autor
Irving Gerardo Campos Gómez - Head of Technological Evolution / Logistics & IT Specialist
