CHAMBRE NOIRE · paquete instalable (PWA)
========================================

Contenido
  index.html              El juego completo (HTML + JS + CSS en un solo archivo).
  manifest.webmanifest    Datos de instalación (nombre, iconos, pantalla completa).
  sw.js                   Service worker: guarda el juego para que funcione sin conexión.
  icon-*.png              Iconos.
  robots.txt              Pide a los buscadores que no indexen la dirección.

Publicación
  1. Subir la carpeta entera, tal cual, a un alojamiento estático con HTTPS
     (sin HTTPS no se instala ni funciona el service worker).
  2. Usar una dirección estable mientras esté en línea: la partida se guarda
     ligada a esa dirección.
  3. Repartir la dirección en mano. Quien la abra en el navegador verá la
     pantalla de instalación; el juego solo arranca desde la pantalla de inicio.

Modo prueba
  En index.html, al principio del código, cambiar
      "prueba": false   por   "prueba": true
  Con el juego abierto, mantener pulsado «Espectadores: 1» (en la Pantalla 0 o
  en la habitación) abre el panel: saltos de tiempo (equivalen a cerrar y volver
  más tarde), deleite, noches sin dormir, fase siguiente, reinicio.
  Para probar en un navegador de escritorio sin instalar, poner también
      "exigirInstalacion": false
  Volver a dejar ambos valores como estaban antes de repartirlo.

Sin verificar (pendiente §21.1)
  - Que la app instalada siga abriendo sin conexión después de retirar la web.
  - Persistencia del almacenamiento en iPhone tras ausencias largas.
  - En iPhone, Safari y la app de pantalla de inicio no comparten datos: la pestaña
    del navegador no puede saber que ya se instaló (en Android sí).
  - El interruptor de silencio del iPhone apaga el sonido del juego.

No envía nada: todo se queda en el teléfono.
