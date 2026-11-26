# Publicar miamiOS 2.0 (borrador; correr desde ~/Desktop/miamiOS/ota-canal, solo con SÍ de Jaime)

Paquete: ../armador/trabajo/miamiOS-2.0-miami.zip, 1722998969 bytes (bajo 2 GiB),
sha256 459d20b2ee1cbaff1a5339492b2c8e6a6e24b377a393066f35ed8dc8fd212500, post-timestamp 1795732696.
Sin data descriptors; payload.bin en offset 1497 (metadata, properties y miami.json.20 coinciden).

Ojo: la release 1.8.5 sigue en Draft y miami.json termina en 1.8.4. 2.0 trae todo lo de 1.8.5,
así que el teléfono pasa directo de 1.8.4 a 2.0. Decidir aparte qué hacer con el draft 1.8.5.

0. Pegar la sección "2.0" de abajo al inicio de CAMBIOS.md (debajo de "# Cambios de miamiOS").
1. Notas y paquete (miami.json todavía no, para que el teléfono no vea una versión sin zip):
   git add CAMBIOS.md PUBLICAR-2.0.md && git commit -m "miamiOS 2.0: notas" && git push
   gh release create 2.0 ../armador/trabajo/miamiOS-2.0-miami.zip -R bomberito111/miamios-ota -t "miamiOS 2.0" -F CAMBIOS.md --latest
   Comprobar: gh release view 2.0 -R bomberito111/miamios-ota  (asset 1722998969 bytes, no Draft)
2. Recién ahí publicar al teléfono:
   mv miami.json.20 miami.json && git add miami.json && git commit -m "miamiOS 2.0" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes.

## 2.0 — 26 de noviembre de 2026
- Incluye todo lo de 1.8.5 (Diagnóstico, Señal con medidor de subida, Cámara 1.1, SOS satelital), que no alcanzó a publicarse.
- Señal rehecha al estilo nativo de Ajustes (Redes e Internet).
- Solo Starlink: nuevo modo "4G normal (datos completos)", activado de fábrica; la red Entel SpaceX se usa como 4G común, sin marcarla satelital. Se puede volver al modo satelital en Afinar.
- Si la red rechaza la conexión (por ejemplo "hay cobertura de Entel"), Panel lo muestra, limpia la red bloqueada y reintenta con esperas de 2, 5 y 15 minutos. Nueva fila "Último rechazo".
- Datos por satélite: elige qué apps usan la red satelital, con cupo de datos, y sigue funcionando en segundo plano con el ahorro de batería activo.
