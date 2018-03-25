# Informe Técnico: Estado del Arte de la Realidad Aumentada (AR) en teléfonos móviles para implementación de aplicación AR en montaje teatral
*Por Aarón Montoya y Guillermo Montecinos*<br>
*27 de abril de 2018*

## Introducción
El siguiente informe técnico aborda el estado del arte de las tecnologías asociadas a la Realidad Aumentada (AR, por sus siglas en inglés), la que ententemos como un continuo que abarca desde un entorno real hasta un entorno virtual puro (Paul Milgram et al., 1994). La AR permite la incorporación de información digital - imágenes, datos, modelos 3D, sonido, entre otros - a un entorno real, mediante el reconocimiento espacial de patrones realizado por un software.

El objetivo de este estudio es describir el panorama de la AR, caracterizar las tecnologías disponibles y las posibles soluciones que se pueden lograr en función de cumplir con los requisitos del montaje teatral "Monga". Para ello se enumeran y describen las tecnologías y estrategias más comunes para desarrollar aplicaciones de AR. Adicionalmente, se revisan qué teléfonos móviles son requeridos para ejecutar las tecnologías revisadas, y qué soporte técnico se requiere para implementar la app en escena.

## Realidad Aumentada
La generación de experiencias AR en dispositivos móviles consiste en el despliegue de información, datos o modelos 3D virtuales en un entorno real. Para que el despliegue de esta información sea coherente con el entorno, los sistemas de AR requieren un análisis del espacio de modo de detectar planos, profundidad, bordes y otros atributos que entreguen información espacial, y el movimiento del equipo respecto de este espacio. Esto se llama odometría y corresponde al análisis de la trayectoria de puntos en el espacio.

Actualmente existen dos métodos para realizar odometría con un dispositivo móvil orientada a AR: la primera consiste en el uso de referencias, particularmente etiquetas, que pueden ser seguidas y permiten el reconocimiento de planos a través de la cámara del equipo. La segunda se denomina Odometría Visual Inercial (VIO, por su nombre en inglés *Visual Intertial Odometry*) y corresponde a un sistema un poco más complejo que mediante el reconocimiento de planos, bordes y puntos de anclaje a través de la cámara, sumado al análisis de la información inercial entregada por los sensores integrados en el equipo, estima la posición y orientación de un equipo en el espacio. 

La calidad de la experiencia generada depende intensamente de la tecnología elegida, ya que una app basada en VIO al contar con mayor información espacial puede tener muchos mejores resultados con un costo mayor de recursos de procesamiento, mientras que una app basada en etiquetas puede lograr resultados menos complejos con una exigencia de procesamiento menor. Las aplicaciones AR pueden ser montadas de dos formas distintas en teléfonos móviles: por un lado se pueden desarrollar localmente en un kit de desarrollo para luego ser publicadas en la *App Store*, mientras que por otro ladose pueden desarrollar en un entorno web que para ser ejecutadas en el navegador. Las características y requerimientos de cada una serán descritas a continuación.

### SDKs para desarrollo de apps AR descargables
Un SDK (Kit de Desarrollo de Software, en inglés *Software Development Kit*) es una plataforma que permite el desarrollo de software en un entorno particular, y que tiene una serie de complementos orientados a ciertas funciones específicas. Durante el año 2017 Apple y Google lanzaron kits de desarrollo de aplicaciones de AR en los sistemas operativos iOS y Android, respectivamente. Con anterioridad a esto Vuforia, creado por la compañía Qualcomm y en 2015 adquirido por PTC, se ha posicionado como la plataforma de desarrollo de aplicaicones AR con más impacto en el mercado.

