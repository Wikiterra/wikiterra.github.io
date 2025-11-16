---
{"dg-publish":true,"permalink":"/wikiterra/about/"}
---


# ¿Qué es WikiTerra ?

WikiTerra es una pequeña enciclopedia web del modelo cosmológico terrestre gestionada entera sobre una bóveda o baúl de artículos desde el gestor de notas [Obsidian.md](https://obsidian.md/).

## Web estática

Wikiterra es una web estática, lo que significa que no hay lado servidor todo se ejecuta en lado cliente (en el navegador web, "chrome", "firefox", etc). Los artículos están escritos en formato [[zen/obsidian-md-syntax/markdown\|markdown]], un lenguaje de marcado sencillo y fácil de leer, que mediante un [generador de sitios estáticos (SSG)](https://en.wikipedia.org/wiki/Static_site_generator) se convierte al formato web (HTML, CSS, JS) usando un 

Hay cientos de generadores estáticos en [JamStack](https://jamstack.org/generators/) clasifican 355, entre los más importantes están: Next.js, HUGO, Docusaurus, Nuxt, Astro, Jekyll, GitBook, Docsify, VuePress, MkDocs, Eleventy. Cada SSG tiene su propio lenguaje de programación con su propio estilo de plantillas para ser transformados a formato web. Pero al final lo que importa es la plantilla que uses y que sea intuitivo, tenga una gran comunidad y se mantenga en desarrollo.

En el caso de Wikiterra, la web ha sido testeada en local con diferentes SSG como HUGO con el tema [Hextra](https://imfing.github.io/hextra/), Astro con el tema [Starlight](https://starlight.astro.build/), o Tiddlywiki con el tema [Featherwiki](https://feather.wiki/) que permite tener un web entera sobre un único HTML.

Sin embargo la opción que se ha mantenido ha sido la plantilla web de [Digital Garden de Ole Eskild](https://github.com/oleeskild/digitalgarden) que usa 11Ty como generador con el tema [digitalgarden](https://github.com/oleeskild/digitalgarden), por su bonito diseño y su fácil uso a través de Obsidian.

## Creación de la web con Digital Garden

> Wikiterra se basa la plantilla web [Digital Garden de Ole Eskild](https://github.com/oleeskild/digitalgarden) que utiliza 11Ty como generador de sitios estáticos (SSG)

Para configurar la web es necesario realizar los siguientes pasos:

1. Instalar [obsidian](https://obsidian.md/download) y abrir el vault de notas [wikiterra-vault](https://github.com/Wikiterra/wikiterra-vault).
2. Tener una cuenta en GitHub.
3. Hacer un "Pull Request" a [wikiterra-vault](https://github.com/Wikiterra/wikiterra-vault).

### Pros vs contras

- **Ventajas (pros)**
	- El conjunto de notas está escrito en texto plano.
	- Cada nota se enlaza de forma sencilla y se puede ver su relación en un grafo.
	- Se puede descargar fácilmente y visualizar en local.
	- La web es estática, todo carga en lado cliente de forma rápida.

- **Desventajas (contras)**
	- Requiere conocer la sintaxis markdown.
	- El lenguaje markdown no tiene un estándar fijo y varían algunos detalles según la aplicación.
	- Los navegadores web solo leen HTML, CSS y JS, para visualizar markdown en formato web se precisa de un conversor.
