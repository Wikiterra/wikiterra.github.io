---
{"dg-publish":true,"permalink":"/EM/modulacion-EM/","dg-note-properties":{}}
---


# 📡 Modulación EM por constelaciones

## 1. Idea básica

- Una **señal electromagnética** (onda de radio, microondas, luz coherente) transporta información al **modificar sus parámetros físicos**:
    - **Amplitud (A)**
    - **Fase (φ)**
    - **Frecuencia (f)**
    - **Polarización (p)**
- Una **constelación** es un conjunto de “puntos estables” en un espacio matemático (I/Q, o más dimensiones) que representan símbolos discretos.
- Cada punto ↔ símbolo ↔ grupo de bits.

Ejemplo:
- QPSK → 4 puntos → cada punto = 2 bits.
- 64-QAM → 64 puntos → cada punto = 6 bits.

---

## 2. Propiedades físicas

- **Onda portadora EM:**

$$s(t) = A \cos(2\pi f t + \phi)$$
- **Canal real:** introduce **ruido, atenuación, interferencia y desvanecimiento multipath**.
- **Receptor:** debe identificar en qué punto de la constelación cayó la señal recibida, aun con ruido.

---

## 3. Propiedades matemáticas

- La onda se descompone en un **espacio vectorial** de dos ejes:
    - I (In-phase) → componente coseno.
    - Q (Quadrature) → componente seno.

$$s(t) = I \cos(2\pi f t) - Q \sin(2\pi f t)$$

- Una **constelación** es un conjunto discreto de vectores ((I, Q)) en ese plano.
- Cada vector define una combinación única de amplitud y fase.
- Generalización:
    - En lugar de 2 ejes (I/Q), se pueden añadir más dimensiones:
        - Tiempo (multiplexación TDM).
        - Frecuencia (OFDM).
        - Espacio (MIMO).
        - Polarización.
    - Matemáticamente: constelaciones en ($\mathbb{R}^n$) o incluso ($\mathbb{C}^n$).

---

## 4. Aplicación a N-dimensiones

- En comunicaciones modernas, se aprovecha un **hiperespacio de dimensiones**:
    - **I/Q (2D):** fase + amplitud → QAM.
    - **Tiempo (1D extra):** slots → TDM.
    - **Frecuencia (1D extra):** subportadoras → OFDM.
    - **Espacio (n antenas):** MIMO → cada antena añade una dimensión.
    - **Polarización (1D extra):** usar modos ortogonales.
    - **Momento angular orbital (OAM):** añade otra dimensión posible.
- Así, un sistema 5G o de fibra óptica puede estar usando decenas de dimensiones matemáticas simultáneamente.

---

## 5. Intuición geométrica

- Cada símbolo es como una **estrella en una constelación**.
- El transmisor “lanza” la onda hacia esa estrella (ajustando amplitud + fase).
- El receptor recibe algo perturbado por ruido y debe decidir qué estrella estaba más cerca → decodificación.
- En **n-dimensiones**, la constelación se convierte en un **hipercubo o hiperesfera de puntos**.

---

✅ **Resumen final:** 

La modulación por constelación convierte los parámetros continuos de una onda EM en un **espacio geométrico discreto** de símbolos. Matemáticamente son vectores en $(\mathbb{R}^n) (o (\mathbb{C}^n))$, físicamente se implementan ajustando amplitud, fase, frecuencia y otras propiedades de la onda. Aplicado a N dimensiones, cada parámetro físico adicional abre un nuevo eje, y así se construyen los sistemas de comunicación modernos (QAM, OFDM, MIMO, polarización).
