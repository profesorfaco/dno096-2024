### Introducción al desarrollo web desde el diseño → Clase 10 → 09/10/2024 

# Conociendo Bootstrap v5.3

### Teoría

[Bootstrap](https://getbootstrap.com/) es un kit de herramientas de código abierto para la implementación de diseño [responsive](https://es.wikipedia.org/wiki/Dise%C3%B1o_web_adaptable) y [mobile-first](https://en.ryte.com/wiki/Mobile_First) de sitios y aplicaciones web. 

Con [Bootstrap](https://getbootstrap.com/) puedes implementar tanto prototipos rápidos como productos acabados, esto mediante el uso de Elementos de HTML5 relacionados con reglas de CSS3 predefinidas con [Sass](https://sass-lang.com/), además de una biblioteca de Javascript. 

Nosotros trabajaremos con [la más reciente](https://getbootstrap.com/docs/versions/), la quinta versión (punto tres, punto dos). 

Hay distintas maneras de comenzar a trabajar con Boostrap. Nosotros podemos partir con una adaptación de la [Starter template](https://getbootstrap.com/docs/5.3/getting-started/introduction/#quick-start), en un documento HTML que debe verse así: 

```
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>DNOO37 | BOOTSTRAP 5.3.2</title>
        <!--El CSS de Bootstrap-->
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
    </head>
    <body>
        <!--La biblioteca JS de Bootstrap-->
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
    </body>
</html>
```

Pueden copiar y pegar el código en un documento nuevo, creado en su editor de código fuente. Pueden guardar tal documento como `bootstrap.html`.

En el cuerpo del mismo documento HTML (`<body></body>`) podemos comenzar a utilizar las clases del CSS de Bootstrap, las que nos permiten tomar de 1 a 12 columnas (`class="col"`) en cada fila (`class="row"`) que esté dentro de un contenedor (`class="container"`).

Puesto de otro modo, podemos incluir, entre etiquetas `<body>…</body>`, algo como: 

```
<div class="container">
  <div class="row">
    <div class="col-4">Esto</div>
    <div class="col-4">es</div>
    <div class="col-4">Bootstrap</div>
  </div>
</div>
```

El código recién escrito indica que lo ancho se divide en 3 desde 0 pixeles de ancho. Sería distinto si usara las clases: `col-sm-4`, `col-md-4`, `col-lg-4`, `col-xl-4` o `col-xxl-4`. Por ejemplo, dentro de la división de clase `row`, podrían incluir:

```
<div class="col-lg-4"><img src="https://picsum.photos/300/300?random=1" class="w-100 my-2 shadow" /></div>
<div class="col-lg-4"><img src="https://picsum.photos/300/300?random=2" class="w-100 my-2 shadow" /></div>
<div class="col-lg-4"><img src="https://picsum.photos/300/300?random=3" class="w-100 my-2 shadow" /></div>
```

Nuevamente tomo 3 veces 4 columnas de las 12 disponibles; por ello tengo 3 imágenes en una misma fila en pantallas grandes (`-lg-`, de *large*), esto exige un ancho de la ventana del navegador igual o mayor a 992px.

Para más detalles sobre tamaños, conviene consultar directamente a la documentación de Bootstrap: https://getbootstrap.com/docs/5.3/layout/grid/#grid-options


- - - - - - - 

### Práctica

Pendiente.

- - - - - - - 

###### [← CLASE ANTERIOR](https://github.com/profesorfaco/dno096-2024/tree/main/clase-09) — [SIGUIENTE CLASE →](https://github.com/profesorfaco/dno096-2024/tree/main/clase-11)
