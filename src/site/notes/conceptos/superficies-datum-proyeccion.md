---
{"dg-publish":true,"permalink":"/conceptos/superficies-datum-proyeccion/"}
---


# Datum y Proyección para Superficies Generales

Cuando hablamos de **datum** y **proyección**, no necesariamente nos referimos a la Tierra. Estos conceptos pueden aplicarse a **cualquier superficie continua y suficientemente grande** que queramos mapear, como cuerpos celestes, asteroides, planetas hipotéticos, o incluso superficies industriales complejas (tanques, hangares, estructuras curvas).

---

## 1. Datum: marco de referencia para cualquier superficie

Un **datum** es un **sistema de referencia que define posiciones sobre una superficie**. Sus elementos fundamentales son:

- Un **origen**, que puede ser un punto físico sobre la superficie o un centro de masa del objeto.
- Una **geometría de referencia**, que aproxima la forma del objeto: puede ser esférica, elipsoidal, cilíndrica, cónica o totalmente arbitraria.
- La **orientación** de los ejes de coordenadas, que sirve para establecer cómo se miden las posiciones.

> En términos generales: el datum transforma puntos de la superficie a **coordenadas medibles y comparables** en un sistema común.

### Métodos para definir un datum en cualquier superficie

1. **Observaciones astronómicas o ambientales (si aplica)**  
    Para cuerpos que orbitan, se pueden usar referencias celestes como estrellas o puntos fijos conocidos. En la antigüedad, se medían las posiciones de estrellas y del Sol para determinar latitudes y longitudes.
    - La **latitud** se obtenía midiendo la altura del **Ecuador celeste** o del **Zenit de una estrella** respecto al horizonte.
    - La **longitud** se determinaba por observación de los meridianos celestes y relojes precisos.

2. **Triangulación o medición directa de la superficie**
    - Se pueden usar puntos de referencia conocidos y medir distancias y ángulos entre ellos.
    - Se construyen **redes geodésicas locales** adaptadas a la geometría de la superficie. Esto permitía construir mapas con gran precisión usando el concepto de **gran círculo** entre los puntos y el Ecuador celeste.

3. **Modelos matemáticos de la superficie**
    - Para superficies irregulares, se puede usar un **modelo paramétrico** o una malla 3D como referencia.
    - Cada punto de la superficie se proyecta sobre este modelo para obtener coordenadas.

#### Ejemplos de datum en superficies genéricas

La siguiente tabla propone orígenes y métodos prácticos para definir un datum en distintos tipos de superficies. Son ejemplos: cada proyecto puede adaptar la elección según precisión requerida y restricciones prácticas.

| Objeto / Superficie         | Origen / Referencia                         | Método de definición                         | Comentario / uso principal                                   |
| --------------------------- | ------------------------------------------- | -------------------------------------------- | ------------------------------------------------------------ |
| Plano (parcelas, talleres)   | Un punto de esquina o una marca geodésica   | Estación total, GNSS local, medición directa | Conveniente para topografía local; fácil de mantener         |
| Esférico / Elipsoide        | Centro de masa (o centro del elipsoide)     | Observación astronómica, radar, GNSS         | Usado para cuerpos celestes y mapas globales                 |
| Superficie irregular        | Punto central de malla o referencia local    | Escaneo 3D (LiDAR/photogrammetry), malla 3D  | Datum definido por malla poligonal; útil en ingeniería y AR  |
| Superficie industrial curva | Eje geométrico, intersección de referencias  | Medición directa, CAD, estaciones totales    | Para piezas y estructuras: referencia a elemento de diseño   |
| Satélite/vehículo espacial  | Centro de masa + ejes principales           | Telemetría, modelos CAD, radiometría         | Permite control de actitud y navegación                      |
| Asteroide / pequeño cuerpo  | Centro de masa aproximado + vértices locales| Modelado con sondas, fotogrametría orbital   | Datum dependiente de malla y referencias desde misión        |

#### Modelo Tierra elipsoide convexo — datum

> El paso a los **datum geodésicos** vino recién con la **triangulación global** y los **métodos gravimétricos y satelitales** del siglo XX.

| **NAD27 (EE. UU.)**     | Meades Ranch, Kansas               | Triangulación terrestre, estrellas      | Basado en el elipsoide Clarke 1866 |
| ----------------------- | ---------------------------------- | --------------------------------------- | ---------------------------------- |
| **ED50 (Europa)**       | Punto central en Potsdam, Alemania | Observación astronómica y triangulación | Usado en cartografía militar       |
| **Tokyo Datum (Japón)** | Observatorio de Tokio              | Triangulación terrestre y astronomía    | Reemplazado por WGS84              |

#### Modelo Tierra plana

Antes del uso de _datum elipsoidales_ (siglo XIX en adelante), todos los mapas —incluso los “grandes”— se basaban en:
- **coordenadas planas cartesianas o polares**,
- **sistemas visuales o astronómicos simples** (ecuador, polos, rumbos),
- sin referencia matemática global.

Estos mapas antiguos son mapas planos sin datum elipsoidal.

| Época / Mapa          | Tipo de coordenadas                         | Proyección / Base geométrica |
| --------------------- | ------------------------------------------- | ---------------------------- |
| Ptolomeo (s. II)      | Lat/long planas                             | Cónica simple / plano        |
| Portulanos medievales | Cartesianas planas (rumbos)                 | Plana (loxodrómica)          |
| Hereford o Ebstorf    | Simbólicas, planas                          | Azimutal plana               |
| Gleason (1885)        | Polar azimutal plana (modelo terraplanista) | Plano con radio constante    |

