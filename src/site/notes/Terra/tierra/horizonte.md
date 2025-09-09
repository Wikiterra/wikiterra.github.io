---
{"dg-publish":true,"permalink":"/Terra/tierra/horizonte/"}
---


# El horizonte

El **horizonte** es la línea aparente que separa el cielo de la superficie terrestre o marina, es decir, el límite visual entre dos medios.
El término proviene del griego antiguo **ὁρίζων κύκλος** (*horizōn kýklos*), literalmente “círculo separador”, de **ὁρίζειν** (*horizéin*, “delimitar”), a su vez derivado de **ὅρος** (*hóros*, “límite, frontera\*).

De esta raíz proceden las formas modernas en distintas lenguas: *horizonte* (español, portugués, gallego), *horitzó* (catalán), *horizon* (francés, inglés, neerlandés), *orizzonte* (italiano), *orizont* (rumano) y *горизонт* (*gorizont*, ruso).

> [!infobox]
>
> ![Horizonte con puesta de Sol|cover small](https://i.imgur.com/TEvoK23.jpg)
>
> ## Horizonte con puesta de Sol

Este límite físico se forma en torno al observador y genera una línea de visión máxima entre dos medios de separación, la cual se denomina línea del horizonte u horizonte. El horizonte, al ser un concepto óptico, se forma siempre en la superficie de separación entre el aire y el nivel del mar o el punto más lejano del terreno visible.

El horizonte está muy ligado al concepto de [[Terra/concepto/visibilidad\|visibilidad]], ya que según la altura del observador y las condiciones climatológicas las distancias máximas observadas variarán.

## Tipos de horizonte

Existen dos tipos de horizonte: el horizonte geométrico, que depende de la geometría de la superficie, y el horizonte óptico, que viene definido por la óptica del medio. Sin embargo, el horizonte observable, el típico que vemos cuando miramos a lo lejos, es una combinación de ambos: la forma de la superficie y las condiciones ópticas del medio.

### Horizonte geométrico

El horizonte geométrico viene determinado por la geometría o forma de la superficie y es un puro cálculo matemático, nunca puede observarse en la realidad porque siempre interviene la óptica.

#### Geometría plana

- El caso más sencillo es sobre un plano, donde **no existe horizonte geométrico finito**.
- La línea de visión nunca se interrumpe por curvatura: en teoría, puedes ver indefinidamente lejos si nada bloquea.
- Mirando en recto, el horizonte geométrico queda siempre a 90º. Y a medida que subes se mantiene.

$$d_{geom, \ plane} \rightarrow \infty$$

#### Geometría esférica

- Sobre una esfera, el horizonte geométrico se ve afectado por la curvatura de la superficie que depende de la altura del observador y el radio de la esfera.

**Horizonte geométrico para una esfera (derivado del Teorema de Pitágoras):**

$$d = \sqrt{2Rh + h^2}$$

donde:

- $d = distancia \ al \ horizonte \ (km)$
- $R = radio \ de \ la\ esfera$
- $hh = altura \ del \ observador \ (km)$

**Para el modelo esférico (R=6371 km), aproximación (válida si h≪R):**

$$d \approx \sqrt{2Rh} \approx 3.57 \sqrt{h}$$

### Horizonte óptico

El **horizonte óptico** es el límite observable de un medio, resultado de la interacción entre la geometría de la superficie y las propiedades ópticas del medio (transparencia, dispersión, refracción).

1. **Óptica del medio**:
	1. **Transparencia/visibilidad**: cuánta luz se atenúa por dispersión molecular o de partículas.
	2. **Efectos ópticos en el medio**: refracción, reflexión u otros fenómenos que modifican la trayectoria de la luz.
2. **Horizonte geométrico**: determinado únicamente por la geometría de la superficie (plana, esférica u otra).

El horizonte óptico se expresa como un límite mixto:

$$d_{optics} = min \left( d_{geom} \ , d_{vsibility} \right)$$

donde:

- $d_{optics}$: distancia al horizonte óptico
- $d_{geom}$: distancia al horizonte geométrico
- $d_{visibility}$: distancia máxima visible

De forma genérica:

- Si el medio es muy transparente → el límite lo fija la geometría.
- Si el medio es turbio → el límite lo fija la visibilidad.
- En medios refractivos → la refracción puede extender o reducir el alcance.

#### Transparencia: dispersión de Rayleigh

La visibilidad máxima en un medio transparente puede estimarse a partir de la **sección eficaz de dispersión de Rayleigh**, que describe cómo una molécula dispersa la luz.  
De la suma de estas interacciones se obtiene el **coeficiente de extinción** del medio, que fija la **longitud de atenuación** (distancia media a la que la intensidad de la luz se reduce en un factor 1/e).

> En meteorología, este concepto se conecta con la **fórmula de Koschmieder**, que relaciona el coeficiente de extinción con la visibilidad práctica para el ojo humano, tomando como umbral un contraste mínimo detectable (≈2%).

$$\sigma(\lambda) = \frac{8\pi^3}{3N^2\lambda^4}\left( n^2 - 1 \right)^2$$

Donde:

- $\lambda$ = longitud de onda de la luz
- $n$ = índice de refracción del gas
- $N$ = densidad molecular

#### Geometría plana

Si la geometría no limita, el **horizonte óptico** queda fijado únicamente por el medio:

$$d_{optics, \ plane} = d_{visibility}$$
donde $d_{visibility}$ se calcula a partir del coeficiente de extinción del medio (Rayleigh, Mie, aerosoles, absorción).

#### Geometría esférica y criterio de Rayleigh

En el caso particular de una superficie esférica con atmósfera estratificada, la refracción curva la trayectoria de la luz. Se introduce entonces el **criterio de Rayleigh**, usando un radio efectivo:

$$R' = \frac{7}{6}R$$

**Fórmula exacta con refracción:**

$$d \approx \sqrt{2R'h + h^2}$$

**Aproximación simplificada (válido si h≪R):**

$$d \approx \sqrt{2R'h} \approx 3.86 \sqrt{h}$$

---

## Ejemplos Práticos

Primero presentamos una tabla teórica para el horizonte geométrico y óptico para una esfera de R=6371 km, según la altura del observador tenemos lo siguiente:

| Altura del observador | Horizonte geométrico | Horizonte con refracción (óptico) |
| --------------------- | -------------------- | --------------------------------- |
| 2 m (playa)           | 5.0 km               | 5.5 km                            |
| 100 m (acantilado)    | 35.7 km              | 38.6 km                           |
| 450 m (colina)        | 75.6 km              | 81.8 km                           |
| 11.000 m (avión)      | 374 km               | 405 km                            |

Ahora pasemos a una tabla de fotografías reales y su alcance máximo de visión:

| Fotografía (fuente)                                                                                                                                            | Altura observador | Altura objeto | Distancia (observador - objeto) | "Altura oculta" (curvatura terrestre) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ------------- | ------------------------------- | ------------------------------------- |
| [Lancha a nivel del mar](https://i.imgur.com/3QFFDpb.png)                                                                                                      | 0.001 km          | 0.001 Km      | 6.6 Km                          | 0.13 Km                               |
| [Rascacielos Chicago en lago](https://i.imgur.com/vbDEcSq.png)                                                                                                 | 0.5 km            | 0.176 m       | 53.3 Km                         | 0.14 Km                               |
| [El Teide visto desde Lanzarote](https://i.imgur.com/KrUDLNJ.png)                                                                                              | 0.4 km            | 3.72 Km       | 300 Km                          | 3.75 Km                               |
| [Cerro Name a Tupungato](https://www.latercera.com/resizer/itsUMcmq45ZCTH3nfPaYOL2Zl5g=/arc-anglerfish-arc2-prod-copesa/public/C4DYU5G5I5FAVHHDDBYE4QN554.jpg) | 0.82 km           | 6.57 Km       | 346 Km                          | 346 Km                                |
| [Pic de Salòrita en Cataluña desde el Puig d'en Galileu Mallorca](https://i.imgur.com/3M0RfWa.jpeg)                                                            | 1.18 km           | 2.79 Km       | 324 Km                          | 3.18 Km                               |
| [Pirineos a Alpes](https://i.imgur.com/KseVEwt.png)                                                                                                            | 3.2 Km            | 3 Km          | 443 Km                          | 5 Km                                  |
| [Sobrevolando Canadá](https://i.imgur.com/kNLOSy4.png)                                                                                                         | 10.5 Km           | 8.5 Km        | 1600 Km                         | ~30 Km                                |
| [Vuelo Bangkok a Dubai](https://i.imgur.com/ZKHUMmU.png)                                                                                                       | 11.58 Km          | 8.85 Km       | ~1300 Km                        | ~100 Km                               |

Considerando refracción atomsférica (con radio efectivo 16% más grande ~ 7390 km) son posibles los casos de imágenes a larga distancia desde tierra, ahora bien cuando subimos en altura vemos que esto no se cumple.

Por lo que se demuestra que la Tierra no es una superficie esférica. Y que además cumple los mismos efectos en una geometría plana.

## Ejemplo comparativo

Un ejemplo muy típico para medir la distancia máxima al horizonte óptico es la fotografía
del Teide sacada desde Lanzarote (en este caso por [Gustavo Medina](https://www.flickr.com/photos/121856779@N03/)), donde se visualiza el Teide desde la zona de los 2000 metros desde 300 km de distancia.

En el modelo plano ambos horizontes coinciden, sin embargo en el modelo esférico hay que recurrir a índices de refracción altísimos (fuera del rango medible).

![Comparación de horizontes según modelo terrestre](https://i.imgur.com/aI2hoTg.png)


---

## Conclusión

El horizonte demuestra que no hay ocultación de objetos por curvatura sino que se trata de una invisibilidad provocada por la óptica del medio y sus fenómenos. Y por tanto la geometría de la superficie se extiende de forma plana.

Los objetos que se alejan en la superficie no se observan cortados por una curvatura terrestre, lo que se observa es una disminución en la visibilidad de los objetos a medida que estos se alejan más allá del horizonte. La invisibilidad comienza por las zonas bajas donde se producen más fenómenos ópticos (reflexión y refracción) debido al cambio de medio y al mayor gradiente térmico entre las superficies en contacto, lo que genera turbulencias en el aire que afecta a la dispersión de la luz.

![Diagrama de visibilidad de objetos en la distancia](https://i.imgur.com/sQxrzzi.png)
