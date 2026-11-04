# miamiOS — canal de actualizaciones

Canal OTA de miamiOS para Motorola edge 30 neo (`miami`). El Updater del teléfono lee
`miami.json` de este repositorio y baja el paquete desde Releases.

- Paquetes firmados con la clave de miamiOS; el teléfono rechaza cualquier otro.
- Instalación A/B: se escribe en el otro slot sin borrar datos. Si no arranca, vuelve solo al anterior.
- Cambios de cada versión: [CAMBIOS.md](CAMBIOS.md).
