### Introducción al desarrollo web desde el diseño → Clase 06

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

Y así de extraño puede ser el uso de una `{{frase típica}}` de cualquier dialecto.

Piense, por ejemplo, en la pregunta `{{cómo cancela}}` frente al hablante de castellano que no es chileno: *¡No, yo no quiero cancelar, quiero pagar lo que he consumido!*.  

Enfrentar el dialecto "chileno" con el "castellano actual" es una analogía que sirve para explicar el problema de usar *libraries* o *frameworks* de JavaScript antes que el "JavaScript a secas", analogía que se puede extender de la siguiente manera: 

El chileno se entiende en Chile. El argentino en Argetina. El mexicano se entienden en toda Hisponoamérica por el peso de sus empresas traductoras y televisivas. Pero lo que diga un castellano (del centro de España) debería ser entendido por chilenos, argentinos y mexicanos. 

Al alemán, inglés o italiano, le vendría mejor aprender castellano antes que chileno, argentino o mexicano, para moverse por Chile, Argentina, México y/o España sin mayores problemas.

Como la posición del curso frente a JavaScript se parece más a la de alemanes, ingleses o italianos frente al castellano, conviene comenzar a explorar JavaScript a secas, sin *libraries* ni *frameworks*.

#### Fetch()

En la práctica **haremos *fetch* de un JSON y una API**. 

**Pero no lo haremos con la ayuda de p5.js ni jQuery. Lo haremos sin bibliotecas de Javascript.**

Para explorar el JavaScript más estándar, sin bibliotecas, avanzaremos al [uso de `fetch()`](https://developer.mozilla.org/es/docs/Web/API/Fetch_API/Using_Fetch). 

Para comprender el uso del `fetch()`, es recomedable tomarse 32 minutos para ver dos videos de Daniel Shifmann:

- [fetch() - Working With Data & APIs in JavaScript](https://youtu.be/tc8DU14qX6I)
- [JSON - Working with Data and APIs in JavaScript](https://youtu.be/uxf0--uiX0I) 

En lo preparadao para la práctica:

El `fetch()` del JSON será muy sencillo, porque usa algo que está en la carpeta de esta clase:  
  
```
async function una() {
    const consulta = await fetch("https://raw.githubusercontent.com/profesorfaco/dno037-2023-2/main/clase-06/ciudades.json");
    const data = await consulta.json();
    console.log(data);
}
una().catch((error) => console.error(error));
```

El `fetch()` de la API nos exigirá un poco más, porque el uso de [Current Weather Data](https://openweathermap.org/current) requiere la definición de algunos parámetros y una autentificación con una API Key (que cualquier persona puede generar siendo [*user*](https://home.openweathermap.org/users/sign_in) de OpenWeather).

```
async function otra() {
    const consulta = await fetch("https://api.openweathermap.org/data/2.5/weather?q={city name},{country code}&appid={API key}");
    const data = await consulta.json();
    console.log(data);
}
otra().catch((error) => console.error(error));
```

- - - - - - -

### Práctica

Pendiente.

- - - - - - - - - - - -

###### [← CLASE ANTERIOR](https://github.com/profesorfaco/dno096-2024/tree/main/clase-05) — [SIGUIENTE CLASE →](https://github.com/profesorfaco/dno096-2024/tree/main/clase-08)
