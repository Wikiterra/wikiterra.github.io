---
{"dg-publish":true,"permalink":"/EM/historia-transmision-info/"}
---


# 📡 De la Onda a la Información: Historia de la Transmisión Electromagnética y su Modulación

> “El universo vibra; nosotros aprendimos a escribir con sus ondas.”  
> — Inspirado en Claude Shannon (1948)

---

## 1. Introducción: cuando el ruido se convirtió en mensaje

Todo comienza con un problema ancestral: **¿cómo enviar información a distancia sin perderla en el ruido del mundo?**

A lo largo del siglo XX, los ingenieros y físicos aprendieron que las ondas electromagnéticas —esas oscilaciones invisibles de campos eléctricos y magnéticos— podían llevar voz, música o datos digitales, siempre que supiéramos cómo **modularlas** y **descifrarlas**.

Claude Shannon, en 1948, enunció la teoría fundamental de la información. Su idea fue casi musical:

> “Toda señal, por compleja que parezca, puede descomponerse en una suma de ondas simples.”

De esa intuición nació el **lenguaje universal de la comunicación moderna**.

---

## 2. Primeras notas: las ondas analógicas (1850–1950)

Las primeras transmisiones usaban variaciones **continuas** de una onda portadora.  
La señal era análoga (de ahí “analógica”) a la información original.

|Época|Sistema|Tipo de Modulación|Qué varía|Aplicación|Análogo musical|
|---|---|---|---|---|---|
|1840s|**Código Morse (AM binaria)**|Encendido/Apagado|Presencia de señal|Telegrafía|Silencio ↔ Nota|
|1900|**AM (Amplitude Modulation)**|Amplitud|Volumen de la onda|Radio voz/música|Volumen dinámico|
|1930|**FM (Frequency Modulation)**|Frecuencia|Tono de la onda|Radio de alta fidelidad|Afinación|
|1940|**PM (Phase Modulation)**|Fase|Desfase angular|Radar, comunicaciones|Ritmo o síncopa|

En AM, una canción o voz modulaba la altura de la onda portadora.  
En FM, la frecuencia variaba como las notas en una escala musical.  
Cada tipo de modulación era una manera distinta de “cantar con la electricidad”.

---

## 3. Shannon y el nacimiento del bit (1948–1960)

Shannon introdujo el concepto de **bit** —la unidad mínima de información— y formalizó la capacidad de un canal:

$$C = B \log_2(1 + S/N)$$

donde:

- **C**: capacidad máxima (bits por segundo) 
- **B**: ancho de banda (Hz)
- **S/N**: relación señal-ruido

La ecuación expresa un límite natural:

> Cuanto más limpia la señal (mayor S/N), más bits puede transportar.

La música del universo tenía ahora **una partitura matemática**.

---

## 4. La revolución digital (1960–1990)

Con los transistores y la computación, la información dejó de ser continua.  
Ahora todo se representaba en **ceros y unos**. Las ondas analógicas se **digitalizaron** mediante muestreo y cuantización.

| Paso | Nombre           | Descripción                               | Ejemplo                |
| ---- | ---------------- | ----------------------------------------- | ---------------------- |
| 1    | **Muestreo**     | Captura de valores discretos en el tiempo | CD de audio a 44.1 kHz |
| 2    | **Cuantización** | Asigna un número binario a cada valor     | 16 bits por muestra    |
| 3    | **Codificación** | Agrupa bits para transmitir               | Paquetes TCP/IP, MP3   |

Así nació la transmisión digital, donde una señal ya no era una curva continua, sino **una secuencia de símbolos discretos**.

---

## 5. Modulación digital: las constelaciones del espacio de la información

A diferencia de la radio analógica, las señales digitales se codifican en **símbolos**: combinaciones únicas de **amplitud** y **fase** representadas como puntos en un plano (constelación I/Q).

|Modulación|Bits/símbolo|Puntos|Dimensiones|
|---|---|---|---|
|**BPSK**|1|2|1D|
|**QPSK**|2|4|2D|
|**16-QAM**|4|16|2D|
|**64-QAM**|6|64|2D|
|**1024-QAM**|10|1024|2D|

En **QAM**, cada punto es una **coordenada compleja** (fase y amplitud) que define el estado instantáneo de la onda portadora.  
Esta constelación funciona como un **pentagrama geométrico**, donde cada símbolo ocupa una posición precisa en el tiempo, igual que una nota en una partitura.

