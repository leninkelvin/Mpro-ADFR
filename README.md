# Mpro-ADFR
Convocatoria de Ciencia Básica y/o Ciencia de Frontera Modalidad: Paradigmas y Controversias de la Ciencia 2022  

Número de propuesta: 319268. 

Título: Identificación de inhibidores enzimáticos contra el coronavirus de 2019 (SARS-CoV-2). 

Responsable Técnico: GERARDO SANTOS LOPEZ Institución: INSTITUTO MEXICANO DEL SEGURO SOCIAL. 

Colaboradores: LENIN DOMÍNGUEZ RAMÍREZ 

# Introducción:

El paper "X-ray screening identifies active site and allosteric inhibitors of SARS-CoV-2 main protease" ( doi: 10.1126/science.abf7945 ) describe 32 estructuras de la proteasa del virus del SARS-CoV-2. Los autores usaron cristalografia en lote para encontrar fármacos que mostraran actividad antiviral.
De estas 37 estructuras, 14 son de ligandos no covalentes. Es decir, ligandos que no reaccionaron con la cisteina catalítica formado un enlace covalente. En estos 14 ligandos no covalentes se describe un total de 7 sitios de unión dos de los cuales son alostéricos. Un esta entre dominios de la proteasa y otro en una intercara entre dímeros. 

# Descripción de los datos.

Este repositorio tiene archivos originales para receptores (protease) y ligandos (los cristalizados en el paper mencionado arriba). Los archivos se dividen en receptores y ligandos. 

Los ligandos estan separados de su receptor pero en su misma posicion relativa. Es decir, se pueden usar para comparar los resultados del docking (controles positivos) o, como se hizo con los archivos trg, como referencia para reducir la busqueda del docking al sitio conocido.

Todos los archivos de receptores contienen únicamente a las proteínas, todos los heteroátomos (iones, buffer, moléculas de agua, ligandos) han sido retirados. De acuerdo al artículo, todas las estructuras fueron obtenidas a pH 7.5. Todos los receptores son un monomero y estan alineados de manera que los resultados de cualquiere receptor pueden compararse con otros facílmente. Se incluyen PDBs y PDBQTs. Estos últimos pueden usarse con programas de docking como Autodock, Vina o gnina. 

Para ADFR se requiere un archivo trg. Los receptores y los ligandos se utilizaron en la generación de estos archivos. Esto se describe brevemente a continuación. 

Se uso el agfrgui, se cargó el receptor correspondiente a cada ligando. El ligando se uso para definir una caja entorno al sitio de interacción y se le incremento el tamaño de "padding" a 8. Una vez hecho esto se calcularon las cavidades y se generaron las rejillas para todos los átomos que soporta ADFR. 
Esto último quiere decir que aunque se generó una rejilla basado en un ligando de composición química conocida, se pueden generar rejilas que describan el sitio de unión en función de átomos que no esten presentes en el ligando. Esto permite usar estas rejillas para tamizaje con moléculas no representadas por los átomos de los ligandos de referencia.

Una guía detallada del uso de ADFR y la preparación de los archivos se puede encontrar [aquí](https://github.com/leninkelvin/ADFR-of-varying-flexibility).

Nota, los archivos descomprimidos ocuparan 120 Mbs.
