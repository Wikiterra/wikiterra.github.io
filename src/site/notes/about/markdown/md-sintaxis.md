---
{"dg-publish":true,"permalink":"/about/markdown/md-sintaxis/"}
---

# Markdown

Markdown es un lenguaje de marcado simple que permite formatear texto fácilmente en un editor de texto plano, utilizando una sintaxis mínima y fácil de leer.

El renderizado de Markdown se realiza con un motor de Javascript que lo convierte en formato web, HTML para la estructura y CSS para los estilos. Y este formato web se muestra gracias a un navegador web.

> Obsidian es un Google Chrome "disfrazado", ya que utiliza electronJS un framework que combina chromium + nodeJS, para crear crear aplicaciones multiplataforma.

Algunos temas de Obsidian integran estilos especiales para formatos de Markdown, como infoboxes, grids, tarjetas. Un ejemplo es [ITS Theme Documentación](https://publish.obsidian.md/slrvb-docs/ITS+Theme/ITS+Theme) usado para esta wiki.

A continuación se cita la sintaxis básica de Markdown.

## Sintaxis de markdown

### Cabeceras
```
# Cabecera 1
## Cabecera 2
### Cabecera 3
#### Cabecera 4
##### Cabecera 5
###### Cabecera 6
```
# Cabecera 1
## Cabecera 2
### Cabecera 3
#### Cabecera 4
##### Cabecera 5
###### Cabecera 6

### Émfasis
*Este texto irá en cursiva*
Este texto también estará en cursiva

**Este texto estará en negrita
Este texto también estará en negrita.

==Este texto está subrayado==

```
*Este texto estará en cursiva*

Este texto también estará en cursiva

**Este texto estará en negrita

Este texto también estará en negrita.

==Este texto está subrayado==
```

### Listas
```
#### Desordenadas
* Item 1
* Item 2
  * Item 2a
  * Item 2b
#### Ordenadas
1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b
```

#### Desordenadas
* Item 1
* Item 2
  * Item 2a
  * Item 2b
#### Ordenadas
1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

### Casillas de selección
```markdown
- [ ] Uncheckd
- [x] Checked
```

- [ ]  Uncheckd
- [x]  Checked

### Etiquetas / tags
Haz click en la etiqueta de abajo para ver el contenido en otras páginas con la misma etiqueta.
#etiqueta

### Notas de pie de página
```markdown
Este es un ejemplo de cómo agregar una nota al pie de página[^1].

[^1]: Aquí hay información extra en el pie de página
```

Este es un ejemplo de cómo agregar una nota al pie de página[^1].

[^1]: Este es el texto de la nota al pie.

---

### Archivos:

#### Documentos (.md, .html, .excalidraw, .pdf)
```markdown

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



# Formula

> [!summary] Formula
> $\huge
> {\color{cyan} F} = {\color{yellow} m} \cdot {\color{red} a} 
> $
> > Variables:
> > - $\large \color{cyan} F$: the force generated
> > - $\large \color{red} a$: the acceleration the object
> > - $\large \color{yellow} m$: the mass of the object

## Explanation

- Equation of the force, force is equal mass multiplied by acceleration. 
- Basically F=ma 

</div></div>
  - Insertar documento completo


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



## Explanation

- Equation of the force, force is equal mass multiplied by acceleration. 
- Basically F=ma 

</div></div>
  - Insertar cabecera del documento


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Basically F=ma 

</div></div>
 - Insertar frase del documento
```


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



# Formula

> [!summary] Formula
> $\huge
> {\color{cyan} F} = {\color{yellow} m} \cdot {\color{red} a} 
> $
> > Variables:
> > - $\large \color{cyan} F$: the force generated
> > - $\large \color{red} a$: the acceleration the object
> > - $\large \color{yellow} m$: the mass of the object

## Explanation

- Equation of the force, force is equal mass multiplied by acceleration. 
- Basically F=ma 

</div></div>



<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



## Explanation

- Equation of the force, force is equal mass multiplied by acceleration. 
- Basically F=ma 

</div></div>




<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Basically F=ma 

</div></div>



#### Imágenes (.jpg, .png, .svg)

```markdown
 ![GitHub Logo|300](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)

![github-logo.png](/img/user/recursos/img/github-logo.png)
```

![GitHub Logo|300](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)

![github-logo.png](/img/user/recursos/img/github-logo.png)

#### Audios (mp3, .wav, .ogg)

```html
<audio controls>  
  <source src="../recursos/audio/flute.mp3" type="audio/mp3">
  audio not supported
</audio>

![[flute.mp3]]
```

<audio controls>  
  <source src="../recursos/audio/flute.mp3" type="audio/mp3">  
  audio not supported
</audio>

![[flute.mp3]]

#### Videos (.mp4, .webm)
> [!warning] Usando el generador estático HUGO, no es posible instertar videos mediante `![[(video.mp4]]` es necesario usar HTML con la ruta del video.

Si usamos la plantilla de Digital Gardens es recomendable escribirlo en formato markdown, ya que el plugin se encarga de convertir las rutas en formato válido.

```html
<video src="../recursos/video/Bunny.mp4" controls></video>

![[Bunny.mp4]]

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/1AeihtlrAkU?si=ZmtKlUeIU_LYpgSr" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

<video src="../recursos/video/Bunny.mp4" controls>Not working</video>

![[Bunny.mp4]]

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/1AeihtlrAkU?si=ZmtKlUeIU_LYpgSr" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Enlaces o links

```markdown
[[wikiterra\|wikiterra]]
[[wikiterra#Objetivo\|wikiterra#Objetivo]]
[[wikiterra#^intro1\|wikiterra#^intro1]]
[[wikiterra\|WikiTerra - Una wiki de nuestro cosmos]]
[Hugo](https://gohugo.io)
```

[[wikiterra]]
[[wikiterra#Objetivo]]
[[wikiterra#^intro1]]
[[wikiterra|WikiTerra - Una wiki de nuestro cosmos]]
[Hugo](https://gohugo.io)

### Bloques de referencia

```markdown
> Si he visto más lejos es por estar de pie sobre los hombros de Gigantes.
```

> Si he visto más allá es porque me he subido a hombros de gigantes.

### Código en línea

```markdown
El `código` en línea tiene `marcas de retroceso` a su alrededor.
```

El `código` en línea tiene `marcas de retroceso` a su alrededor.

### Bloques de código

\`\`\`go
func main() {
    fmt.Println("Hello World")
}
\`\`\`

```go
func main() {
    fmt.Println("Hello World")
}
```

### Tablas

```markdown
| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |
```

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

---

### Callouts

```
> [!NOTE] Título de la nota
> Información

> [!WARNING] Una advertencia
> Esto es una advertencia

> [!NOTE]+ Abrir por defecto
> Llamada plegable/colapsable

> [!FAQ]- Cerrado por defecto
> Llamada plegable/colapsable

> [!TIP] Llamadas anidadas
> Texto dentro del aviso
> > [!EXAMPLE] Llamada interna
> > Múltiples capas anidadas
> > [!TODO] Texto dentro del aviso
```
> [!NOTE] Título de la nota
> Información

> [!WARNING] Una advertencia
> Esto es una advertencia

> [!NOTE]+ Abrir por defecto
> Llamada plegable/colapsable

> [!FAQ]- Cerrado por defecto
> Llamada plegable/colapsable

> [!TIP] Llamadas anidadas
> Texto dentro del aviso
> > [!EXAMPLE] Llamada interna
> > Múltiples capas anidadas
> > [!TODO] Texto dentro del aviso

---

## Lenguajes de marcado soportados
Obsidian soporta de forma nativa la integración con Canvas (formato JSON), Excalidraw (formato JSON), KaTeX, Mermaid y PlantUML mediante convertidores en JavaScript y plugins especializados. Además con plugins se pueden usar otros como Graphviz, AsciiMath, Timeline, Chess, Dita.

### Canvas
```md
![[mindmap-luz.canvas|mindmap-luz]]
```

![[mindmap-luz.canvas|mindmap-luz]]

### Excalidraw
```md
<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="squaresexcalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.2.8","elements":[{"id":"o-0H8hFcDdTVPZ9s1V7ov","type":"rectangle","x":-258.25,"y":-320.328125,"width":486,"height":394,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a0","roundness":{"type":3},"seed":1842871772,"version":86,"versionNonce":2043067484,"isDeleted":false,"boundElements":null,"updated":1720498941491,"link":null,"locked":false},{"id":"1IL0KFwMeckSYWKEhN8kD","type":"rectangle","x":-175.25,"y":-248.328125,"width":314,"height":258,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a1","roundness":{"type":3},"seed":810564324,"version":17,"versionNonce":549165276,"isDeleted":false,"boundElements":null,"updated":1720498944024,"link":null,"locked":false},{"id":"0-Stq0F3F3dpNkHzqAeL3","type":"rectangle","x":-124.25,"y":-194.328125,"width":222,"height":160,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a2","roundness":{"type":3},"seed":269229404,"version":26,"versionNonce":1674119780,"isDeleted":false,"boundElements":null,"updated":1720498946927,"link":null,"locked":false},{"id":"LYVBM-LafsdwTKoiDyDkN","type":"rectangle","x":-75.25,"y":-157.328125,"width":130,"height":91,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a3","roundness":{"type":3},"seed":444734948,"version":41,"versionNonce":2000892380,"isDeleted":false,"boundElements":null,"updated":1720498953298,"link":null,"locked":false},{"id":"-5JK6iOxuX3q5p-nPVm84","type":"rectangle","x":-49.25,"y":-136.328125,"width":77,"height":52,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a4","roundness":{"type":3},"seed":1144559196,"version":54,"versionNonce":736498524,"isDeleted":false,"boundElements":null,"updated":1720498978635,"link":null,"locked":false},{"id":"7fsjACAoMWmtzrkPoWtPS","type":"rectangle","x":-296.25,"y":-361.328125,"width":562,"height":484,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a5","roundness":{"type":3},"seed":407614820,"version":55,"versionNonce":1483329884,"isDeleted":false,"boundElements":null,"updated":1720498958611,"link":null,"locked":false},{"id":"QpGUFRJW15LetfJ4nrEBO","type":"rectangle","x":-220.25,"y":-272.328125,"width":413,"height":316,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a6","roundness":{"type":3},"seed":375342556,"version":63,"versionNonce":560917348,"isDeleted":false,"boundElements":null,"updated":1720498963340,"link":null,"locked":false},{"id":"U9UqHGxmbWCmvzXTmbo5n","type":"rectangle","x":-333.25,"y":-392.328125,"width":635,"height":551,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a7","roundness":{"type":3},"seed":1254350564,"version":92,"versionNonce":1528551396,"isDeleted":false,"boundElements":null,"updated":1720498975667,"link":null,"locked":false}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"solid","currentItemStrokeWidth":2,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":1582.0782202833302,"scrollY":1091.5134339720746,"zoom":{"value":0.5499999999999996},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true},"objectsSnapModeEnabled":false},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("squaresexcalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
```

<div id="squaresexcalidraw.md2"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.2.8","elements":[{"id":"o-0H8hFcDdTVPZ9s1V7ov","type":"rectangle","x":-258.25,"y":-320.328125,"width":486,"height":394,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a0","roundness":{"type":3},"seed":1842871772,"version":86,"versionNonce":2043067484,"isDeleted":false,"boundElements":null,"updated":1720498941491,"link":null,"locked":false},{"id":"1IL0KFwMeckSYWKEhN8kD","type":"rectangle","x":-175.25,"y":-248.328125,"width":314,"height":258,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a1","roundness":{"type":3},"seed":810564324,"version":17,"versionNonce":549165276,"isDeleted":false,"boundElements":null,"updated":1720498944024,"link":null,"locked":false},{"id":"0-Stq0F3F3dpNkHzqAeL3","type":"rectangle","x":-124.25,"y":-194.328125,"width":222,"height":160,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a2","roundness":{"type":3},"seed":269229404,"version":26,"versionNonce":1674119780,"isDeleted":false,"boundElements":null,"updated":1720498946927,"link":null,"locked":false},{"id":"LYVBM-LafsdwTKoiDyDkN","type":"rectangle","x":-75.25,"y":-157.328125,"width":130,"height":91,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a3","roundness":{"type":3},"seed":444734948,"version":41,"versionNonce":2000892380,"isDeleted":false,"boundElements":null,"updated":1720498953298,"link":null,"locked":false},{"id":"-5JK6iOxuX3q5p-nPVm84","type":"rectangle","x":-49.25,"y":-136.328125,"width":77,"height":52,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a4","roundness":{"type":3},"seed":1144559196,"version":54,"versionNonce":736498524,"isDeleted":false,"boundElements":null,"updated":1720498978635,"link":null,"locked":false},{"id":"7fsjACAoMWmtzrkPoWtPS","type":"rectangle","x":-296.25,"y":-361.328125,"width":562,"height":484,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a5","roundness":{"type":3},"seed":407614820,"version":55,"versionNonce":1483329884,"isDeleted":false,"boundElements":null,"updated":1720498958611,"link":null,"locked":false},{"id":"QpGUFRJW15LetfJ4nrEBO","type":"rectangle","x":-220.25,"y":-272.328125,"width":413,"height":316,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a6","roundness":{"type":3},"seed":375342556,"version":63,"versionNonce":560917348,"isDeleted":false,"boundElements":null,"updated":1720498963340,"link":null,"locked":false},{"id":"U9UqHGxmbWCmvzXTmbo5n","type":"rectangle","x":-333.25,"y":-392.328125,"width":635,"height":551,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a7","roundness":{"type":3},"seed":1254350564,"version":92,"versionNonce":1528551396,"isDeleted":false,"boundElements":null,"updated":1720498975667,"link":null,"locked":false}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"solid","currentItemStrokeWidth":2,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":1582.0782202833302,"scrollY":1091.5134339720746,"zoom":{"value":0.5499999999999996},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true},"objectsSnapModeEnabled":false},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("squaresexcalidraw.md2");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

### KaTEX (formulas matemáticas)
```latex
$ E = mc^2 $
```

$$ E = mc^2 $$

### Mermaid (diagramas)
```txt
``mermaid
	graph LR;
		A--> B
``

``mermaid
	gantt
		title Diagrama de Gannt
		dateFormat YYYY-MM-DD
		section Section
		A task           :a1, 2014.01-01, 30d
		Another task     :after a1, 20d
		section Another
		Task in sec      :2014.01-12, 12d
		another task     : 24d
``
```

```mermaid
	graph LR;
		A--> B
```

```mermaid
	gantt
		title A Gannt Diagram
		dateFormat YYYY-MM-DD
		section Section
		A task           :a1, 2014.01-01, 30d
		Another task     :after a1, 20d
		section Another
		Task in sec      :2014.01-12, 12d
		another task     : 24d
```
---

### PlantUML  (diagramas UML)
> To render PlantUML in Obsidian.md you need to install the plugin PlantUML.
```plantuml
@startuml
Bob -> Alice : hello
@enduml
```


## References
- [Markdown Syntax](https://www.markdownguide.org/basic-syntax/)
- [Hugo Markdown](https://gohugo.io/content-management/formats/#markdown)