#### Google Android
En 2017 Google lanzó la plataforma [AR Core](https://developers.google.com/ar/), un SDK para desarrollar aplicaciones móviles de AR basado en la experiencia del proyecto [Tango](https://es.wikipedia.org/wiki/Project_Tango), plataforma AR experimental creada por la compañía en 2015. La versión 1.0 fue lanzada a fines de febrero de 2018.

AR Core es una plataforma potente y moderna, compatible con softwares para desarrollo de VR como Unity y Unreal. Requiere un OS Android 7.0 o superior. La limitación de ARCore es que requiere teléfonos móviles de última generación, como el Samsung Galaxy S7 (o superior), el Google Pixel (o superior), y otros especificados [aquí](https://developers.google.com/ar/discover/).

#### Apple iOS
En junio de 2017 Apple lanzó [ARKit](https://developer.apple.com/arkit/), un entorno de programación para desarrollar aplicaciones de AR en iOS. ArKit es compatible con iOS 11 o superior y ya se encuentra disponible en su versión 1.5 que es compatible con iOS 11.3 beta.

#### Multiplataforma
##### [Vuforia](https://www.vuforia.com/)
Es la plataforma de desarrollo de experiencias AR más utilizada. Licencia especial gratuita para desarrolladores que trabajan con [Unity](https://unity3d.com/). Licencia estándar de Vuforia tiene un costo de $499.00.

###### Requerimientos dispositivo móvil
|OS     |Versión|
|-------|-------|
|Android|4.4+   |
|iOS    |9+     |
|Windows|10     |

Fuente: [Vuforia Supported Versions](https://library.vuforia.com/articles/Solution/Vuforia-Supported-Versions.html)

##### [Holokit](https://holokit.io/)
Es una plataforma open source de realidad mixta (MR), que permite generar experiencias inmersivas utilizando el teléfono móvil. La realidad mixta es una variante que intenta mezclar los mejores atributos de VR y AR, generalmente creando experiencias a mediante el uso de visores VR en el que se puede ver el mundo real (mostrado mediante una cámara) sobre el cual se montan modelos de VR.

Holokit consiste en un kit de visores de cartón en el que se monta un teléfono móvil, y un software de desarrollo basado en entornos de AR. Es compatible con ARKit y ARCore, por lo que tiene las mismas limitaciones de costo que dichas plataformas.

#### Preguntas
- Cómo transpilar desde ARCore a ARKit?

https://easyar.com/


#### Cuadro comparativo SDK
|Plataforma |Empresa  |Año  |$ USD|Android|iOS    |
|-----------|---------|-----|-----|-------|-------|
|AR Kit     |Apple    |2017 |N/A  |N/A    |11+    |
|AR Core    |Google   |2017 |N/A  |7.0+   |N/A    |
|Vuforia    |PTC      |     |499  |4.4+   |9+     |

Fuentes:
- [Versión OS Android para AR Core](https://developers.google.com/ar/discover/)
- [Versión iOS para AR Kit](https://developer.apple.com/arkit/)
- [Versiones iOS, Android y Windows compatibles con Vuforia](https://library.vuforia.com/articles/Solution/Vuforia-Supported-Versions.html)
- [Licencia Vuforia](https://developer.vuforia.com/vui/pricing)

precios, disponibilidades en el mercado,

resolucion, latencia,

dependencias, costos mensuales, facilidad de instalacion

### Web-based AR

#### [A-frame](https://aframe.io/)
Es un entorno HTML diseñado originalmente por Mozilla para desarrollar aplicaciones de VR en la web basada en [three.js](https://threejs.org/). Es un entorno VR compatible con la mayoría de los [headsets](https://aframe.io/docs/0.8.0/introduction/) disponibles en el mercado, y puede ser utilizado para generar modelos 3D en aplicaciones de AR-web al incorporar la biblioteca [AR.js](https://aframe.io/blog/arjs/).

Es compatible con las siguientes bibliotecas web (la lista es más larga y se puede encontrar [aquí](https://aframe.io/docs/0.8.0/introduction/faq.html#does-a-frame-support-x-library-or-framework)):
- [D3.js](https://d3js.org/)
- [Preact](https://preactjs.com/)
- [React](https://reactjs.org/)

#### [AR.js](https://github.com/jeromeetienne/AR.js)
Es una biblioteca de JavaScript que permite realizar aplicaciones de AR sobre HTML. Se puede conectar con [A-frame](https://aframe.io/blog/arjs/). En ese caso lo que AR.js hace es controlar la cámara del dispositivo basándose en etiquetas físicas que son detectadas por la cámara, de modo de dar el marco espacial para que A-frame renderice los modelos 3D.

Está basada en three.js y [jsartoolkit5](https://github.com/artoolkit/jsartoolkit5) y pensada para correr aplicaciones AR-web desde cualquier teléfono móvil que tenga webgl y webrtc, incluidos en la versión de Google Chrome 64 o superior. Un ejemplo de esta biblioteca es el [siguiente](https://github.com/jeromeetienne/AR.js#try-it-on-mobile).

Eficiencia en el uso de recursos?

##### Ventajas
* AR.js corre en la mayoría de los teléfonos móviles
* No requiere navegadores WebARonARCore o WebARonARKit

##### Desventajas
* Requiere etiquetas para anclar el modelo al mundo real
* No utiliza sensores espaciales del teléfono
* Espacialización depende sólo de la cámara del equipo
* Estabilidad en localización del modelo depende de la luminosidad del espacio

#### [three.ar.js](https://github.com/google-ar/three.ar.js)
Es una biblioteca de JavaScript desarrollada por Google para crear aplicaciones AR web. Requiere la [extensión](https://github.com/google-ar/three.ar.js/blob/master/webvr_ar_extension.md) de la API WebVR para smartphones, disponibles en los navegadores WebARonARKit and WebARonARCore.

#### Web-based AR for Android
Para el desarrollo de aplicaciones AR web, Google ha desarrollado para Android - de manera no oficial aún - un navegador experimental llamado [WebARonARCore](https://github.com/google-ar/WebARonARCore). Al funcionar sobre AR Core de Google, este navegador exige los mismos requerimientos técnicos.


## Requerimientos técnicos para montaje
El montaje de la obra "Monga" considera el uso de 30 o más disposivos móviles a una red WiFi para la descarga de una aplicación móvil o la descarga de datos a través de una app o el navegador web.

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

## Conclusiones

## Referencias

### Tecnologías

* [Google ARCore](https://developers.google.com/ar/discover/)

### Artículos de Interés
* [Realidad Aumentada, Wikipedia](https://es.wikipedia.org/wiki/Realidad_aumentada)
* [Web-Powered Augmented Reality: a Hands-On Tutorial](https://medium.com/@urish/web-powered-augmented-reality-a-hands-on-tutorial-9e6a882e323e)
* [Web AR with smart plugs using A-Frame](https://medium.com/the-unitgb/web-ar-with-smart-plugs-using-a-frame-d9828a846bd0)
* [How to create Augmented Reality posters with Unity & Vuforia](https://medium.com/@devdevcharlie/how-to-create-augmented-reality-posters-with-unity-vuforia-ec80a82e6d51)
* [How is ARCore better than ARKit?](https://medium.com/super-ventures-blog/how-is-arcore-better-than-arkit-5223e6b3e79d)

### Teléfonos

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

