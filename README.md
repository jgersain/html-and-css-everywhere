# Responsive BulmaCSS

Create a responsive blog using bulma css

#### For debug css use

- Comment or uncomment `debug.css` file
- Alternatively use [X-ray](https://tachyons.io/xray/) plugin for Chrome

## Buenas practicas HTML

### Añadir la estructura básica necesaria dentro de head

```html
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="description" content="Blog sobre perros" />
    <meta name="robots" content="index,follow" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  </head>
</html>
```

- Utilizar la etiqueta figure cuando se trabaje con imágenes, si se necesita una descripción usar figcaption

### Formularios

Select con buscador

```html
<input list="cursos" />
<datalist id="cursos">
  <option value="JavaScript"></option>
  <option value="HTML5"></option>
</datalist>
```

### Uso de imagenes (loseless vs lossy) sin perdida y con perdida

- JPG `lossy` (fotografias e imágenes fijas)
- PNG 8 `lossless` (iconos, con transparencia y sin animación)
- GIF `lossless` (animaciones simples y gráficos con colores planos)
- Vectores `lossless` (imágenes fijas, pantallas de alta resolución, ideal para gráficos y logotipos en la web)

NOTA: El tamaño promedio de una imágen debe de ser de 70kb, para ello hay herramientas que las optimizan:

- Tiny PNG (Mejora el tamaño de las imágenes)
- Verexif (Retira metadatos de las imágenes)

### CSS

- Utilizar el patrón BEM
- Utilizar CSS orientado a objetos
- No utilizar IDs para poner estilos
- Evitar utilizar `!important`
- Evitar estilos enbebidos
- Setear los estilos del navegador
- Conocer el tema de las especificidad de los selectores
  - `!important`
  - Código embebido
  - Ids
  - Clases
  - Tags

> NOTA: Los selectores combinados tienen mayor peso, por ejemplo dos clases en un mismo elemento sobreescriben a una clase con una etiqueta html

### CSS Combinadores

`Hermano asdyacente o cercano:` Todas las etiquetas de parrafo cerca de una etiqueta h2 (adjacent sibling)

```CSS
h2 + p {
  color: red;
}
```

`Hermano general:` Todas las etiquetas de parrafo al mismo nivel de h2

```CSS
h2 ~ p {
  color: red;
}
```

`Hijo:` La etiqueta parrafo que sea hija directa de la etiqueta div

```CSS
div > p {
  color: red;
}
```

`Descendiente:` Todas las etiquetas de parrafo que esten dentro de una etiqueta div

```CSS
div p {
  color: red;
}
```

### Trick medidas REM

Utilizar `rem` en lugar de `px` o `em`, para ello hay que establecer un valor predeterminado en la etiqueta raíz, de esa forma `1.6rem` serían equivalentes a `16px` y se podría manejar todo con valores rem

```CSS
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html  {
  font-size: 62.5%;
}

p {
  font-size: 1.6rem;
}
```

### Posiciones

> Static

- Posiciòn por default
- No es posible utilizar `top`, `right`, `left`, `button`
