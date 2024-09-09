---
dg-publish: true
---

# Los mapas

Un **mapa** es una representación gráfica simplificada de un [territorio](https://es.wikipedia.org/wiki/Territorio "Territorio") sobre una superficie bidimensional, que puede ser plana, esférica o incluso poliédrica. Esta representación mantiene ciertas propiedades [métricas](https://es.wikipedia.org/wiki/Espacio_m%C3%A9trico "Espacio métrico") que permiten medir distancias, ángulos o superficies y relacionarlas con la realidad. Las propiedades métricas del mapa dependen de la proyección utilizada, y en algunos casos se aplican coeficientes conocidos para corregir las medidas y minimizar las distorsiones.

> [!caption|right] Proyecciones de mapas
> ![mapas-proyecciones](https://i.imgur.com/PN3JC1b.png)


Existen muchos tipos de mapas, cada uno especializado en una tarea particular. No hay un mapa perfecto; más bien, hay un mapa diseñado para cada propósito específico. Algunos mapas priorizan la representación de áreas iguales, mientras que otros se enfocan en mantener los ángulos sin distorsionar. La diferencia entre los mapas radica en las proyecciones que se utilizan para convertir la superficie curva de la Tierra en una representación plana.

## Proyecciones de Mapas

Las proyecciones de mapas son técnicas matemáticas que se utilizan para transformar la superficie de la Tierra en diferentes tipos visión. Cada tipo de proyección tiene sus propias ventajas y desventajas, y se elige en función del objetivo del mapa.

Dicho de otra forma las proyecciones son el mismo mapa pero deformando áreas y ángulos, y cambiando el sistema de referencia central.

Entre las proyecciones más conocidas se encuentra la proyección de [Mercator](https://es.wikipedia.org/wiki/Proyecci%C3%B3n_de_Mercator) (proyección cilíndrica conforme), la de [Gleason](https://en.wikipedia.org/wiki/Azimuthal_equidistant_projection) típicamente usada para la Tierra plana (proyección cilíndrica conforme) y la de Tierra esférica ([modelo WGS84](https://es.wikipedia.org/wiki/WGS84) o proyección ortográfica conforme).

<video style="width:100%; aspect-ratio:16 / 10;" controls>
  <source src="https://i.imgur.com/mYuWV77.mp4" type="video/mp4">
  Tu navegador no soporta el formato de video.
</video>

<video style="width:100%; aspect-ratio:16 / 10;" controls>
  <source src="https://i.imgur.com/SDvIwYO.mp4" type="video/mp4">
  Tu navegador no soporta el formato de video.
</video>

### Proyección de Mercator

La **proyección de Mercator**, desarrollada por Gerardus Mercator en 1569desarrollada por Gerardus Mercator en 1569, es una proyección cilíndrica conforme. Esta proyección hace que los países del Norte aparezcan mucho más grandes en comparación con los países del Sur. Históricamente, se ha sugerido que esta proyección fue diseñada para beneficiar las rutas comerciales de Europa, en particular de Inglaterra, proporcionando una imagen exagerada del tamaño y poderío de los países europeos. Aunque esta teoría tiene fundamento en el contexto histórico, la proyección de Mercator ha sido ampliamente utilizada en cartografía náutica y es conocida por su utilidad en la navegación.

- **Ventajas**: Preserva los ángulos, facilitando la navegación y la representación precisa de rutas.
- **Desventajas**: Distorsiona las áreas, especialmente en latitudes altas, lo que puede dar una visión exagerada de los tamaños de los continentes.

### Proyección de Gleason

La **proyección de Gleason** es una proyección azimutal equidistante. En esta proyección, la superficie de la Tierra se proyecta sobre un plano tangente en torno al Polo Norte. Esta técnica preserva las distancias desde el punto de tangencia, lo que es útil para mapas que necesitan mostrar distancias precisas desde un centro específico, como en mapas de radar o de distancias aéreas. Sin embargo, al igual que otras proyecciones azimutales, distorsiona las áreas y las formas a medida que uno se aleja del punto central.

- **Ventajas**: Mantiene las distancias precisas desde el punto de tangencia, lo cual es útil para ciertos tipos de análisis.
- **Desventajas**: Las áreas y las formas se distorsionan a medida que se alejan del punto central, lo que puede afectar la precisión de la representación global.

### Proyección Ortográfica

La **proyección ortográfica** es también una proyección azimutal, pero se diferencia al ofrecer una vista de la Tierra como si se estuviera mirando desde el espacio. Esta proyección proyecta la superficie terrestre sobre un plano tangente en un punto específico, proporcionando una representación bastante realista de la Tierra cerca del punto de tangencia. Aunque ofrece una visión precisa de las áreas y formas cercanas al punto central, también distorsiona las áreas y las formas a medida que se aleja del punto de tangencia.

- **Ventajas**: Ofrece una vista realista de la superficie terrestre desde una perspectiva espacial, ideal para imágenes satelitales y representaciones visuales globales.
- **Desventajas**: Las áreas y formas distorsionan a medida que uno se aleja del punto central, lo que limita su precisión en la representación de regiones alejadas del centro.

### Comparación de las Proyecciones

Aunque todas estas proyecciones buscan representar la superficie de la Tierra en un plano, lo hacen de maneras muy distintas:

- **Sistema de Referencia Central**:
  - **Mercator**: Utiliza un cilindro que toca la Tierra en el ecuador, afectando principalmente las regiones polares.
  - **Gleason**: Utiliza un plano tangente en un punto específico, manteniendo distancias precisas desde ese punto.
  - **Ortográfica**: Utiliza un plano tangente que simula una vista desde el espacio, ofreciendo una perspectiva cerca del punto de tangencia.

- **Deformaciones**:
  - **Mercator**: Distorsiona áreas en latitudes altas pero preserva ángulos.
  - **Gleason**: Mantiene distancias desde el punto central pero distorsiona áreas y formas a medida que se aleja del centro.
  - **Ortográfica**: Ofrece una visión realista cerca del punto de tangencia, pero distorsiona áreas y formas lejos del centro.

En resumen, cada proyección tiene sus propias ventajas y desventajas que se alinean con sus objetivos específicos. La elección de la proyección adecuada depende del propósito del mapa y de las propiedades geométricas que se desean preservar o destacar.

## Proyecciones Matemáticas de Superficies

En matemáticas y geometría, una **proyección** es el proceso de transformar un conjunto de puntos de una superficie tridimensional en una superficie bidimensional, de manera que se mantengan ciertas propiedades geométricas. Este concepto se aplica no solo a la representación de la Tierra en un mapa, sino a cualquier superficie y en diversos contextos matemáticos.

### Tipos de Proyecciones

1. **Proyecciones Cilíndricas**
   - **Definición**: En una proyección cilíndrica, se proyecta la superficie tridimensional sobre un cilindro que toca la superficie en una línea o una curva. Luego, el cilindro se desenrolla en un plano.
   - **Características**: Estas proyecciones tienden a preservar los ángulos y la forma local, pero suelen distorsionar el tamaño de las áreas. Un ejemplo es la proyección de Mercator.
   - **Uso**: Se utilizan comúnmente en la navegación debido a la preservación de ángulos.

2. **Proyecciones Cónicas**
   - **Definición**: En una proyección cónica, se proyecta la superficie tridimensional sobre un cono que toca la superficie en una línea o una curva. El cono se desenrolla en un plano.
   - **Características**: Estas proyecciones suelen mantener bien la forma y las áreas en una región limitada, como un continente o una región.
   - **Uso**: A menudo se utilizan para mapas de áreas con un mayor desarrollo en latitud, como países o estados.

3. **Proyecciones Azimutales**
   - **Definición**: En una proyección azimutal, se proyecta la superficie tridimensional sobre un plano tangente a la superficie en un punto específico.
   - **Características**: Estas proyecciones pueden preservar las distancias desde el punto de tangencia y los ángulos, pero suelen distorsionar áreas y formas a medida que se alejan del punto central.
   - **Uso**: Se utilizan para representar áreas alrededor de un punto central, como en mapas de radar o de vuelo.

4. **Proyecciones Interseccionales**
   - **Definición**: Estas proyecciones se basan en la intersección de la superficie tridimensional con un plano o una superficie geométrica más compleja.
   - **Características**: La elección del tipo de proyección interseccional puede variar dependiendo de los objetivos del mapeo y las propiedades que se desean preservar.
   - **Uso**: Se aplican en diversas áreas como la arquitectura, diseño gráfico, y análisis de datos espaciales.

### Propiedades Matemáticas de las Proyecciones

Las proyecciones pueden afectar varias propiedades geométricas:

- **Ángulos**: Algunas proyecciones preservan los ángulos (proyecciones conformes), lo que significa que la forma local se mantiene, pero puede haber distorsión en las áreas.
- **Áreas**: Otras proyecciones conservan las áreas (proyecciones equivalentes), asegurando que las proporciones de las áreas sean correctas, aunque las formas pueden distorsionarse.
- **Distancias**: Algunas proyecciones preservan las distancias desde un punto específico (proyecciones equidistantes), lo que es útil para ciertas aplicaciones prácticas.

---

## Referencias
- [Vídeo de TED "Por qué todos los mapas del mundo están equivocados"](https://ed.ted.com/lessons/why-every-world-map-is-wrong-kayla-wolf)
- [Vídeo de Vox "Por qué todos los mapas del mundo están mal"](https://www.youtube.com/watch?v=kIID5FDi2JQ)
- [The true size of](https://thetruesize.com)
- [Lista de proyecciones cartográficas](https://en.wikipedia.org/wiki/List_of_map_projections)
- [Transición de proyeccciones](https://observablehq.com/@d3/projection-transitions)
- [Sede observable](https://apl.esri.com/jg/Distortion/index.html)
- [Generador de mapas mundiales](https://www.worldmapgenerator.com/en/wizard/)