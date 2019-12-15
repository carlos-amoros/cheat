# MarkDown CheatSheet

[Sitio oficial](https://daringfireball.net/projects/markdown)

[Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Cabeceras

```# Este es un tag h1```

# Este es un tag h1

```## Este es un tag h2```

## Este es un tag h2

```###### Este es un tag h6```

###### Este es un tag h6

```
Este es un tag h1 también
=========================
```

Este es un tag h1 también
=========================

```
Este es un tag h2 también
-------------------------
```

Este es un tag h2 también
-------------------------

Líneas horizontales:
```***```
***
```___```
___

## Énfasis
```*Texto en itálica*```
*Texto en itálica*
```_Texto en itálica_```
_Texto en itálica_
```**Texto en negrita**```
**Texto en negrita**
```__Texto en negrita__```
__Texto en negrita__
```*También **puedes** combinarlos*```
*También **puedes** combinarlos*

## Listas
### Desordenadas

```
* Item 1
* Item 2
	* Item 2a
	* Item 2b
```
* Item 1
* Item 2
	* Item 2a
	* Item 2b

### Ordenadas
```
1. Item 1
2. Item 2
3. Item 3
	* Item 3a
	* Item 3b
```

1. Item 1
2. Item 2
3. Item 3
	* Item 3a
	* Item 3b

## Imágenes

```
![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)
```

![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)

## Links

```
http://github.com - automatic!
[GitHub](http://github.com)
```

http://github.com - automatic!
[GitHub](http://github.com)

## Caracteres de escape

```\*Asteriscos Literales\*```

\*Asteriscos Literales\*

Markdown proporciona caracteres de escape para:

```
\ backslash
` backtick
* asterisk
_ underscore
{} curly braces
[] square brackets
() parentheses
# hash mark
+ plus sign
- minus sign (hyphen)
. dot
! exclamation mark
```

## Bloques de código

Si proporcionamos un identificador 
```
```javascript
function test() {
console.log("look ma’, no spaces");
}```
```

```javascript
function test() {
console.log("look ma’, no spaces");
}
```

[Lenguajes soportados](https://support.codebasehq.com/articles/tips-tricks/syntax-highlighting-in-markdown)