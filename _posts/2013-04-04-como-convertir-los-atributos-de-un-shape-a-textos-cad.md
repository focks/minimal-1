---
layout: post
title: Cómo convertir los atributos de un shape a textos CAD
description: 
modified: {}
category: articles
tags: 
  - carmona
  - cartografía histórica
  - formación
  - recursos
image: 
  feature: "jornadaseiel.jpg"
  credit: Texture Lovers
  creditlink: "http://texturelovers.com"
published: true
comments: true
---
 En varias ocasiones me han preguntado cómo pasar los atributos de fichero shape a anotaciones en un fichero CAD. Hace tiempo yo mismo realicé varias consultas en foros de SIG opensource, en concreto gvSIG, pero sin solución. En gvSIG, Kosmo y Qgis probé a editar los  atributos de capas de etiquetas convertidas a puntos  para que se ajustara a los campos que propios de un fichero DXF. Tras la exportación a tipo CAD el resultado fue nulo, al menos al intentar abrirlo con software LibreCAD.

En su día, mi problema se solucionó porque en mi puesto de trabaja tenían licencias de Geomedia y esta conversión de shape a CAD con anotaciones funcionaba bastante bien. Sé también que con ArcGIS este trabajo se realiza sin problemas.

Este tema volvió a mi mente hace pocas semanas, a través de un correo electrónico de un lector. Recuperando el tema por donde lo dejé, y por pura cabezonería, he seguido buscando en Internet sobre el tema. La solución vino de la mano de un programa gratuito llamado DXFAutor que encontré en la web Free Geography Tools.

La conversión con DXFAutor es simple y sencilla. Tras la descarga e instalación, el programa:

    Se carga el shape a convertir (File>Loada Data Set) en el programa. En mi caso he probado con el shape tipo área del catastro que representa los polígonos  de rústica de la provincia de Córdoba (MASA.shp). 


    Tras elegir la opción File>Convert to DXF file,  el sistema nos permitirá exportar elementos gráficos, anotaciones y bloques.
    Para los gráficos, podremos dar nombre a la capa (ej. masa_catastro), seleccionar un color y un estilo de línea.
    En la exportación de anotaciones, editaremos la capa  (ej. masa_txt), asignaremos el tamaño del texto, el color y se elegirá el/los atributos del shape a convertir (yo he seleccionado el número de polígono re rústico que está en el atributo MASA). Comentar que el sistema sitúa el texto en el centro de cada objeto gráfico. Esto puede causar algunos errores de desplazamiento deberemos arreglar a posteriori.

    Por último podemos crear bloques CAD asociados a un elemento gráfico y combinando varios atributos del shape.
    Seleccionamos la carpeta donde se guardará el archivo DXF y…listo.

Fichero CAD final con referencias catastrales

Seguro que alguno de vosotros podrá completar esta entrada con otras maneras de hacer este tipo de trabajo, incluso con algunos de los SIG libres actuales. El debate  está abierto y se agradecen las aportaciones. 
