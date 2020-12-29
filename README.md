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

### Uso de imagenes (loseless vs lossy) sin perdida y con perdida

- JPG `lossy` (fotografias e imágenes fijas)
- PNG 8 `lossless` (iconos, con transparencia y sin animación)
- GIF `lossless` (animaciones simples y gráficos con colores planos)
- Vectores `lossless` (imágenes fijas, pantallas de alta resolución, ideal para gráficos y logotipos en la web)
