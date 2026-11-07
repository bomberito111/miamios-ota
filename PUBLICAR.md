# Publicar miamiOS 1.6 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

El repo bomberito111/miamios-ota ya existe (1.5 publicada). Paquete:
../port/salida/ota/miamiOS-1.6-miami.zip, 1,7 GB, sha256 fc4ef1fcacd3277ebe81e45612486c12223d20d8ea56a5d0705f1a5eda080b69

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.6: notas" && git push
   gh release create 1.6 ../port/salida/ota/miamiOS-1.6-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.6" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.6" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes.
