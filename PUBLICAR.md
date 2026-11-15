# Publicar miamiOS 1.8.2 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

Paquete: ../port/salida/ota/miamiOS-1.8.2-miami.zip, 1,74 GB (1739684007 bytes, bajo el límite de 2 GiB),
sha256 3be63a1ccd22581940421309dd4fefc212efd875e93b5ec5fb0c86bdda0c2321

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.8.2: notas" && git push
   gh release create 1.8.2 ../port/salida/ota/miamiOS-1.8.2-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.8.2" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.8.2" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes. Pruebas: ../port/versiones/1.8.2/PRUEBAS.md
