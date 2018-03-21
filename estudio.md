# Estudio de realidad aumentada

## Web-based AR
Artículos de interés:<br>
- [Web-Powered Augmented Reality: a Hands-On Tutorial](https://medium.com/@urish/web-powered-augmented-reality-a-hands-on-tutorial-9e6a882e323e)
- [Web AR with smart plugs using A-Frame](https://medium.com/the-unitgb/web-ar-with-smart-plugs-using-a-frame-d9828a846bd0)
### [A-frame](https://aframe.io/)
Es un entorno HTML diseñado originalmente por Mozilla para desarrollar aplicaciones de VR en la web basada en [three.js](https://threejs.org/). Es un entorno VR compatible con la mayoría de los [headsets](https://aframe.io/docs/0.8.0/introduction/) disponibles en el mercado, y puede ser utilizado para generar modelos 3D en aplicaciones de AR-web al incorporar la biblioteca [AR.js](https://aframe.io/blog/arjs/).

Es compatible con las siguientes bibliotecas web (la lista es más larga y se puede encontrar [aquí](https://aframe.io/docs/0.8.0/introduction/faq.html#does-a-frame-support-x-library-or-framework)):
- [D3.js](https://d3js.org/)
- [Preact](https://preactjs.com/)
- [React](https://reactjs.org/)

### [AR.js](https://github.com/jeromeetienne/AR.js)
Es una biblioteca de JavaScript que permite realizar aplicaciones de AR sobre HTML. Se puede conectar con [A-frame](https://aframe.io/blog/arjs/). En ese caso lo que AR.js hace es controlar la cámara del dispositivo basándose en etiquetas físicas que son detectadas por la cámara, de modo de dar el marco espacial para que A-frame renderice los modelos 3D.

Está basada en three.js y [jsartoolkit5](https://github.com/artoolkit/jsartoolkit5) y pensada para correr aplicaciones AR-web desde cualquier teléfono móvil que tenga webgl y webrtc, incluidos en la versión de Google Chrome 64 o superior. Un ejemplo de esta biblioteca es el [siguiente](https://github.com/jeromeetienne/AR.js#try-it-on-mobile).

Eficiencia en el uso de recursos?

#### Ventajas
- AR.js corre en la mayoría de los teléfonos móviles
- No requiere navegadores WebARonARCore o WebARonARKit
#### Desventajas
- Requiere etiquetas para anclar el modelo al mundo real
- No utiliza sensores espaciales del teléfono
- Espacialización depende sólo de la cámara del equipo
- Estabilidad en localización del modelo depende de la luminosidad del espacio
### [three.ar.js](https://github.com/google-ar/three.ar.js)
Es una biblioteca de JavaScript desarrollada por Google para crear aplicaciones AR web. Requiere la [extensión](https://github.com/google-ar/three.ar.js/blob/master/webvr_ar_extension.md) de la API WebVR para smartphones, disponibles en los navegadores WebARonARKit and WebARonARCore.

## Apple iOS

[ARKit](https://developer.apple.com/arkit/)

## Google Android
Google desarrolló la plataforma [AR Core](https://developers.google.com/ar/) para desarrollar aplicaciones móviles descargables de AR. La versin 1.0 fue lanzada a fines de febrero de 2018.

AR Core es una plataforma potente y moderna, compatible con softwares para desarrollo de VR como Unity y Unreal. La limitación de AR Core es que requiere teléfonos móviles de última generación, como el Samsung Galaxy S7 (o superior), el Google Pixel (o superior), y otros especificados [aquí](https://developers.google.com/ar/discover/).

### Web-based AR for Android
Para el desarrollo de aplicaciones AR web, Google ha desarrollado para Android - de manera no oficial aún - un navegador experimental llamado [WebARonARCore](https://github.com/google-ar/WebARonARCore). Al funcionar sobre AR Core de Google, este navegador exige los mismos requerimientos técnicos.

## Multiplataforma
- [Vuforia](https://www.vuforia.com/)
- [Holokit](https://holokit.io/) y [Holokit SDK](https://github.com/holokit/holokitsdk)

# Resources for AR app development
- [Web based VR talk](https://www.youtube.com/watch?v=9HAAbh6rq9Q)
- [How is ARCore better than ARKit?](https://medium.com/super-ventures-blog/how-is-arcore-better-than-arkit-5223e6b3e79d)

# Preguntas
- Cómo transpilar desde ARCore a ARKit?

https://easyar.com/

## Requerimientos tecnicos

|Marca |Modelo   |OS          |WiFi              |
|------|---------|------------|------------------|
|Apple |iPhone SE|iOS 11.2.6  |802.11ac          |
|Apple |iPhone 6s|iOS 11.2.6  |802.11ac with MIMO|
|Apple |iPhone 7 |iOS 11.2.6  |802.11ac with MIMO|
|Apple |iPhone 8 |iOS 11.2.6  |802.11ac with MIMO|
|Apple |iPhone X |iOS 11.2.6  |802.11ac with MIMO|
|Google|Pixel 2  |Android Oreo|802.11 a/b/g/n/ac |

# CUADRO COMPARATIVO DE LAS DISTINTAS APPROACHES

precios, disponibilidades en el mercado, marcas, años

resolucion, latencia, costos

dependencias, costos mensuales, facilidad de instalacion

## Referencias

* [iPhone SE](https://www.apple.com/iphone-se/specs/)
* [iPhone 6s](https://www.apple.com/iphone-6s/specs/)
* [iPhone 7](https://www.apple.com/iphone-7/specs/)
* [iPhone 8](https://www.apple.com/iphone-8/specs/)
* [iPhone X](https://www.apple.com/iphone-x/specs/)
* [Google Pixel 2](https://store.google.com/us/product/pixel_2_specs)
