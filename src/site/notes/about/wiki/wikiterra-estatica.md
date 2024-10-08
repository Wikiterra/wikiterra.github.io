---
{"dg-publish":true,"permalink":"/about/wiki/wikiterra-estatica/"}
---


# Wiki estática

> WikiTerra es una wiki estática escrita en formato markdown desde Obsidian.md y desplegada en formato web en GitHub.

Las wikis estáticas son páginas web estáticas que solo interactúan en el lado cliente o front-end donde el formato web (HTML, CSS, JS) es visible por los navegadores web. 

El término "wiki" alude al nombre que recibe una comunidad virtual, cuyas páginas son editadas directamente desde el navegador web, donde los mismos usuarios crean, modifican, corrigen o eliminan contenidos.

Sin embargo al ser estáticas no hay registro de usuarios por ello es necesario almacenar los cambios en un una *plataforma que tenga un control de versiones* , como GitHub, GitLab, Codeberg, etc; con el versión de controles Git.

Algunas wikis estáticas siguen la estrategia de editar archivos markdown alojados en GItHub y luego mediante un proceso automatizado subir el contenido y convertirlo en formato web. Como es el caso de la [wiki de Hyprland](https://wiki.hyprland.org/)

Hacer una web que los usuarios cambien directamente desde GitHub implica usar:
1. Lenguaje de marcado HTML, de estilos CSS y de programación JS, bajo un plantilla. 
2. Lenguaje de marcado simple markdown, plantilla y generador de sitios estáticos

La forma tradicional de hacer wikis es mediante una web dinámica, es decir 
con lado cliente y lado servidor (con base de datos). Lo que facilita la edición online y mantiene un registro de los usuarios. 

La wiki por excelencia más famosa de todas es [Wikipedia](https://wikipedia.org/), la cual sigue esta filosofía desde sus inicios en 2001, usando MediaWiki un gestor de wikis desarrollado en PHP que permite alojar el contenido en una base de datos (mySQL) y un servidor web (apache http).

Las wikis dinámicas están pensadas para proyectos muy grandes pero tienen la desventaja de que su mantenimiento es más caro que una web estática.
