# Cambios de miamiOS

## 1.7.3 — 14 de noviembre de 2026
- Encontrar mi dispositivo: Google Play Services, Encontrar mi dispositivo y los servicios de Google quedan
  fuera del reposo profundo (Doze) y del ahorro de datos, fijo desde el sistema. Así los localizadores
  deberían actualizarse en el teléfono sin tener que abrir la web.

## 1.7.2 — 14 de noviembre de 2026
- Ultra ahorro: ahora existe de verdad. App "Ultra ahorro" con su ícono y pantalla, y mosaico en
  Ajustes rápidos. Al activarlo: apaga Wi-Fi y sincronización, baja el tiempo de pantalla a 15 s,
  quita animaciones y enciende el ahorro de batería de Android. Al apagarlo (o si apagas el ahorro
  de Android) devuelve todo como estaba. La pantalla sigue siempre a 120 Hz.

## 1.7.1 — 13 de noviembre de 2026
- Vuelta a la 1.7: la 1.8 no funcionó bien y se retiró. Esta versión es la 1.7 tal cual, con fecha
  nueva para que el teléfono la acepte. La pantalla queda siempre en 120 Hz, también en ahorro de energía.

## 1.7 — 8 de noviembre de 2026
- Pánico: 5 toques al botón de encendido ya **no llaman a emergencias**. Bloquean el teléfono,
  apagan la huella (pide PIN) y cortan datos, Wi-Fi y Bluetooth. Se restaura desde Panel.
- Panel miamiOS (nueva app): antenas con mapa, batería real, red por app, conexiones en vivo y pánico.
  La primera vez pide permiso de Bluetooth y de notificaciones. Las conexiones en vivo piden root en KernelSU.
- Seguridad miamiOS (nueva app): muro que bloquea conexiones entrantes por Wi-Fi, vigía que avisa
  cambios del sistema, sin ssh.
- Termux de sistema: tras actualizar se instalan solos Termux, Termux:API, Termux:Boot y KernelSU-Next.
  Si ya los tienes, no se tocan. Al abrir Termux se bajan solos claude y agy con suma verificada.
  Nadie tiene root hasta que lo des en KernelSU-Next.
- Nodo Meshtastic virtual, solo MQTT, conectado a Mesh Chile (mqtt.meshchile.cl, msh/CL).
  Vive solo mientras Termux está abierto. No trae usuario ni clave del broker: se configuran en el teléfono.
- Fallos miamiOS sube todos los reportes por internet y avisa cuando la pantalla táctil se traba.

## 1.6 — 7 de noviembre de 2026
- Arreglo para los cortes de música y video, y para el Bluetooth que saltaba al parlante: "Hey Google"
  agotaba las sesiones de detección de voz y el sistema reiniciaba el audio una y otra vez.
- Fallos miamiOS ahora funciona: antes se caía al arrancar y no podía leer los fallos del sistema.
- Fallos también anota cuando el teléfono va lento: cuadros que no alcanzan los 120 Hz por app,
  memoria, CPU y calor. Mide una vez por hora, sin servicio residente, y deja el detalle en el teléfono.

## 1.5 — 4 de noviembre de 2026
- Reporte automático de fallos: nueva app "Fallos miamiOS". Junta las caídas, bloqueos y
  reinicios inesperados que el sistema ya guarda, les quita correos, IP, redes y nombres de apps
  de terceros, y los manda a un repo privado de GitHub. Sin servicio residente. Necesita que
  pegues una vez un token de GitHub en la app; sin él los reportes esperan en el teléfono.

## 1.4 — 4 de noviembre de 2026
- Brillo automático que aprende: con el brillo automático encendido, cada vez que mueves la barra
  queda guardado "con esta luz quiero este brillo" y la curva se recalibra (también para luces
  parecidas). Lo reciente pesa más; lo de hace meses se va olvidando. Nunca usa el modo luz solar.
  Se guarda y no se borra al apagar la pantalla ni al reiniciar.
- Más fluido y menos batería en pantalla: vuelve la caché de composición y el reposo del
  controlador de pantalla cuando nada se mueve (Motorola los traía apagados).
- Memoria: el sistema ya no manda tan rápido las apps y juegos a la memoria comprimida
  (swappiness 60 en vez de 100): menos tirones al volver a una app.
- Actualizador: ya dice miamiOS y la versión real (1.4) en vez de LineageOS 24.0; logo y textos propios.
- Seguridad: revisión completa del sistema; sin parches nuevos disponibles para miami este mes
  (el último de LineageOS para miami sigue en el boletín de octubre).

## 1.3 — 3 de noviembre de 2026
- Pantalla de bloqueo limpia: la hora queda siempre gigante, sin notificaciones encima.
  Deslizando hacia abajo aparecen completas, sin pedir clave (desbloquear sigue pidiendo PIN o huella).
- Reloj del bloqueo más grande (190 dp).
- Animación de arranque a 120 cuadros por segundo.
- Huella: arreglado el registro de huellas (permiso de la calibración del sensor).
- El canal de actualizaciones ya no vuelve a ofrecer la misma versión tras instalarla.

Ajustes que no viajan en la actualización (se cambian en Ajustes):
- Tono grafito frío: Fondo de pantalla y estilo → Colores.
- Hora sin segundos en la barra: en los ajustes de la barra de estado (reloj).
