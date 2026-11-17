# Publicar miamiOS 1.8.3 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

Paquete: ../port/salida/ota/miamiOS-1.8.3-miami.zip, 1,77 GB (1766675547 bytes, bajo el límite de 2 GiB),
sha256 777bacac2d729ddc5b8549426f063b48bd6119db3c8cd641abf5efdf0e4e6fcb

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.8.3: notas" && git push
   gh release create 1.8.3 ../port/salida/ota/miamiOS-1.8.3-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.8.3" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.8.3" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes. Pruebas: ../port/versiones/1.8.3/PRUEBAS.md
