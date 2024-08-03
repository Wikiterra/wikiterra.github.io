---
{"dg-publish":true,"permalink":"/about/wikiterra-dev/"}
---


# ¿Qué es WikiTerra ?
WikiTerra es una pequeña enciclopedia web del modelo cosmológico terrestre gestionada entera sobre una bóveda o baúl de artículos desde el gestor de notas [Obsidian.md](https://obsidian.md/).

## Web estática
Wikiterra es una [[about/wikiterra-estatica\|web estática]], lo que significa que no hay lado servidor todo se ejecuta en lado cliente (en el navegador web, "chrome", "firefox", etc). Los artículos están escritos en formato [[about/markdown/markdown-sintaxis\|markdown-sintaxis]], un lenguaje de marcado sencillo y fácil de leer, que se convierte al formato web (HTML, CSS, JS) usando un [Generador de sitios estáticos (SSG)](https://en.wikipedia.org/wiki/Static_site_generator).

Hay cientos de generadores estáticos en [JamStack](https://jamstack.org/generators/) clasifican 355, algunos de los más importantes son: Next.js, HUGO, Docusaurus, Nuxt, Astro, Jekyll, GitBook, Docsify, VuePress, MkDocs, Eleventy. 

Cada SSG uno tiene su propio lenguaje de programación con su propio estilo de plantillas para ser transformados a formato web. Pero al final lo que importa es la plantilla que uses y que el framework o SSG sea intuitivo, tenga una gran comunidad y se mantenga en desarrollo.

En el caso de Wikiterra, la web ha sido testeada en local con diferentes SSG como HUGO con el tema [Hextra](https://imfing.github.io/hextra/), Astro con el tema [Starlight](https://starlight.astro.build/), o Tiddlywiki con el tema [Featherwiki](https://feather.wiki/) que permite tener un web entera sobre un único HTML.

Sin embargo la opción que se ha mantenido ha sido la plantilla web de [Digital Garden de Ole Eskild](https://github.com/oleeskild/digitalgarden) que usa 11Ty como generador, por su bonito diseño y su fácil uso através de Obsidian.

## Creación de la web con Digital Garden
> Wikiterra se basa la plantilla web [Digital Garden de Ole Eskild](https://github.com/oleeskild/digitalgarden) que utiliza 11Ty como generador de sitios estáticos (SSG)

Para configurar la web es necesario realizar los siguientes pasos:
1. Primero tenemos que tener instalado [obsidian](https://obsidian.md/download) y nuestro vault de notas abierto.
2. Tener una cuenta en una plataforma de git (GitHub, GitLab, Codeberg, etc).
3. Instalar el plugin para Obsidian [Digital Garden Publication Center](https://github.com/oleeskild/obsidian-digital-garden), y configurar el nombre de usuario, repositorio y token de la plataforma de git.
4. Clonar la [plantilla de Digital Garden](https://github.com/oleeskild/digitalgarden) para **hospedar la plantilla con el contenido** y configurar el proveedor de alojamiento de sitios estáticos para **desplegar  la webgenerada **, puede ser: [Cloudflare Pages](https://pages.cloudflare.com/), [GitHub Pages](https://pages.github.com/), [GitLab Pages](https://docs.gitlab.com/ee/user/project/pages/), [Netlify](https://www.netlify.com/), [Vercel](https://vercel.com/). 
5. Y configurar el proceso de despliegue, para GitHub Pages con [GitHub actions](https://docs.github.com/en/actions) en `.github/workflows/build.yml`, para Vercel en `vercel.json`, para Netlify en `netlify.toml`, etc.

En el caso de WikiTerra es lo siguiente:
1. Se escribe en formato markdown en obsidian.md.
2. Se publica el contenido con el plugin de Obsidian [Digital Garden Publication Center](https://github.com/oleeskild/obsidian-digital-garden) que sincroniza los archivos con el la plantilla web [WikiTerra/wikiterra.github.io en GitHub](https://github.com/Wikiterra/wikiterra.github.io).
3. Se despliega la web usando "flujos de trabajo de GitHub Actions" configurado en [`.github/workflows/build.yml`](https://github.com/Wikiterra/wikiterra.github.io/blob/main/.github/workflows/build.yml) que hacen uso de 11Ty programado en la plantilla.
```bash
npm install # instalar paquetes de node.js
npm run build # construir web
npm run watch:eleventy # visualizar web, alternativas "npm run start" o "npx @11ty/eleventy --serve"
```

Para más información visitar la documentación oficial, [Digital Garden Docs](https://dg-docs.ole.dev/).

### Pros vs contras

- **Ventajas (pros)**
	- El conjunto de notas markdown se encuentra indexado en una bóveda con los gestores de conocimiento (PKM) como Obsidian.md.
	- Permite enlazar artículos de manera sencilla y ver su relación en un grafo.
	- El contenido está en local en tu propia máquina.

- **Desventajas (contras)**
	- Requiere conocer la sintaxis markdown.
	- El lenguaje markdown varía según la aplicación, no tiene un estándar fijo.
	- Los navegadores web solo leen HTML (junto con CSS y JS), para visualizar markdown con formato se necesita un conversor (como hace obsidian, vscode y otros).

## ¿Cómo editar?

Para editar la wiki consulta la sección de [[about/wikiterra-edicion\|wikiterra-edicion]].
