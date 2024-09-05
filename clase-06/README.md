### Introducción al desarrollo web desde el diseño → Clase 06 → 11/09/2024

# Aplicando HTML5, CSS3 y JS sin bibliotecas

### Teoría (para la casa)

Ya avanzada la segunda década del 2000, cuando casi no se habla de sitios sino aplicaciones web, podría ser necesario exigir a las bibliotecas de JavaScript algo más que simplificarnos la tarea de manipular el DOM y hacer transiciones animadas. 

Tanto corresponde exigirles que, a veces, el concepto de biblioteca (*library*) queda chico, y se cambia por marco de trabajo (*framework*).

Hay 3 frameworks de JavaScript importantes en la actualidad:

- React → https://es.reactjs.org/

- Angular → https://angular.io/

- Vue.js → https://vuejs.org/

El primero es de Meta (Facebook). El segundo es mantenido por Google. El tercero tiene cierta independencia y ofrece una alternativa progresiva: No debes transformar todo tu código fuente a su particular redacción, puedes ir adoptándolo de a poco. Pero su objetivo, ya en lo más básico, apunta al "montaje" de aplicaciones:

```
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
        <title>Ejemplo</title>
    </head>
    <body>
        <div id="app">{{ message }}</div>
        <script>
            const { createApp, ref } = Vue
            createApp({
                setup() {
                    const message = ref('¡Hola Vue.js!')
                    return {
                        message
                    }
                }
            }).mount('#app')
        </script>
    </body>
</html>
```

En el código tenemos una estructura reconocible: ¡Es una página `.html`! 

Pero incluye algo extraño: `{{ message }}`, que en su carga es reemplazado por un `¡Hola Vue.js!`, que es un texto que allí es "montado" como si se tratara de una aplicación (ver: [`createApp`](https://vuejs.org/guide/essentials/application.html#the-root-component), [`mount()`](https://vuejs.org/guide/essentials/application.html#mounting-the-app)). 

Pero no queremos desarrollar aplicaciones web. Por ahora será suficiente *desarrollar, de manera autónoma, su primer sitio web profesional o prototipo avanzado de aplicación web*. Por eso sólo basta con referir a los "frameworks", para no confudirlos con "libraries". 

Por lo pronto, vamos a empezar a avanzar en el trabajo en JavaScript independiente de p5.js, ml5.js, jQuery u otras.

#### Fetch()

En la práctica **hemos trabajando con un JSON y una API. Lo hicimos con la ayuda de jQuery. Ahora lo haremos sin bibliotecas de Javascript.**

Para comenzar a trabajar con el JavaScript estándar más reciente, y sin bibliotecas, partiremos con el [`fetch()`](https://developer.mozilla.org/es/docs/Web/API/Fetch_API/Using_Fetch). 

Para comprender el uso del `fetch()`, es recomedable tomarse 32 minutos para ver dos videos de Daniel Shifmann:

- [fetch() - Working With Data & APIs in JavaScript](https://youtu.be/tc8DU14qX6I)
- [JSON - Working with Data and APIs in JavaScript](https://youtu.be/uxf0--uiX0I) 

Si la clase pasada fuimos a buscar un JSON de esta manera:

```
$.getJSON("https://raw.githubusercontent.com/profesorfaco/dno096-2024/main/clase-05/datos.json", function (data) {
    console.log(data);
});
```

En la clase de hoy lo iremos a buscar de esta otra:

```
async function astros() {
    const consulta = await fetch("https://raw.githubusercontent.com/profesorfaco/dno096-2024/main/clase-05/datos.json");
    const data = await consulta.json();
    console.log(data);
}
astros().catch((error) => console.error(error));
```

Aquí aparece el `asyn`, que conviene revisar en [MDN web docs]( https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/async_function#descripci%C3%B3n)

- - - - - - -

### Práctica

Pendiente.

- - - - - - - - - - - -

###### [← CLASE ANTERIOR](https://github.com/profesorfaco/dno096-2024/tree/main/clase-05) — [SIGUIENTE CLASE →](https://github.com/profesorfaco/dno096-2024/tree/main/clase-08)
