# Publicar miamiOS 1.7 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

El repo bomberito111/miamios-ota ya existe (1.6 publicada). Paquete:
../port/salida/ota/miamiOS-1.7-miami.zip, 1,8 GB (1795247880 bytes, bajo el límite de 2 GiB), sha256 efeb66f3c9e536091f75e261d1114374d10d0c31b866736a61c038efc754dc8c

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.7: notas" && git push
   gh release create 1.7 ../port/salida/ota/miamiOS-1.7-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.7" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.7" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes.
