### Introducción al desarrollo web desde el diseño → Clase 05

# Aplicando HTML5, CSS3 y otras bibliotecas de JS

### Teoría (para la casa)

Existen [muchas bibliotecas de JavaScript](https://en.wikipedia.org/wiki/List_of_JavaScript_libraries), además de [p5.js](https://p5js.org/es/) y [ml5.js](https://ml5js.org/). 

La [biblioteca de JavaScript](https://en.wikipedia.org/wiki/List_of_JavaScript_libraries) que exploraremos hoy será [jQuery](https://jquery.com/) - *A fast, small, and feature-rich JavaScript library*.

**[jQuery](https://jquery.com/) es una biblioteca que nos simplifica la redacción de instrucciones en JavaScript, sobre todo cuando se busca manipular el DOM y hacer transiciones animadas**. Su primera versión estable fue lanzada el año 2006, lo que es anterior a la primera revisión importante del [estándar de JavaScript](https://en.wikipedia.org/wiki/ECMAScript), la [ES5 del 2009](https://www.w3schools.com/js/js_es5.asp), con la que se comenzó a simplificar la redacción del mismo lenguaje.

Conviene partir con un ejemplo: En una página web tenemos varios elementos con una clase a la que denominamos "media". Para afectar a todos los elementos que tienen esa clase con un cambio de color desde JavaScript, sin usar bibliotecas, hace algunos años habríamos escrito la siguiente instrucción:

```
var elementos = Array.from(document.getElementsByClassName("media"));
elementos.forEach(function(elemento){
  elemento.style.color="red";
});
```

Pero con el [estándar de JavaScript actual](https://www.w3schools.com/js/js_versions.asp) se simplifica un poco:

```
var elementos = document.querySelectorAll(".media");
elementos.forEach(elemento => elemento.style.color="red");
```

Ahora bien, usando [jQuery](https://jquery.com/), basta con escribir:

```
$(".media").css("color","red");
```

Para la primera década del 2000, [jQuery](https://jquery.com/) ofrecía una simplificación radical en el trabajo con JavaScript. Pero en los años más recientes el mismo lenguaje ha tendido a simplificarse o hacerse más moderno, como veremos líneas más abajo: ¡No conviene perder de vista esta tendencia por prestarle mucha atención a la biblioteca!

Hecha la advertencia, agreguemos un nivel más al ejemplo para poder entender el uso de la biblioteca: 

```
function enrojece() {
  $(".media").css("color","red");
}
$("#cambio").on("click", enrojece);
```

Tal instrucción está abreviando, mediante [jQuery](https://jquery.com/), lo siguiente:

```
function enrojece(){
  var elementos = document.querySelectorAll(".media");
  elementos.forEach(elemento => elemento.style.color="red");  
}
document.querySelector("#cambio").addEventListener("click", enrojece);
```

Con la última instrucción de jQuery, el cambio de color sobre todos los elementos de clase "media" se hace al presionar el botón de identidad "cambio". **Y ya resulta evidente que la clave del uso de [jQuery](https://jquery.com/) está en la concatenación de un selector y una acción: `$(selector).action()`** 

- - - - - - -

#### Práctica

Pendiente.

- - - - - - - -

###### [← CLASE ANTERIOR](https://github.com/profesorfaco/dno096-2024/tree/main/clase-04) — [SIGUIENTE CLASE →](https://github.com/profesorfaco/dno096-2024/tree/main/clase-06)
