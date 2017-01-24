#Pestaña *"Print Settings"*
En esta pestaña nos encontramos varios apartados que vamos a ir viendo individualmente:

##Layers and Perimeters

En este primer apartado nos encontramos las opciones para ajustar las capas, la calidad de la impresión y varios ajustes más, vamos a verlos en detalle: 

![ ](https://puu.sh/tys8m/7ad647ce49.png
  "Layers and Perimeters")
  
**Layer Height:** Esté parámetro nos permite ajustar la altura de capa, a más altura de capa menor tiempo de impresión y menor gasto de material, no es recomendable usar una altura de capa superior al 85% ó 90% del diámetro del nozzle, así las nuevas capas tendrán una buena adherencia entre ellas.

**First Layer Height:** Este parámetro indica la altura de la primera capa de impresión, recomiendo dejarla en el 100%, o se puede introducir un valor entre 90-100%.

**Perimeters:** Este parámetro define la cantidad de lineas horizontales que tendrá la pieza(Número de vueltas que tendrá la pared).
Por defecto 3 está bien, si se quiere tener más grosor se puede aumentar a 4.

**Spiral Vase:** Es un modo "Jarrón", imprime una base, después imprime la figura con una sola capa de perímetro, y en vez de subir el eje Z en cada capa, lo sube poco a poco y suavemente, logrando una mejor definición de la pieza y con menos costuras en la pieza.

**Horizontal Shells:** Es el numero de capas rellenas completamente en la parte superior e inferior de la pieza,con 3 es suficiente, pero si se desea ampliar se puede ampliar a 4-5 capas arriba y abajo(Top y Bottom respectivamente).

**Extra perimeters if needed:** Esta opción crea perímetros extra en zonas que el programa cree conveniente.

**Avoid crossing perimeters:** Evita los perímetros que llegan a cruzarse.

**Detect Thin Walls:** Detecta las zonas más finas y ajusta la impresión para rellenarlos correctamente.

**Detect Bridging Perimeters:** Esta opción detecta los perímetros que están en el aire(puente).

**Seam Position:** Ajusta la posición de los inicios de cada capa,hay tres opciones:Alineado(Aligned)el más cercano(Nearest), y aleatorio(Random).Yo  personalmente recomiendo el aleatorio porque deja las costuras más disimuladas al estar distribuidas por el contorno de la pieza.

**External Perimeters First:** Con esta opción marcada el programa realizará el contorno primero y el relleno después(Esto es útil en determinadas ocasiones para no dejar marcado el relleno en la parte exterior de la pieza).

