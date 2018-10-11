# Taller de Santa Whoops

Este es un pequeño tutorial de como convertir un dron Eachine E11c o JJRC H67 en un Santa Whoop, es decir, un micro dron de 65mm con FPV para volar en interior (y si no hace viento también en exterior) y con un firmware libre, [NFE Silverware](https://github.com/NotFastEnuf/NFE_Silverware). El coste total suele ser <20€.

<p align="center"><img src="images/portada.png" height="400px" align = "center"></p>

## Materiales

 - Drone Eachine E11c o JJRC H67 [link](https://www.xt-xinte.com/JJRC-H67-Flying-Santa-Claus-w-Christmas-Songs-RC-Quadcopter-Drone-Headless-Mode-Toys-RTF-for-Kids-Best-Gift-VS-H36-E011C-E010-p410672.html)
 - Cámara LST-S2+ [link](https://www.xt-xinte.com/FPV-AIO-Micro-Camera-5-8G-25MW-40CH-800TVL-Transmitter-LST-S2-FPV-Camera-w-OSD-p497464.html)
 - Canopy BetaFPV (opcional) [link](https://www.amazon.es/BETAFPV-Whoop-Plastic-Canopy-Black/dp/B07D7XL5NK)
 - Programador ST-Link V2 [link](https://es.aliexpress.com/store/product/1PCS-ST-LINK-Stlink-ST-Link-V2-Mini-STM8-STM32-Simulator-Download-Programmer-Programming-With-Cover/1095279_32792513237.html)

NOTA: Los links de compra son orientativos. En Xt-Xinte recordad que existe un cupón de 5$ cada vez que creas una cuenta, por lo que se recomienda pedir cada artículo desde diferentes cuentas.

## Hardware

El dron según sale de la caja tiene este aspecto. Quizás te preguntarás por qué se ha elegido un dron Papa Noel para el tutorial, existiendo otros drones en paginas chinas similares y menos horteras. Resulta que este modelo a parte del muñeco de Papa Noel lleva un buzzer bastante grande con el que hace sonar villancicos mientras vuela. Por culpa del peso de las dos cosas juntas, el fabricante ha decidido meter motores de 7mm, que son más grandes que los que suelen montar el resto de drones de este tamaño, 6mm.

<p align="center"><img src="images/deserie.jpg" height="400px" align = "center"></p>

 La carcasa de Lego se quita solo con dos pestañas, y permite ver los cables del buzzer. Hay que eliminar el buzzer para quitar peso en el dron y hacerlo más ágil (además la turra de los villancicos es impresionante). Se recomienda desoldar los cables y dejar los pads limpios, aunque también pueden cortarse a ras con unos alicates.

<p align="center"><img src="images/cablesbuzzer.jpg" height="400px" align = "center"></p>

Por la parte de abajo el buzzer está sujeto con pegamento. Para acceder a él hay que quitar los tornillos de la PCB. No es necesario quitar los conectores de los motores, pero conviene tener cuidado con ellos, ya que son muy frágiles y pueden romperse con un tirón. El buzzer se puede quitar tirando suavemente de él.

<p align="center"><img src="images/buzzer.jpg" height="400px" align = "center"></p>

Una vez hecho esto la PCB queda limpia. En la foto además podemos ver los pines en los que más adelante soldaremos la cámara, los que están al lado de la antena. Puede utilizarse cualquier par de pines que estén conectados directamente a la batería.

<p align="center"><img src="images/pcb.jpg" height="400px" align = "center"></p>

En este punto podemos aprovechar para ver cómo queda el canopy. A veces hay que ajustar un poco los agujeros de los tornillos laterales para que encajen con el frame, pero por lo general vienen bastante bien ajustados.

<p align="center"><img src="images/canopies.png" height="400px" align = "center"></p>

Los tornillos para el canopy deben ser pequeños y se recomienda reciclarlos de cualquier chatarra electrónica que tengas en casa.

<p align="center"><img src="images/canopysincam.jpg" height="400px" align = "center"></p>

Hecho esto pasamos a la cámara. Se ha montado una LST-S2+ porque estaba en oferta en el momento de escribir este tutorial, pero cualquier cámara FPV AIO (es decir, con VTX integrado) de tamaño micro puede valer para este dron. Este modelo tiene capacidad para utilizar OSD con los cables amarillo y blanco, pero como nuestro dron no lo soporta los dejaremos sueltos. También pueden cortarse directamente.

<p align="center"><img src="images/camara.jpg" height="400px" align = "center"></p>

En el conector de tres pines soldamos los cables de la cámara, poniendo el rojo en el + y el negro en el -. El pin SX lo dejaremos libre.

<p align="center"><img src="images/camsoldada.jpg" height="400px" align = "center"></p>

En este punto pegamos la cámara al canopy con pegamento termofusible. Hay que tener cuidado de no calentar mucho el plástico del canopy, porque puede deformarse o incluso derretirse. El dron finalmente queda como se ve en la siguiente foto.

<p align="center"><img src="images/final.jpg" height="400px" align = "center"></p>

Opcionalmente, si quieres utilizar baterías en formato stick como las que utilizan otro Whoops puedes hacerle un corte al frame utilizando un cutter. El plástico es muy fácil de cortar y conviene que la abertura quede redondeada y ajustada a la batería para evitar que se raje.

<p align="center"><img src="images/cortelipos.jpg" height="400px" align = "center"></p>

Para afianzar la batería al frame puede utilizarse una goma pequeña sujeta a los pines laterales del frame. ***TODO: También hace falta soldarle un cable con conector, pero ahora mismo no tengo fotos de cómo lo puse***

<p align="center"><img src="images/gao.jpg" height="400px" align = "center"></p>

## Firmware