En la actualidad se trabaja con modelos planos en mapas locales o proyectos conceptuales, donde el datum y la proyección se simplifican. Aquí se muestra una tabla con opciones prácticas:

| Escenario / Alcance        | Origen / Referencia           | Proyección / Sistema sugerido             | Comentario                                            |
| -------------------------- | ----------------------------- | ----------------------------------------- | ----------------------------------------------------- |
| Parcela agrícola (pequeña) | Estaca o mojón en el terreno  | Plano cartesiano local (X,Y)              | Precisión métrica; suficiente para obras y siembra    |
| Obra civil (urbana)        | Puntos de control topográfico | Sistema local con orientación a meridiano | Mantener coherencia con planos catastrales            |
| Evento temporal (obra)     | Datum temporal (marcadores)   | Coordenadas locales relativas             | Útil cuando no interesa integración con redes mayores |

> A nivel oficial: si el área supera unos pocos kilómetros cuadrados, se suele usar una proyección conforme local (p. ej. UTM o Lambert) para pasar al modelo esférico.

---

## 2. Proyección: representar una superficie en un sistema de coordenadas

Una **proyección** es la forma de trasladar posiciones de la superficie a un **plano o a un sistema de coordenadas manipulable**, respetando la geometría del objeto.

- Para superficies **curvas**, se usan aproximaciones: proyecciones cilíndricas, cónicas o azimutales adaptadas al objeto.
- Para superficies **planas**, se pueden usar coordenadas métricas directas (X, Y, Z).
- Para superficies **irregulares**, se usan mallas 3D o parametrizaciones (u,v) para representar cada punto de manera única.

### Ejemplos de proyección para cualquier superficie

| Superficie                 | Tipo de proyección           | Uso principal               | Comentario                                               |
| -------------------------- | ---------------------------- | --------------------------- | -------------------------------------------------------- |
| Esfera o elipsoide         | Cilíndrica, cónica, azimutal | Mapas globales, navegación  | Conserva ángulos, áreas o distancias según la proyección |
| Superficie cilíndrica      | Cilíndrica plana             | Mapas de tubos o tanques    | Fácil medición de distancias rectas                      |
| Superficie irregular       | Paramétrica (u,v)            | Modelado 3D, simulaciones   | Cada punto se ubica mediante parámetros locales          |
| Plano o superficie pequeña | Cartesiana (X,Y)             | Obras civiles, inspecciones | Coordenadas métricas directas, sin distorsión            |

#### Modelo Tierra elipsoide convexo — proyección

| Sistema                 | Tipo                            | Uso principal            | Comentario                                                 |
| ----------------------- | ------------------------------- | ------------------------ | ---------------------------------------------------------- |
| UTM                     | Proyección cilíndrica conformal | Mapas topográficos y GPS | Divide el globo en zonas de 6° de longitud                 |
| Lambert Conformal Conic | Proyección cónica               | Mapas regionales         | Conserva formas en zonas medias                            |
| Plano cartesiano local  | Plano                           | Parcelas, obras civiles  | Coordenadas métricas directas, fácil cálculo de distancias |

#### Modelo Tierra plana

Cuando se trabaja con superficies pequeñas, como parcelas agrícolas o urbanas, no es práctico usar coordenadas esféricas. Se emplean **datum locales planos**, donde:

- El sistema de coordenadas se define en **X, Y sobre un plano**.
- Las distancias y ángulos son métricos directos.
- No se necesita referirse al Ecuador celeste, aunque históricamente estos planos se alineaban con meridianos y paralelos locales.

En el pasado  existieron **mapas grandes (continentales o incluso “mundiales”)** que usaban **coordenadas cartesianas planas** mucho antes de la invención de los _datum elipsoidales_. En ellos, las posiciones se calculaban en **planos o discos**, no sobre un modelo matemático de la Tierra. Vamos a verlo con ejemplos claros.

---

### Contrato técnico breve (inputs / outputs / errores)

- Inputs: definición de la superficie (malla, ecuación analítica o descripción geométrica), puntos de control y precisión requerida.
- Outputs: datum (origen, ejes), proyección seleccionada (fórmulas o parámetros) y transformación entre sistema superficial y plano.
- Errores / modos de fallo: datum mal definido (origen fuera de la superficie), pérdida de precisión por proyección inadecuada, ambigüedad en mallas no orientadas.

### Casos límite y consideraciones

- Área grande (> cientos de km): preferir datum elipsoidal/global y proyecciones por zonas (UTM) para controlar distorsión.
- Superficies altamente irregulares: usar mallas 3D y parametrizaciones locales (u,v); evitar forzar una única proyección global.
- Sistemas mecánicos o industriales: alinear el datum con elementos de diseño CAD para reducir errores de manufactura.
- Necesidad de interoperabilidad (GNSS, mapas): documentar claramente transformaciones entre datum (p. ej. NAD27 → WGS84).

---

## 3. Resumen general

- **Datum:** Define un marco de referencia para medir posiciones sobre cualquier superficie, no solo planetas. Puede basarse en puntos físicos, geometrías ideales o mallas 3D.
- **Proyección:** Convierte coordenadas de la superficie a un sistema manipulable, ya sea plano o paramétrico.
- **Superficies planas vs. curvas:** Los sistemas planos permiten cálculos directos; las superficies curvas requieren proyecciones adaptadas a la geometría.

> En conclusión, datum y proyección son **herramientas universales de referencia espacial**, aplicables a cualquier objeto grande o complejo, permitiendo ubicar y representar puntos de manera precisa y consistente.
