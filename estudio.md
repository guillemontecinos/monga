# Estudio de realidad aumentada

## Web-based AR

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
En junio de 2017 Apple lanzó [ARKit](https://developer.apple.com/arkit/), un entorno de programación para desarrollar aplicaciones de AR en iOS. ArKit es compatible con iOS 11 o superior y ya se encuentra disponible en su versión 1.5 que es compatible con iOS 11.3 beta.

## Google Android
Google desarrolló la plataforma [AR Core](https://developers.google.com/ar/) para desarrollar aplicaciones móviles descargables de AR. La versin 1.0 fue lanzada a fines de febrero de 2018.

AR Core es una plataforma potente y moderna, compatible con softwares para desarrollo de VR como Unity y Unreal. Requiere un OS Android 7.0 o superior. La limitación de AR Core es que requiere teléfonos móviles de última generación, como el Samsung Galaxy S7 (o superior), el Google Pixel (o superior), y otros especificados [aquí](https://developers.google.com/ar/discover/).

### Web-based AR for Android
Para el desarrollo de aplicaciones AR web, Google ha desarrollado para Android - de manera no oficial aún - un navegador experimental llamado [WebARonARCore](https://github.com/google-ar/WebARonARCore). Al funcionar sobre AR Core de Google, este navegador exige los mismos requerimientos técnicos.

## Multiplataforma
### [Vuforia](https://www.vuforia.com/)
Es la plataforma de desarrollo de experiencias AR más utilizada. Licencia especial gratuita para desarrolladores que trabajan con [Unity](https://unity3d.com/). Licencia estándar de Vuforia tiene un costo de $499.00.

#### Requerimientos dispositivo móvil
|OS     |Versión|
|-------|-------|
|Android|4.4+   |
|iOS    |9+     |
|Windows|10     |

Fuente: [Vuforia Supported Versions](https://library.vuforia.com/articles/Solution/Vuforia-Supported-Versions.html)



### [Holokit](https://holokit.io/)
Es una plataforma open source de realidad mixta (MR), que permite generar experiencias immersivas utilizando el teléfono móvil. La realidad mixta es una variante que intenta mezclar los mejores atributos de VR y AR, generalmente creando experiencias a mediante el uso de visores VR en el que se puede ver el mundo real (mostrado mediante una cámara) sobre el cual se montan modelos de VR.

Holokit consiste en un kit de visores de cartón en el que se monta un teléfono móvil, y un software de desarrollo basado en entornos de AR. Es compatible con ARKit y ARCore, por lo que tiene las mismas limitaciones de costo que dichas plataformas.

# Preguntas
- Cómo transpilar desde ARCore a ARKit?

https://easyar.com/

# Requerimientos técnicos para montaje

|Marca  |Modelo        |Fecha|$ USD|OS                |WiFi              |
|-------|--------------|-----|-----|------------------|------------------|
|Apple  |iPhone 6s     |2015 |449  |iOS 11.2.6        |802.11ac with MIMO|
|Apple  |iPhone SE     |2016 |349  |iOS 11.2.6        |802.11ac          |
|Apple  |iPhone 7      |2016 |549  |iOS 11.2.6        |802.11ac with MIMO|
|Apple  |iPhone 8      |2017 |699  |iOS 11.2.6        |802.11ac with MIMO|
|Apple  |iPhone X      |2017 |999  |iOS 11.2.6        |802.11ac with MIMO|
|Google |Pixel         |2016 |549  |Android Oreo 8.0  |802.11 a/b/g/n/ac |
|Google |Pixel 2       |2017 |649  |Android Oreo 8.0  |802.11 a/b/g/n/ac |
|Samsung|Galaxy S7     |2016 |469  |Android Nougat 7.0|802.11 a/b/g/n/ac |
|Samsung|Galaxy S7 edge|2016 |569  |Android Nougat 7.0|802.11 a/b/g/n/ac |
|Samsung|Galaxy S8     |2017 |599  |Android Oreo 8.0  |802.11 a/b/g/n/ac |
|Samsung|Galaxy S8+    |2017 |689  |Android Oreo 8.0  |802.11 a/b/g/n/ac |
|Samsung|Galaxy Note 8 |2017 |950  |Android Oreo 8.0  |802.11 a/b/g/n/ac |
|Samsung|Galaxy S9     |2018 |719  |Android Oreo 8.0  |802.11 a/b/g/n/ac |
|Samsung|Galaxy S9+    |2018 |839  |Android Oreo 8.0  |802.11 a/b/g/n/ac |


# Cuadro comparativo SDK
|Plataforma         |Empresa  |$ USD|Android|iOS    |Windows|
|-------------------|---------|-----|-------|-------|-------|
|AR Kit             |Apple    |     |N/A    |11+    |N/A    |
|AR Core            |Google   |     |7.0+   |N/A    |N/A    |
|Vuforia            |PTC      |499  |4.4+   |9+     |10     |

Fuentes:
- [Versión OS Android para AR Core](https://developers.google.com/ar/discover/)
- [Versión iOS para AR Kit](https://developer.apple.com/arkit/)
- [Versiones iOS, Android y Windows compatibles con Vuforia](https://library.vuforia.com/articles/Solution/Vuforia-Supported-Versions.html)
- [Licencia Vuforia](https://developer.vuforia.com/vui/pricing)

precios, disponibilidades en el mercado, años

resolucion, latencia,

dependencias, costos mensuales, facilidad de instalacion

# Referencias

## Tecnologías

* [Google ARCore](https://developers.google.com/ar/discover/)

## Artículos de Interés
* [Web-Powered Augmented Reality: a Hands-On Tutorial](https://medium.com/@urish/web-powered-augmented-reality-a-hands-on-tutorial-9e6a882e323e)
* [Web AR with smart plugs using A-Frame](https://medium.com/the-unitgb/web-ar-with-smart-plugs-using-a-frame-d9828a846bd0)
* [How to create Augmented Reality posters with Unity & Vuforia](https://medium.com/@devdevcharlie/how-to-create-augmented-reality-posters-with-unity-vuforia-ec80a82e6d51)
* [How is ARCore better than ARKit?](https://medium.com/super-ventures-blog/how-is-arcore-better-than-arkit-5223e6b3e79d)

## Teléfonos

* [Apple iPhone SE specs](https://www.apple.com/iphone-se/specs/)
* [Apple iPhone SE wiki](https://en.wikipedia.org/wiki/IPhone_SE)
* [Apple iPhone 6s specs](https://www.apple.com/iphone-6s/specs/)
* [Apple iPhone 6s wiki](https://en.wikipedia.org/wiki/IPhone_6S)
* [Apple iPhone 7 specs](https://www.apple.com/iphone-7/specs/)
* [Apple iPhone 7 wiki](https://en.wikipedia.org/wiki/IPhone_7)
* [Apple iPhone 8 specs](https://www.apple.com/iphone-8/specs/)
* [Apple iPhone 8 wiki](https://en.wikipedia.org/wiki/IPhone_8)
* [Apple iPhone X specs](https://www.apple.com/iphone-x/specs/)
* [Apple iPhone X wiki](https://en.wikipedia.org/wiki/IPhone_X)
* [Google Pixel specs](https://store.google.com/us/product/pixel_phone_specs)
* [Google Pixel wiki](https://en.wikipedia.org/wiki/Pixel_(smartphone))
* [Google Pixel 2 specs](https://store.google.com/us/product/pixel_2_specs)
* [Google Pixel 2 wiki](https://en.wikipedia.org/wiki/Pixel_2)
* [Samsung Galaxy S7](http://www.samsung.com/global/galaxy/galaxy-s7/)
* [Samsung Galaxy S7 specs](https://www.gsmarena.com/samsung_galaxy_s7-7821.php)
* [Samsung Galaxy S7 wiki](https://en.wikipedia.org/wiki/Samsung_Galaxy_S7)
* [Samsung Galaxy S8](http://www.samsung.com/global/galaxy/galaxy-s8/)
* [Samsung Galaxy S8 specs](http://www.samsung.com/global/galaxy/galaxy-s8/specs/)
* [Samsung Galaxy S8 wiki](https://en.wikipedia.org/wiki/Samsung_Galaxy_S8)

