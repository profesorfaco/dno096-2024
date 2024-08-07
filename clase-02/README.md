### Introducción al desarrollo web desde el diseño → Clase 02 → 14/08/2024

# Comprendiendo dos lenguajes y una biblioteca: HTML5, CSS3 y p5.js

### Teoría (para la casa)

Ya pudimos reconocer la diferencia entre los lenguajes de descripción (HTML y CSS) y el lenguaje de programación (JS). 

Para comenzar a profundizar en un lenguaje de programación aprovechamos [p5.js](https://p5js.org/es/), una biblioteca fue creada por [Lauren McCarthy](http://lauren-mccarthy.com/) y es desarrollada por una comunidad de colaboradores, con apoyo de [Processing Foundation](https://processingfoundation.org/) y [NYU ITP](https://tisch.nyu.edu/). Entre los colaboradores hay 2 chilenos, que se han encargado de la traducción de referencias, tutoriales y [un libro](https://drive.google.com/drive/folders/1uGeBOGVAqwp6-JXnojcw2cvOIaS79ZEn?usp=sharing) al castellano; ellos son: [Guillermo Montecinos](https://guillemontecinos.cl/) y [Aarón Montoya-Moraga](https://montoyamoraga.io/).

[p5.js](https://p5js.org/es/) es una reinterpretación de [Processing](https://processing.org/) para la web. Consideremos que cuando se trabaja en Processing cada *sketch* tiene su `void setup()` y `void draw()`. Hay un `setup` que se ejecuta una única vez, en la partida. Hay un `draw` que por defecto se ejecuta una y otra vez. Ahora, cambiemos el `void` de [Java](https://es.wikipedia.org/wiki/Java_(lenguaje_de_programaci%C3%B3n)) por el `function` de [JavaScript](https://es.wikipedia.org/wiki/JavaScript), y tenemos:

```
function setup(){
  //colocas acá lo que se ejecuta una única vez
}

function draw(){
  //colocas acá lo que necesitas dibujar una y otra vez
}
```

Como se trata de una biblioteca de JavaScript se que ofrece como *una herramienta amigable para aprender a programar y hacer arte*, con [p5.js](https://p5js.org/es/) accedemos a un conjunto completo de funcionalidades para dibujar una y otra vez (`draw`). Sin embargo, no estamos limitados a dibujar; podemos tomar toda la página que se despliega en el navegador.

Y podemos tomar toda la página del navegador por el [Modelo de Objeto de Documento (DOM)](https://developer.mozilla.org/es/docs/Glossary/DOM): **A través del DOM, los programas escritos en JavaScript pueden acceder y modificar el contenido, estructura y estilo a la vista**.

Con el DOM podemos manipular una página así como cuando *photoshopeamos* una imagen. Si capturaste una imagen con 3 elementos y agregas un cuarto *photoshopénadolo*, en ningún caso modificas el fenómeno capturado, pero todos podrán ver una imagen con 4 elementos. 

Por la manipulación del DOM **podríamos encontrar inconcruencias entre** dos vista: la del **código fuente de la página** y la de los **elementos de la página**. Estirando la analogía: En el código fuente de la página ves el fenómeno tal como fue capturado, mientras que en la vista de elementos de la misma página está lo *photoshopeado* a partir de datos o ciertas condiciones.

Antes de continuar, conviene aclarar algunas cosas sobre datos en programación.

Partamos con el número 18261884. 

Si nos entregan tal número, sin contexto alguno, resultaría inútil. Pero es distinto de la siguiente manera: 

| País      |  Población       | Superficie     |
|:----------|:-----------------|:---------------|
| Chile     | 18261884         | 756102         |

Entendiendo cómo funciona una tabla, contamos con una clara orientación para la utilización de tal número como dato sobre algo concreto: La población en Chile. 

Además del dato de la población de Chile, contamos con su superficie. Si dividimos el primer dato por el segundo, obtenemos la densidad de la población en Chile. El resultado de aquella división es 24,15267252.

Los números 18261884 y 24,15267252 tienen una diferencia que corresponde apuntar:

- **18261884** es un número entero, un `int` (del inglés *integer*).

- **24,15267252** es un número de coma flotante, un `float` (del inglés *floating point number*; y no se olviden de esta diferencia, lo que para nosotros es coma, *for them* es punto, y el *coding* se hace en *english*).

A estos dos tipos de datos, podemos agregar: 

- **true** o **false** como las dos opciones posibles de un [tipo de dato lógico](https://es.wikipedia.org/wiki/Tipo_de_dato_l%C3%B3gico) (bool: *boolean*)

- **"A"** como un carácter (char: *character*)

- **"ALGUNAS PALABRAS"** como una cadena de caracteres (en inglés: *string*)

¡En el tipo de dato numérico y booleano no se usan comillas, pero cuando se tienen caracteres aislados o en cadena, sí!

Mencionamos `int`, `float`, `bool`, `char` y `string`, porque son palabras que en lenguajes de programación más clásicos se reservan para **declarar que tal variable almacenará tal tipo de dato. Pero en JavaScript podemos crear toda variables con una única palabra reservada,`var`**. También podemos usar `let` y `const`. Para entender la diferencia, conviene: 

- consultar el artículo [Var, let y const. ¿Donde, cuando y por qué?](https://medium.com/@tatymolys/var-let-y-const-donde-cuando-y-por-qu%C3%A9-d4a0ee66883b).

- ver el video [let vs var - Topics of JavaScript/ES6](https://www.youtube.com/watch?v=q8SHaDQdul0) (12 mins.)

Pero insistamos en el `var` para explorar las siguientes alternativas:

```
var a = 18261884;
var b = 24.15267252;
var c = true;
var d = "siguiente";
var e = ["siguiente", "repüyen", "seguente", "suivant", "next", "Nächster", "次の", "다음의"];
var f = {
    mom: "Luann Van Houten",
    dad: "Kirk Van Houten",
    child: "Milhouse Van Houten"
};
var g = {
    mom: "Marge Simpson",
    dad: "Homer Simpson",
    children: ["Bart Simpson", "Lisa Simpson", "Maggie Simpson"]
};
var h = [
    {
        mom: "Luann",
        dad: "Kirk",
        children: ["Milhouse"]
    },
    {
        mom: "Marge",
        dad: "Homer",
        children: ["Bart", "Lisa", "Maggie"]
    },
    {
        mom: "Manjula",
        dad: "Apu",
        children: ["Poonam", "Sashi", "Pria", "Uma", "Anoop", "Sandeep", "Nabendu", "Gheet"]
    }
];
```
**Lo que cambia viene después del signo igual `=`, que en este caso está asignando contenido a cada variable (es lo que se guarda dentro de ella si es que la pensamos como una caja).** 

Las variables de nombre `a`, `b` y `c` no requieren comillas. La variable `d`, que contiene una cadena de caracteres (*string*) sí usa comillas. 

La variable de nombre `e`, que contiene un arreglo, usa paréntesis cuadrado y cada elemento, por tratarse de un *string*, usa comillas (si fuesen números o booleanos no las usarían). 

La variable de nombre `f`, que contiene un objeto, usa paréntesis de llave que en su interior contiene pares de `nombre:valor`. 

Las variables de nombres `g` y `h` son mezclas de las anteriores.

- - - - - - - - - - - - -

### Práctica (para la clase)

Pendiente.

- - - - - - - 

###### [← CLASE ANTERIOR](https://github.com/profesorfaco/dno096-2024/tree/main/clase-01) — [SIGUIENTE CLASE →](https://github.com/profesorfaco/dno096-2024/tree/main/clase-03)

