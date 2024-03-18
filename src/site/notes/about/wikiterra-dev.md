---
{"dg-publish":true,"permalink":"/about/wikiterra-dev/"}
---


# ¿Qué es WikiTerra ?

WikiTerra es una pequeña enciclopedia web del modelo cosmológico terrestre gestionada entera sobre una bóveda o baúl de artículos.

## ¿Cómo se desarrolla?

Wikiterra es una [[about/wiki-estatica\|wiki-estatica]], lo que significa que no hay lado servidor todo se ejecuta en lado cliente (en el navegador). Los artículos están escritos en formato [[blog/markdown\|markdown]], un lenguaje de marcado sencillo y fácil de leer, que se convierte al formato web (HTML, CSS, JS) usando un [Generador de sitios estáticos (SSG)](https://en.wikipedia.org/wiki/Static_site_generator).

Hay cientos de generadores estáticos en [JamStack](https://jamstack.org/generators/) clasifican 355 SSGs, algunos de los más importantes son: Next.js, HUGO, Docusaurus, Nuxt, Astro, Jekyll, GitBook, Docsify, VuePress, MkDocs, Eleventy. 

Cada SSG uno tiene su propio lenguaje de programación con su propio estilo de plantillas para ser transformados a formato web. Pero al final lo que importa es la plantilla que uses y que el framework o SSG sea intuitivo, tenga una gran comunidad y se mantenga en desarrollo.

En el caso de Wikiterra, la web ha sido testeada en local con diferentes SSG como HUGO con el tema [Hextra](https://imfing.github.io/hextra/), Astro con el tema [Starlight](https://starlight.astro.build/), o Tiddlywiki con el tema [Featherwiki](https://feather.wiki/) que permite tener un web entera sobre un único HTML.

Sin embargo la opción que se ha mantenido ha sido la plantilla web de [Digital Garden de Ole Eskild](https://github.com/oleeskild/digitalgarden) que usa 11Ty como generador, por su bonito diseño y su fácil uso.

### Plantilla Digital Garden

> Wikiterra usa la plantilla web [Digital Garden de Ole Eskild](https://github.com/oleeskild/digitalgarden) que utiliza el SSG 11Ty

Esta plantilla está diseñada para ser usada junto el plugin [Obsidian Digital Garden](https://github.com/oleeskild/obsidian-digital-garden),  siguiendo estos pasos:
1. Clonar la plantilla de Digital Garden en GitHub (como control de versiones) y hospedarlo en Vercel (para el despliegue web), cosa automatizable pulsando el siguiente link https://vercel.com/new/clone?repository-url=https://github.com/oleeskild/digitalgarden
2. Obtener un token para sincronizar los cambios en local al repositorio remoto de GitHub
3. Configurar lo básico en el plugin de Obsidian: {username}, {repository name }, {token}.

Sin embargo este método hacía que la web no fuese accesible localmente, y que todos los cambios se enviasen a Vercel, sin saber que ocurría por detrás. Por lo que ahora la web usa GitHub como control de versiones y como sitio de despliegue.

Y hay dos formas de desplegar el contenido en GitHub:
1. Usar [GitHub actions](https://docs.github.com/en/actions) para automatizar el despliegue en una máquina virtual Ubuntu, usando el siguiente [workflow de ejemplo](https://github.com/oleeskild/obsidian-digital-garden/discussions/389#discussioncomment-7437123) y configurando un token como secreto en el repositorio para que se hagan los cambios automáticamente.
2. Construir la web en local con npm (node.js package manager) y desplegarla en GitHub en el directorio `docs/`.

```bash
npm install # instalación de paquetes
npm run build # construcción de la web en el directorio por defecto como "dist/"
npm run watch:eleventy # visualizar la web en http://localhost:8080 # npm run start or npx @11ty/eleventy --serve
```

Para más información visitar la documentación oficial, [Digital Garden Docs](https://dg-docs.ole.dev/).

### Pros vs contras

- **Ventajas (pros)**
	- El conjunto de notas markdown se encuentra indexado en una bóveda con los gestores de conocimiento (PKM) como Obsidian.md.
	- Permite enlazar artículos de manera sencilla y ver su [[relación\|relación]] en un grafo.
	- El contenido está en local en tu propia máquina.
- **Desventajas (contras)**
	- Requiere conocer la sintaxis markdown.
	- El lenguaje markdown varía según la aplicación, no tiene un estándar fijo.
	- Los navegadores web solo leen HTML (junto con CSS y JS), para visualizar markdown con formato se necesita un conversor (como hace obsidian, vscode y otros).

## ¿Cómo editar?

Para editar la wiki consulta la sección de [[about/editar-contenido\|editar-contenido]].
