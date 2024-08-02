---
{"dg-publish":true,"permalink":"/about/digitalgarden-template/"}
---


# Template de DigitalGarden

La plantilla o template original para generar la web estática desde Obsidian es [digitalgarden](https://github.com/oleeskild/digitalgarden) usando 11Ty como generador sitios estáticos (SSG).

> Los archivos markdown escritos en Obsidian (`archivo.md`) se añaden dentro de `src/site/notes/`. 
> Mientras las imágenes van en `src/site/img/user/ruta-absoluta-imagen`, aunque es recomendable no sobrecargar la web con imágenes para mejorar la optimización y rendimiento.

Árbol de directorios y archivos de digitalgarden:
```sh
# Comando para generar tree:
# tree -aL 3 --prune -I 'node_modules' 
.
├── dist
│   ├── 404
│   │   └── index.html
│   ├── apple-touch-icon.png
│   ├── favicon.ico
│   ├── favicon.svg
│   ├── feed.xml
│   ├── graph.json
│   ├── img
│   │   ├── default-note-icon.svg
│   │   ├── outgoing.svg
│   │   ├── tree-1.svg
│   │   ├── tree-2.svg
│   │   └── tree-3.svg
│   ├── index.html
│   ├── manifest.webmanifest
│   ├── searchIndex.json
│   ├── sitemap.xml
│   └── styles
│       ├── custom-style.css
│       ├── custom-style.css.map
│       ├── digital-garden-base.css
│       ├── digital-garden-base.css.map
│       ├── obsidian-base.css
│       ├── obsidian-base.css.map
│       ├── style.css
│       ├── style.css.map
│       └── _theme.eae2f3b6.css
├── .eleventyignore
├── .eleventy.js
├── .env
├── .github
│   ├── dependabot.yml
│   └── workflows
│       └── build.yml
├── .gitignore
├── netlify.toml
├── package.json
├── package-lock.json
├── plugin-info.json
├── README.md
├── src
│   ├── helpers
│   │   ├── constants.js
│   │   ├── filetreeUtils.js
│   │   ├── linkUtils.js
│   │   ├── userSetup.js
│   │   ├── userUtils.js
│   │   └── utils.js
│   └── site
│       ├── 404.njk  
│       ├── _data  
│       │   ├── dynamics.js  
│       │   ├── eleventyComputed.js  
│       │   └── meta.js  
│       ├── favicon.svg  
│       ├── feed.njk  
│       ├── get-theme.js  
│       ├── graph.njk  
│       ├── img  
│       │   ├── default-note-icon.svg  
│       │   ├── outgoing.svg  
│       │   ├── tree-1.svg  
│       │   ├── tree-2.svg  
│       │   └── tree-3.svg  
│       ├── _includes  
│       │   ├── components  
│       │   │   ├── calloutScript.njk  
│       │   │   ├── filetreeNavbar.njk  
│       │   │   ├── filetree.njk  
│       │   │   ├── graphScript.njk  
│       │   │   ├── linkPreview.njk  
│       │   │   ├── lucideIcons.njk  
│       │   │   ├── navbar.njk  
│       │   │   ├── notegrowthhistory.njk  
│       │   │   ├── pageheader.njk  
│       │   │   ├── references.njk  
│       │   │   ├── searchButton.njk  
│       │   │   ├── searchContainer.njk  
│       │   │   ├── searchScript.njk  
│       │   │   ├── sidebar.njk  
│       │   │   └── timestamps.njk  
│       │   └── layouts  
│       │       ├── index.njk  
│       │       └── note.njk  
│       ├── notes  
│       │   ├── notes.11tydata.js  
│       │   └── notes.json  
│       ├── search-index.njk  
│       ├── sitemap.njk  
│       └── styles  
│          ├── custom-style.scss  
│          ├── digital-garden-base.scss  
│          ├── obsidian-base.scss  
│          ├── style.scss  
│          └── _theme.eae2f3b6.css
├── tree.md
└── vercel.json
```

---

## Modificaciones del template de DigitalGarden
Se ha añadido un pie de página en `user/notes/footer/edit-note.njk`. Para crear un botón de editar nota que redirige a GitHub creando una copia o "fork" del original. Así los usuarios podrían editar contenido y mandar los cambios, haciendo click directamente sobre el botón.

> [!note] Acutalmente está comentado para que no haga efecto en la web.

```html
<!--
<div class="content">
    <button id="editButton" style="margin-top: 10px;">Editar en GitHub</button>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    var path = window.location.pathname;
    var editButton = document.getElementById('editButton');
    editButton.setAttribute('onclick', "window.location.href='https://www.github.com/user/wiki-vault/blob/main/" + path + "'");
});
</script>
-->
```

Más info para añadir componentes [aquí](https://dg-docs.ole.dev/advanced/adding-custom-components/)

---

