# Tutorial Simplify3D 3.1.1

Esto no es un tutorial exhaustivo de Simplify3D, es más una mera guía de cuales son las opciones más importantes y los botones más comunes que usaremos el día a día. También hay opciones que no he usado nunca y que investigaré para describirlas.

## Pantalla principal

La pantalla principal tiene 4 zonas importantes.

Previsualización:

![](https://puu.sh/tflD6/baa05a60df.png)

Muy importante los ejes de coordenadas. Si miramos la imagen anterior, están en la esquina inferior izquierda y coincide con la esquina inferior izquierda de nuestra impresora. Es importante para piezas grandes, para saber en qué posición va a salir en la impresora por si tenemos los clips para agarrar el cristal (para que no choque).

Lista de piezas:

![](https://puu.sh/tflN6/5fa3ff7492.png)

Si le damos a importar, podemos cargar todos los stl que queramos, alternativamente, podemos arrastrarlos desde el explorador a la ventana de simplify.

Procesos:

![](https://puu.sh/tflUc/d295734f1e.png)

Un proceso es la operación de filitear nuestros stl. Es donde configuramos la altura de capa, velocidad, etc etc.

En la siguiente sección veremos como _Editar configuración de proceso_.

Editar STL:

![](https://puu.sh/tfm3n/182d0d5449.png)

Para conseguir esta ventana, hacemos click en una figura en la previsualización o en el listado. Aquí podremos escalar la pieza, rotarla, moverla... También podemos hacer click en los botones de la derecha para conseguir el mismo resultado.

Como truco, si giráis un stl y se queda ahí atravesando la cama, podéis darle a CTRL+T para reiniciar su posición.

## Configurando el proceso

Antes que nada, las opciones aquí mostradas son las que uso yo para mi, siempre podréis ir cambiando las opciones a vuestro gusto y como siempre, depende de la pieza en cuestión.

![](https://puu.sh/tfmE3/f376919ddc.png)

Esta es la pantalla para editar el proceso.

La parte de arriba especifica el nombre, el perfil que estamos usando (no os mareéis mucho con el perfil, vamos a crear uno nuevo en el tutorial.

También tenemos una barrita para cambiar el porcentaje de relleno (infill). Esto se podrá cambiar en otra pestaña más detalladamente.

### Extrusor

Aquí configuraremos todo lo relacionado con el extrusor. Por defecto tendremos creado un extrusor llamado "Extruder 1" y como nuestra ANET solo tiene 1, pues no necesitamos más.

A la derecha tenemos una serie de opciones, detallaré las más importantes:

* **Índice del cabezal del extrusor** - Aquí nos saldrá una lista de posibles "hotends" y nosotros seleccionaremos el 0 que siempre coincidirá con el primer extrusor (en la informática empezamos a contar desde 0 y no desde 1).
* **Diámetro de la boquilla** - Aquí colocamos la medida del nozzle, que por defecto es 0,40.
* **Multiplicador de extrusión** - Aquí configuraremos el flow, o sea, la cantidad de plástico que echará el extrusor. Por defecto viene a 0.95 y es un buen valor. Hay que ir toqueteandolo un poco si vemos que necesitamos más (numero más grande) o menos (numero más pequeño) plástico.
* **Ancho de extrusión** - La he dejado por defecto.

Luego tenemos las opciones de control de goteo (retraction). Esto es probablemente lo más difícil de configurar de todo. Depende del color del plástico, depende del tipo de material, depende de la pieza... Yo todavía tengo problemas de retracción, así que id probando.

Retracción:

* **Distancia de retracción** - Cuanto plástico retrae.
* **Distancia adicional de reinicio** - Mucha retracción puede hacer que luego no salga lo suficiente cuando empiece a echar de nuevo. Añadiendo un valor aquí, se compensará esa pérdida.
* **Levante vertical de retracción** - También conocido como zhop. Esto levantará el extrusor (subirá la Z) tantos mm como le indiquemos cada vez que hace un movimiento donde no imprime nada.
* **Velocidad de retracción** - A qué velocidad retrae el plástico. Esto junto a la distancia de retracción, son los dos parámetros más importantes de la retracción y los más difíciles de ajustar bien.

* **Rodar al final, distancia de rodaje** - Sirve para aliviar presión después de una retracción y que no salgan "baches" en la impresión.
* **Limpiar boquilla, distancia de limpieza** - Técnicamente sirve para limpiar el nozzle al empezar una nueva vuelta. No lo he probado.

### Capa

![](https://puu.sh/tfovj/9a942be7a1.png)

Vamos a comentar los puntos más importantes aquí.

* **Altura de capa primaria** - La altura de cada capa, ya sabéis, 0.05mm, 0.1mm, 0.2mm, etc.
* **Capas sólidas superiores** - Cuantas capas superiores poner para tapar un relleno.
* **Capas de fondo sólido** - Número de capas a colocar en la base antes de empezar con el relleno.
* **Cubiertas de contorno/perímetro** - Cuantas "vueltas" darle a cada perímetro. O sea, qué grosor darle a los muros teniendo en cuenta que son múltiplo del nozzle. Si nuestro nozzle es de 0.4, 2 paredes será 0.8 de grosor en nuestros muros.

Configuraciones de primer capa:

Aquí es importante 2 aspectos, uno es la velocidad de la primera capa, un 50% está bien, nos ayuda a tirar una primera capa de calidad, y segundo la altura de la primera capa. Os pego un texto de la documentación oficial de Simplify3D traducido por mi acerca de la altura de la primera capa:

>Porcentajes por debajo del 100% reducirá la altura de la primera capa (sin cambiar la cantidad que se extruye). Por ejemplo, si introduces 7%, la altura de tu primera capa será reducida mientras que tu extrusión sigue al 100%. Otra forma de pensarlo es que el 100% de la extrusión se fuerza en un espacio del 75%. Esta reducción en altura genera presión extra y más area de superficie para la primera capa, lo cual ayudará a que la primera capa se adhiera a la cama

>En otros casos, un porcentaje superior al 100% es util. Por ejemplo, si estás imprimiendo capas muy finas, por ejemplo 0.05mm, la minima variación (o imperfección) en la cama puede resultar en una primer capa muy pobre en adherencia. Una altura de capa por encima del 100% puede ser extremadamente útil en estos casos. Muchas máquinas se benefician de usar una altura inicial de 200 o 300% para usar 0.05mm o 0.1mm. El extra grosor para la primera capa podrá absorver los pequeños defectos de la cama y proveer más superficie de contacto, lo cual ayuda en una mejor primera capa

En resumen, yo intento que la primera capa sea siempre 0.2, y voy a justando la altura para que sea así.

* Capa 0.3 -> Altura 67%
* Capa 0.2 -> Altura 100%
* Capa 0.1 -> Altura 200%
* Capa 0.05 -> Altura 400%

Puntos de inicio:

Por defecto está en *Optimiza los puntos de inicio para obtener la mas alta velocidad de impresión*. ¿Qué quiere decir esto? Que Simplify3D va a buscar un punto exacto de la pieza donde empezar una nueva capa. Vale, pero ¿qué quiere decir esto? Pues que al moverse el nozzle a ese punto para empezar, puede dejar un poquito extra de plástico, no se nota, pero cuando llevas 50 capas, es posible que veas un efecto cremallera:

![](https://puu.sh/tgmHH/52b5632563.png)

No tiene por qué pasar con una impresora bien calibrada, pero al menos sabemos la posible causa.

Existe la opción *Usa puntos de inicio aleatorios para todos los perímetros*. Con esta opción, empezará cada capa en un sitio diferente. Es más lento, pero no es apenas notable.

### Adiciones

Aquí es donde configuramos la falda, borde, balsa...

![](https://puu.sh/tgn00/0e48005322.png)

**Falda/Borde**, aquí es una sola opción para hacer lo mismo, no es como Cura que tienes dos opciones diferentes.

Si el offset es mayor a 0, cuenta como falda. Si el offset es 0, saldrá pegado a la pieza y será un borde.

Podréis poner el numero de contornos para la falda / borde. Dependiendo del tamaño, dejo un contorno o dos dependiendo del tamaño de la pieza para que así le de tiempo a regular el flujo de plástico. Para el borde, me vuelvo loco y lo mismo le dejo 14. Depende de la pieza.

Las capas de la falda, en el 99% de los casos con 1 capa está bien. Pero os dejo un truco:

> Uno de los problemas más tipicos con el ABS son los cambios de temperatura y las corrientes. Para evitar corrientes, puedes poner tantas capas de la falda como capas tenga la pieza. Con esto conseguiremos que haya una "cortina" alrededor de toda la pieza y esta nos evitará esas malditas corrientes.

**Balsa**, aquí configuraremos la balsa, la cual nos ayudará a que determinadas piezas se fijen mejor a la cama. 

Podremos configurar cuantas capas tiene, el offset, el cual nos indica cuanto va a "sobresalir" la balsa de nuestra pieza. Luego tenemos 2 valores que nos ayudará a que la balsa se quede más o menos pegada a la pieza en si.

Sinceramente, no he encontrado una configuración que haga que las balsas de Simplify3D sean faciles de despegar.

**Pilar de preparación**. Esto es para extrusores que acepten más de un filamento a la vez, así que no nos sirve. Como curiosidad, el pilar de preparación es un pilar que se crea en una esquina de la cama que sirve para limpiar el nozzle cada vez que cambia de filamento.

**Escudo de goteo**. El goteo (ooze) son los restillos de plastico que van saliendo de cuando en cuando. Si tenemos 2 extrusores, que va a ser que no, al ir cambiando de filamento, el otro puede gotear y joder la pieza. Esto crea una capa extra alrededor de la pieza que es la que se va a "tragar" todos esos goteos. Al terminar se quita super fácil y tenemos una pieza multicolor y limpia.

### Relleno

![](https://puu.sh/tgs6g/6708c72e6a.png)

Aquí es donde configuraremos el relleno (infill).

Simplify3D tiene diferentes tipos de rellenos. El más común es el *Full Honeycomb* (panel de abeja completo) o el *Rectilinear* (que es el que usa Cura). Técnicamente, el *FullHoneycomb* gasta menos plástico.

Aquí podremos configurar:

* **Extrusor del rellenado** - Pues el extrusor que se usará para relleno, elegimos el único que tenemos.
* **Patrón de rellenado interno** -  El patrón que vamos a usar para rellenar las piezas.
* **Patrón de rellenado externo** - Para hacer las capas solidas de fondo y superiores. El *rectilinear* es el clásico de siempre.
* **Porcentaje de llenado interior** - La cantidad de rellenado (infill) que queramos poner. Concuerda con lo que hemos puesto en la barrita que hay más arriba.
* **Superposición de contorno** - Con esta opción, podemos solapar el relleno con los bordes para no dejar huecos vacíos.
* **Ancho de la extrusión de rellenado** - La cantidad de plástico a echar en el relleno comparado con el borde. 100% significa que echará la misma cantidad.
* **Longitud de rellenado mínima** - Si un hueco es muy muy pequeño, no imprimirá ningún relleno. Aquí configuramos cuanto de pequeño tiene que ser para que lo ignore o si queremos que eche si o si. Yo tengo puesto que no deje ningún hueco sin rellenar.

De las otras 2 que siguen, ni idea, así que no las he tocado.

A la derecha vemos los distintos ángulos de rellenado. En el caso de la imagen, hará el relleno de 3 formas diferentes, uno en cada capa. Podemos poner si queremos que use todos esos ángulos en una misma capa.

### Soporte

![](https://puu.sh/tgsE7/afa9b5da7e.png)

Aquí configuraremos los posibles soportes.

* **Porcentaje de relleno de soporte** - La distancia entre las distintas paredes del soporte.
* **Distancia de inflación adicional** - Hace que la base del soporte sea algo más ancha (no la he probado).
* **Capas de soporte densas** - numero de capas densas (o sea, no haciendo eses como hace el soporte, si no una capa completa entre la pieza y el final del soporte. Tampoco lo he probado.
* **Porcentaje de rellenado denso** - En caso de activar la opción anterior, qué porcentaje de rellenado tendrá.
* **Imprime soporte cada** - Por si queremos imprimir soporte cada 1 capa o cada X capas. Yo siempre cada 1 capa, cada 2 capas suena muy muy raro.

Hay una sección llamada *Separación de la pieza* que se supone que es para alejar más el soporte de la pieza. Cuando pruebe actualizaré la sección.

La sección *Colocación automática* es donde tiene las opciones de cómo generará Simplify3D sus soportes. En el caso de la imagen, con una resolución de 4mm y se generará para los angulos mayores de 45 grados.

**MUY** importante es donde pone *Tipo de soporte: De la plataforma de construcción únicamente*.

¿Qué significa esto? Que solo generará soportes desde la cama. O sea, imaginad que tenéis una pieza que es una letra F. El palito de abajo de la F necesita soporte, y el de arriba también. En este caso solo generaría soporte para el palito de abajo, o sea, desde la plataforma de construcción (o sea, la cama) únicamente. Dicho de otra forma, si necesitas un soporte que se cree desde la pieza para sujetar algo más arriba, no lo hace.

Si queremos que haga esto último, necesitamos cambiar el tipo de soporte a *Normal*.

Simplify3D tiene una opción para crear soportes a mano que comentaré más adelante.

El último recuadro es como el de relleno, para que en diferentes capas lo haga diferente, pero realmente no hace falta.

### Temperatura

![](https://puu.sh/tgBDo/83391dac4f.png)

Esta es la parte más confusa sin duda de todo Simplify3D.

A la izquierda necesitamos 2 controladores de temperatura, 1 para el extrusor y otro para la cama. Si os sale un controlador solo (que creo que es así por defecto) le dais a *Agregar controlador de temperatura* y le poneis el nombre que queráis.

En la *Vista general* lo importante es:

* **Identificador de temperatura** - Lo dejáis en T0 para los dos controladores.
* **Tipo de controlador de temperatura** - Pues el de extrusor en extrusor y el de plataforma caliente pues la cama caliente.

Lo de monitorizar no lo he usado nunca, y dejamos activado el que espere a la estabilización, así no empieza a imprimir antes.

Lo importante son los *Puntos de referencia de temperatura por capa*. En Simplify3D podemos especificar qué temperatura queremos en cada capa.

En la imagen estamos diciendo, desde la capa 1 **en adelante**  quiero 200 grados. Si quisiéramos hacer una torre de temperatura que cambian los grados cada centímetro (capas a 0.2 serían 50 capas un centímetro) haríamos:

![](https://puu.sh/tgC8N/dc03ee90d0.png)

En la capa 1 en adelante, 185 grados, en la 51 en adelante, 190, etc etc. Si hubiesen 500 capas, desde la 151 se pondrá a 200 grados.

Con la cama hacemos lo mismo, desde la capa 1 en adelante pues 60 grados por ejemplo:

![](https://puu.sh/tgCbs/17b2731927.png)


### Enfriamiento

![](https://puu.sh/tgCcT/cfd0b863c7.png)

Esta es la que toco menos.

Por un lado tenemos los *Controles de ventilador de capa* que funcionan exactamente igual que los de temperatura de los que acabamos de hablar.

Aparte de eso, podemos hacer que el ventilador emita un sonido cuando cambie la velocidad (que no sé si la anet hará).

El resto de opciones las desconozco, se investigarán y se documentarán.


### G-Code

![](https://puu.sh/tgClT/dcf23df8be.png)

¿Es la sección donde añadimos gcodes a mano? Pues no.

Por un lado hay una sección de *Opciones de G-Code*. Ahí no tocar nada. Está perfecto como está y dudo que haya nunca ninguna razón para tocarlo.

En *Offsets globales de G-Code* Podemos corregir todo un gcode al vuelo. Si por ejemplo quieres que cada vez que se mueva la X, se mueva 5mm más por alguna razón, le añades un offset de 5. Por norma general, no es útil.

En *Modificar definición de máquina* Le diremos que es cartesiana de volumen rectangular, la otra opción es para las delta.

Y le damos los tamaños de los ejes. O sea, 220 x 220 x 240 como aparece en la imagen.

Desconozco si las opciones en *Modificar la configuración del firmware* hacen falta si no la tenemos conectada por USB, pero en cualquier caso, elegiremos RepRap (las prusas son RepRap) y esos baudios.


### Scripts

![](https://puu.sh/tgDcM/0a3af052ef.png)

En scripts es donde cambiamos los gcode. Tenemos 5 secciones donde podemos escribir gcodes.

* **Script inicial** - Es lo que se ejecutará antes de imprimir, es donde ponemos que queremos autolevel, que apague ventiladores (para la primera capa), que vaya a home... Muchas cosas :P
* **Script de cambio de capa** - Si queremos que haga algo cada vez que cambia de capa. Vacío por defecto.
* **Script de retracción** - Para que haga algo cada vez que hace retracción. Vacío por defecto.
* **Script de cambio de cabezal** - Ni fruta idea.
* **Script de finalización** - Aquí añadimos G-Code para apagar el extrusor, la cama, motores... Por defecto tiene buenos valores ya.

### Otro

![](https://puu.sh/tgDmd/f5c7167a8d.png)

En otro están las cosas que no encajan en otros sitios, pero igualmente importantes, sobretodo las velocidades.

* **Velocidad de impresión** - Pues la velocidad a la que queremos imprimir nuestras piezas.
* **Velocidad baja para contorno** - Cuando Simplify3D hace bordes, veréis como uno de ellos (el externo) lo hace más lento, para que de más calidad. En este caso irá a un 50% de velocidad.
* **Velocidad baja de rellenado de sólidos** - Como con el borde exterior, las primeras capas y las últimas las hará lentamente para que tengan más calidad.
* **Velocidad baja de la estructura de soporte** - Los soportes los hará a 80% de la velocidad.
* **Velocidad de movimiento de los ejes X/Y** - También conocido como velocidad de viaje en otras aplicaciones. Es la velocidad a la que se mueve la impresora cuando no está imprimiendo.
* **Velocidad de movimiento del eje Z** - La velocidad en la que sube el eje Z cuando cambia de capa.

En propiedades de filamento, lo único importante es decir que nuestro filamento es de 1.75.

Las opciones de *Puenteo* parecen interesante pero las desconozco. Las investigaré.


### Avanzado

![](https://puu.sh/tgEiU/374b488488.png)

Muchas opciones aquí, pero no son muy interesantes y no van a cambiar entre impresiones. Las investigaré para ver si hay algún cambio decente aquí.

## Soportes personalizados

ESTO es lo que hace simplify bueno. Si hacemos click en el menú *Herramientas -> Personalizar estructuras de soporte* nos saldrá la siguiente ventana:

![](https://puu.sh/tgIDW/bca14a353b.png)

La primera sección es para soportes automáticos. Si le damos a *Generar soportes automáticos* nos saldrán los soportes en la previsualización. Aquí podremos si queremos ajustar el *ángulo máximo de colgante* (que también podemos configurar en el proceso). Algunos recomiendan 40 grados, otros 45.

Lo bonito es que una vez generemos los soportes automáticos, podemos *agregar nuevas estructuras de soporte* o *quitar soportes existentes*. O sea, podemos agregar un soporte donde nos de la gana o quitar alguno que pensemos que sobra y no nos va a aportar nada.

## ¡Preparar para imprimir!

Nuestra pieza está lista! Pues abajo a la izquierda hay un botón que pone *¡Preparar para imprimir!*

Si le damos veremos:

![](https://puu.sh/tgJ0w/daffbce411.png)

Aquí nos engañará diciendo cuanto tardará en imprimir (realmente no engaña, pero no sabe cómo tenemos configurado nuestro firmware que puede potencialmente reducir la velocidad de impresión).

Nos dirá cuanto cuesta el material de la pieza, cuantos metros es, el peso...

Lo importante aquí es poder darle a imprimir o guardar el .gcode a un fichero para meterlo en la SD o lanzarlo desde otro programa como octoprint.

Como curiosidad, podemos ver una previsualización de las capas y manejarla con los siguientes controles:

![](https://puu.sh/tgJ7O/e1791e97ba.png)
