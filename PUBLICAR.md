# Publicar miamiOS 1.4 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

El repo bomberito111/miamios-ota ya existe (1.3 publicada). Paquete:
../port/salida/ota/miamiOS-1.4-miami.zip, 1,7 GB, sha256 f5eb3df4b796cc48aed8a6f601989a94f9ced94a79fa5ea45fd248095d6a4074

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.4: notas" && git push
   gh release create 1.4 ../port/salida/ota/miamiOS-1.4-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.4" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.4" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes.
