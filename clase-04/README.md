### Introducción al desarrollo web desde el diseño → Clase 04 → 28/08/2024 

# Conociendo y comprendiendo otras bibliotecas de JS

### Teoría (para la casa)

Para comenzar a comprender JavaScript, aprovechamos [p5.js](https://p5js.org/es/): una biblioteca de JavaScript que es una reinterpretación de [Processing](https://processing.org/) para la web. 

Aprendimos que en el sitio web  oficial de tal biblioteca de Javascript se pueden encontrar secciones de referencias, tutoriales, ejemplos, etc. Tales secciones nos permiten aprender a reconocer lo que sería, en analogía, un dialecto. Estirando la analogía: Consideren lo que pasa con el chileno en algún oficio o región determinada: Tienen a la base el castellano, pero puede haber instrucciones con palabras que no hagan sentido a quienes las escuchen desde otro oficio o región.

Para acercarnos a otras bibliotecas, corresponde aprovechar su sitio web oficial, y las secciones que ofrezca para poder relacinarse con sus particulares instrucciones y palabras.

#### ml5.js

Recordemos una escena de Matrix: [Cuando Trinity aprende a pilotar un helicóptero B-212 después de recibir un programa](https://youtu.be/6AOpomu9V6Q?si=aMsX5lEtYqG6WP_D). Partiendo de esa ficción, hagamos de cuenta que una "página web" puede aprender a asociar lo que escucha con alguna etiqueta (*label*), indicando un grado de confianza (*confidence*) para tal asociación. 

Podría ser que sus etiquetas (*labels*) sean limitadas. Que se limiten, por ejemplo, a las siguientes palabras en inglés: *zero*, *one*, *two*, *three*, *four*, *five*, *six*, *seven*, *eight*, *nine*, *up*, *down*, *left*, *right*, *go*, *stop*, *yes* o *no*.

Con tal ejemplo en mente, revisemos este *sketch* preparado en el Editor Web de p5.js: https://editor.p5js.org/ml5/sketches/HUm7NYMW3

Después de un *play*, aceptar que el navegador acceda al micrófono y darle un tiempo a que cargue un listado de palabras, podemos comenzar a decir tales palabras.

Eso es p5.js trabajando con **ml5.js, otra biblioteca de JavaScript**; ambas bibliotecas son compatibles desde sus intenciones, de hecho el [ml5.js Community Statement](https://ml5js.org/about) es un *copy/paste* del [p5.js community statement](https://p5js.org/community/). Esta compatibilidad explicaría el *5* después del *ml* de *Machine Learning*, pero:

> Developing [ml5](https://ml5js.org/about/) is not just about developing machine learning software, it is about making machine learning approachable for a broad audience of artists, creative coders, and students. The library provides access to machine learning algorithms and models in the browser, building on top of [TensorFlow.js](https://www.tensorflow.org/learn?hl=es-419) with no other external dependencies.

Para explorar esta biblioteca de JavaScript, así como cualquier otra biblioteca del mismo lenguaje de programación, corresponde consultar las referencias que, por lo general, se presentan en su sitio web oficial.

En el caso de las [referencia de ml5.js](https://docs.ml5js.org/#/reference/overview), tenemos un presentación organizada en 7 modelos, basadas en los tipos de entrada y salida con los que se puede trabajar:

1 BodyPose

2 BodySegmentation

3 HandPose

4  FaceMesh

5 ImageClassifier

6 SoundClassifier

7 Sentiment

Antes de seguir –antes de la práctica–, conveniente revisar: 

- Este video: [A Beginner's Guide to Machine Learning with ml5.js](https://www.youtube.com/watch?v=jmznx0Q1fP0)

- Este artículo: [El mal que aqueja a las IA es la abducción](https://hipermediaciones.com/2023/08/21/el-mal-que-aqueja-a-las-ia-es-la-abduccion/)

Viendo tal video y/o leyendo tal artículo podrían hacerse de una idea sobre el concepto de *machine learning* y comenzar a relacionarlo con varios más.

- - - - - - - - - - - - -

### Práctica (para la clase)

Pendiente.

- - - - - - - 

###### [← CLASE ANTERIOR](https://github.com/profesorfaco/dno096-2024/tree/main/clase-03) — [SIGUIENTE CLASE →](https://github.com/profesorfaco/dno096-2024/tree/main/clase-05)
