---
{"dg-publish":true,"permalink":"/blog/wiki-estatica/"}
---

# Wiki estática

## Definición
Las wikis estáticas son páginas web estáticas, es decir, que solo interactúan en el lado cliente o front-end donde el código HTML, CSS y JS es visible por los navegadores web. Al tratarse de wikis significa que son webs con artículos editables por los usuarios que almacenan los cambios. Sin embargo al ser estáticas no hay registro de usuarios por ello es necesario almacenar los cambios de usuarios en otro lugar, par ello se usa una *plataforma que tenga un control de versiones como las basadas en Git*, como GitHub, GitLab, Codeberg, etc.

## Ejemplos
- [Wiki nikiv](https://wiki.nikiv.dev/) en [nikitavoloboev/knowledge · GitHub](https://github.com/nikitavoloboev/knowledge)
- [DG Docs](https://dg-docs.ole.dev/)
- [100rabbit](https://100rabbit.co/)

## Problema de las wikis estáticas
El problema de las wikis es que necestan un backend, una base de datos para registrar a los usuarios y los cambios. 

Por tanto para hacer una wiki estática solo con frontend hay que llevar el backend a una plataforma externa a la web como puede ser un repositorio de GitHub.

Algunas wikis estáticas siguen la estrategia de editar archivos markdown alojados en GItHub y luego mediante un proceso automatizado subir el contenido y convertirlo en formato web. Como es el caso de la [wiki de Hyprland](https://wiki.hyprland.org/)

Hacer una web que los usuarios cambien directamente desde GitHub implica usar:
- HTML, CSS y JS y que respeten el tema y no lo modifiquen. 
- Lenguaje de marcado más sencillo como markdown y usar un generador estático de webs como HUGO o 11ty. Y cada cambio en los artículos markdown se tendría que convertir a web HTML de manera automática con el generador correspondiente.


## Solución: Wikis dinámicas
[Wikipedia](https://wikipedia.org/) es una web dinámica tiene frontend y backend (base de datos en un servidor y conexión con servidor). Lo que facilita la edición online y mantiene un registro de los usuarios. Y usa el gestor de wikis MediaWiki desarrollado en PHP que permite editar de manera sencilla las webs.

El problema de las wikis dinámicas es que necesitan un servidor dedicado y eso vale dinero y consume muchos recursos. Mientras las wikis estáticas se pueden desplegar de manera gratuita. Además el contenido se edita online o en la nube en lugar de en local.
