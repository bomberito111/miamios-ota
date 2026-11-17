# Publicar miamiOS 1.8.4 (correr en este orden, desde ~/Desktop/miamiOS/ota-canal)

Paquete: ../port/salida/ota/miamiOS-1.8.4-miami.zip, 1,72 GB (1724258815 bytes, bajo el límite de 2 GiB),
sha256 29c0a51b9676500c3059c85b1968a883d22aebff386d7be6ef681ecb1dbc954a

1. Subir el paquete y las notas (miami.json todavía no, para que el teléfono no vea una versión
   cuyo zip aún no existe; demora):
   git add CAMBIOS.md PUBLICAR.md && git commit -m "miamiOS 1.8.4: notas" && git push
   gh release create 1.8.4 ../port/salida/ota/miamiOS-1.8.4-miami.zip -R bomberito111/miamios-ota -t "miamiOS 1.8.4" -F CAMBIOS.md
2. Recién ahí publicar la versión al teléfono:
   git add miami.json && git commit -m "miamiOS 1.8.4" && git push

En el teléfono: Ajustes → Sistema → Actualizaciones → buscar. Se instala en el otro slot; si no
arranca, vuelve solo a la versión de antes. Pruebas: ../port/versiones/1.8.4/PRUEBAS.md
