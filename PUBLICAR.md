# Publicar miamiOS 1.8.1 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

Paquete: ../port/salida/ota/miamiOS-1.8.1-miami.zip, 1,78 GB (1782614342 bytes, bajo el límite de 2 GiB),
sha256 cfe04389d50485de629128c7e75e120530d53a7f55a8f9b88efd88fb26e171a7

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.8.1: notas" && git push
   gh release create 1.8.1 ../port/salida/ota/miamiOS-1.8.1-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.8.1" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.8.1" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes. Pruebas: ../port/versiones/1.8.1/PRUEBAS.md
