---
{"dg-publish":true,"permalink":"/blog/wikiterra-digital-garden/"}
---

# ¿Qué es WikiTerra Digital Garden?

WikiTerra Digital Garden es una pequeña enciclopedia web del modelo cosmológico terrestre gestionada entera sobre una bóveda o baúl de artículos. Los artículos están escritos en formato [[blog/markdown\|markdown]], un lenguaje de marcado sencillo y fácil de leer.

### WikiTerra Obsidian DG

> Actualemente la web de WikiTerra se publica mediante el plugin Obsidian DG

El plugin [Obsidian Digital Garden](https://github.com/oleeskild/obsidian-digital-garden) del gestor de notas Obsidian permite publicar de manera sencilla las notas markdown en una web estática al estilo *Jardín Digital* o *wiki personal* o web de documentación. 

El plugin utiliza un [tema personalizado de 11Ty](https://github.com/oleeskild/digitalgarden) un generador de webs estáticas (SSG). Luego usa una API para alojar el contenido en [GitHub](https://github.com/) y a despliega la web en una máquina Linux a través de [Vercel](https://vercel.com/) o GitHub Pages.

Para más información visitar [Digital Garden Docs](https://dg-docs.ole.dev/).

### WikiTerra Hextra
WikiTerra Hextra es un tema para el generador de webs estáticas [HUGO](https://gohugo.io/). Su nombre viene de H(UGO) + extra (basado en el tema Nextra). 

La ventaja es que este método permite construir la web en local usando y luego subirla con GItHub. Mientras que Obsidian DG la web se construye en el servidor (Vercel / Netlify / GItHub Pages).

## Editar contenido

> [!NOTE] La opción de editar está desactivada

Método de edición:
1. Hacer una "fork" (bifurcación del repositorio): https://github.com/Curiosity432/wikiterra-vault/fork
2. Realizar los cambios y mejoras correspondientes en los artículos.
3. Solicitar cambios en el repositorio haciendo una Pull Request: https://github.com/Curiosity432/wikiterra-vault/compare

Los artículos están escritos en formato [[blog/markdown\|markdown]] un lenguaje de marcado mu sencillo. Por tanto hay que conocer la sintaxis para poder editar.

### Normas de edición
Hacer una enciclopedia no es una tarea sencilla, en este caso WikiTerra es una Beta en pruebas con el objetivo de ser un enciclopedia accesible para todo el mundo.
1. La información ha de ser objetiva, hay que intentar dejar de lado los aspectos subjetivos y escribir usando evidencias que sean comprobables y empíricas.
2. Escribir con adecuación al tema y sentido.
3. No cometer errores ortográficos, ni gramáticos.
4. Usar un tiempo verbal estándar (presente a ser posible).
5. No escribir opiniones personales, si se trata de una opinión ha de llevar argumentos verificables.
6. Intentar poner referencias de los hechos para verificar la autenticidad.

## Descargar WikiTerra
El conjunto de artículos de WikiTerra se almacena en la bóveda de [WikiTerra](https://github.com/Curiosity432/wikiterra-vault) publicada en GItHub. Para descargarlo solo hay descargar el [repositorio de GitHub](https://github.com/Curiosity432/wikiterra-vault/archive/refs/heads/main.zip) o clonarlo en local `git clone https://github.com/Curiosity432/wikiterra-vault`.

---

## Pros vs contras
- **Ventajas (pros)**
	- El conjunto de notas markdown se encuentra indexado en una bóveda con los gestores de conocimiento (PKM) como Obsidian.md.
	- Permite enlazar artículos de manera sencilla y ver su [[relación\|relación]] en un grafo.
	- El contenido está en local en tu propia máquina.
- **Desventajas (contras)**
	- Requiere conocer la sintaxis markdown.
	- El  lenguaje markdown varía según la aplicación, no tiene un estándar fijo.
	- Los navegadores web solo leen HTML (junto con CSS y JS), para visualizar markdown con formato se necesita un conversor (como hace Obsidian y otros).
