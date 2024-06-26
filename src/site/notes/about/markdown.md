---
{"dg-publish":true,"permalink":"/about/markdown/"}
---

# Markdown

Markdown es un lenguaje de marcado simple que permite formatear texto fácilmente en un editor de texto plano, utilizando una sintaxis mínima y fácil de leer.

La renderización de Markdown se realiza convirtiéndolo a HTML, que luego se procesa normalmente en un navegador web. Además, se incluyen CSS predefinidos para dar estilo al texto.

Algunos temas de Obsidian integran estilos especiales para formatos de Markdown, como infoboxes, grids, tarjetas. Un ejemplo es [ITS Theme Documentación](https://publish.obsidian.md/slrvb-docs/ITS+Theme/ITS+Theme) usado para esta wiki.

A continuación se cita la sintaxis básica de Markdown.

## Cabeceras

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

``text
*Este texto irá en cursiva*
Este texto también estará en cursiva

**Este texto estará en negrita
Este texto también estará en negrita.

Puedes combinarlos
```
*Este texto estará en cursiva*

Este texto también estará en cursiva

**Este texto estará en negrita

Este texto también estará en negrita.

Puedes combinarlos
```

### Listas

#### Desordenadas
* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

#### Ordenadas
1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

### Imágenes

```markdown
 ![GitHub Logo|300](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)
```

![GitHub Logo|300](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)

### Videos
> [!warning] Insertar videos mediante !\[[(video.mp4]\]  no es posible

Para insertar video ha de ser con HTML o con el formato en HUGO.

```html
<video src="../resources/video/como-editar-wiki-github.mp4" controls></video>
```


### Links

```markdown
[Hugo](https://gohugo.io)
```

[Hugo](https://gohugo.io)

### Blockquotes

```markdown
> Si he visto más lejos es por estar de pie sobre los hombros de Gigantes.
```

> Si he visto más allá es porque me he subido a hombros de gigantes.

### Inline Code

```markdown
El `código` en línea tiene `marcas de retroceso` a su alrededor.
```

El `código` en línea tiene `marcas de retroceso` a su alrededor.

### Bloques de código

#### Resaltado de sintaxis

````markdown
```go
func main() {
    fmt.Println("Hello World")
}
```
````

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

## References
- [Markdown Syntax](https://www.markdownguide.org/basic-syntax/)
- [Hugo Markdown](https://gohugo.io/content-management/formats/#markdown)
