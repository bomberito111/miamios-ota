# Publicar miamiOS 1.8 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

El repo bomberito111/miamios-ota ya existe (1.7 publicada). Paquete:
../port/salida/ota/miamiOS-1.8-miami.zip, 1,8 GB (1770155147 bytes, bajo el límite de 2 GiB), sha256 bd1fd8566af936ff07973520ffd8a7c4c1b00c39e3360604944ca5197061ddf7

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.8: notas" && git push
   gh release create 1.8 ../port/salida/ota/miamiOS-1.8-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.8" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.8" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes.