---

### Extensión a espacios multidimensionales

La constelación 2D es solo una proyección de un fenómeno más amplio.  
Al incorporar nuevas variables físicas —**polarización, frecuencia, tiempo o espacio**—, la modulación se expande a un **espacio N-dimensional**, donde cada eje representa un grado de libertad de la onda electromagnética.

|Dimensión|Variable modulada|Significado físico|
|---|---|---|
|1D|Amplitud (ASK)|Intensidad de la señal|
|2D|Fase y amplitud (QAM)|Estado complejo del vector|
|3D|Polarización|Orientación del campo eléctrico|
|4D|Frecuencia o tiempo|Desplazamiento espectral o temporal|
|5D+|Espacio / MIMO|Canales simultáneos o espaciales|

Cada símbolo puede así representarse como un **punto en una constelación hiperesférica**, donde las distancias miden diferencias combinadas de fase, energía y orientación.  
La modulación se convierte en una **coreografía geométrica** dentro del **espacio de la información**, un hiperespacio donde cada dimensión abre una nueva vía para codificar significado.

---

## 6. Del plano al espectro: OFDM y el paralelismo armónico

A finales del siglo XX, los ingenieros descubrieron que podían **usar muchas portadoras a la vez**, cada una modulada de forma independiente.  
Así nació **OFDM (Orthogonal Frequency Division Multiplexing)** —la base de Wi-Fi, LTE y 5G.

> Es como un coro donde cada voz canta una frecuencia distinta, pero todas están perfectamente afinadas para no solaparse.

|Tecnología|Frecuencia central|Ancho de canal|Modulación|Bits/símbolo aprox.|
|---|---|---|---|---|
|Wi-Fi 2.4 GHz|2.412–2.472 GHz|20–40 MHz|64–1024-QAM|~10⁶|
|LTE 4G|800 MHz – 2.6 GHz|1.4–20 MHz|64-QAM|~150 Mbps|
|5G NR|3.5–28 GHz|50–100 MHz|256–1024-QAM|>1 Gbps|
|Fibra óptica DWDM|193 THz (1550 nm)|50 GHz por canal|Coherent-QAM|>1 Tbps|

---

## 7. En la frontera óptica (2000–2025)

En fibra óptica, las ondas electromagnéticas viajan como luz infrarroja.  
Cada canal puede usar **polarización, fase y amplitud** —equivalente a una modulación de alta dimensión (4D o más).  
Hoy se alcanzan **más de 1 terabit por segundo por hilo**, y los sistemas espaciales de múltiples modos experimentan con hasta **20 dimensiones ópticas**.

---

## 8. Epílogo: el universo como orquesta

Desde las primeras chispas de Morse hasta los pulsos coherentes del láser, la humanidad aprendió a **escribir con el electromagnetismo**.  
Cada señal, cada bit, es una nota tocada sobre el pentagrama del tiempo.  
La teoría de Shannon nos dio las reglas armónicas; la ingeniería las convirtió en melodía digital.

> “Donde antes oíamos ruido, ahora escuchamos significado.”

---

## 9. Tabla resumen: evolución histórica de la modulación EM

|Etapa|Tipo|Portadora|Dimensiones|Representación|Capacidad|
|---|---|---|---|---|---|
|Morse|Analógica binaria|Corriente eléctrica|1D|Pulsos / silencios|< 1 bps|
|AM/FM|Analógica continua|Radio|1D|Altura o tono de onda|~100 kbps|
|PSK/QAM|Digital|Microondas / radio|2D|Constelación plana|1–100 Mbps|
|OFDM|Digital multicarrier|Radio / Wi-Fi / LTE|n×2D|Múltiples constelaciones|1 Gbps|
|Coherent Optical QAM|Digital cuántico-luz|Infrarrojo|4D–20D|Constelaciones hiperesféricas|>1 Tbps|

---

## 10. Reflexión final

Toda tecnología de comunicación —desde el telégrafo hasta el 5G cuántico— es un esfuerzo por **modular el universo**, por transformar vibraciones en sentido.  
El osciloscopio, el espectro y la constelación no son más que distintos modos de leer esa partitura invisible.

> La modulación electromagnética es, en el fondo, una música escrita en el espacio-tiempo. 
> Y cada bit, una nota del lenguaje universal de la energía.
