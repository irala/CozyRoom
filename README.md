# CozyRoom 🧸

CozyRoom es una habitación virtual compartida para pasar un rato en compañía: conversar, personalizar muñecos, decorar el espacio y disfrutar de música o una videollamada.

## Entrar y compartir una sala

1. Abre [CozyRoom](https://irala.github.io/CozyRoom/).
2. Elige tu nickname cuando se solicite. Puedes cambiarlo después desde el vestidor.
3. Escribe un código de sala y pulsa **Ir**. Si no eliges otro, entrarás en `sala-principal`.
4. Pulsa **Invitar** o **Copiar enlace de sala** y comparte el enlace con quienes quieras invitar.

> Los códigos de sala no son contraseñas. No compartas información sensible hasta haber revisado los permisos de acceso de Firebase.

## Qué puedes hacer

- **Muñeco:** personaliza su aspecto, accesorios y estado desde el vestidor; arrastra el dibujo para moverlo.
- **Chat:** envía mensajes y emojis a las personas de la sala.
- **Cositas:** añade objetos decorativos o sube una foto como objeto compartido.
- **Ambiente:** cambia el fondo y usa los controles de sonido ambiental.
- **Música y vídeo:** elige contenido en el reproductor de YouTube.
- **Videollamada:** únete a una llamada de Jitsi desde la habitación.

En móvil, los botones inferiores permiten abrir los paneles de la habitación.

## Ejecutar el proyecto en local

El proyecto es una página estática. Descarga o clona el repositorio y abre `index.html` en un navegador moderno. También puedes servir la carpeta con un servidor web local.

La conexión en tiempo real depende de Firebase; YouTube, Jitsi, las fuentes y otros recursos se cargan desde servicios externos y necesitan conexión a internet. El navegador puede solicitar permisos para cámara y micrófono o bloquear la reproducción automática.

## Datos y privacidad

El chat, los avatares y los objetos compartidos, incluidas las fotos subidas, se envían a Firebase. El nickname y un identificador de usuario se guardan en el almacenamiento local del navegador.

Las salas no deben considerarse privadas solo por tener un código: es necesario revisar las reglas de Firebase y configurar los controles de acceso adecuados. Comparte únicamente contenido que las personas de la sala estén de acuerdo en compartir.

## Estado y mejoras pendientes

La versión publicada puede ir por detrás de los cambios locales: las correcciones de movimiento del muñeco y de miniaturas, la limpieza del nombre de prueba `Tester` y los sonidos de olas y bosque están pendientes de publicarse.

Entre las mejoras identificadas están:

- Restringir la edición del vestidor al muñeco propio y revisar los permisos de Firebase.
- Mejorar la presencia cuando una persona abre varias pestañas y la estabilidad del arrastre.
- Mostrar avisos cuando un mensaje, una foto o un cambio no se pueda guardar.
- Probar y pulir la experiencia táctil y la accesibilidad en móviles reales.
- Mejorar los controles de audio y definir límites y limpieza para fotos y mensajes.
