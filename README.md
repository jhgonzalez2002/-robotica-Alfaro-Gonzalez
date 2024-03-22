# -robotica-Alfaro-Gonzalez

Descripcion de la solucion:

Para el desarrollo de esta practica en principio se hizo el diseño de la herramienta basado en el acople que tiene el robot como se ve en el archivo adjunto de diseño de herramienta, luego de esto se creo la estacion de trabajo y se creo la herramienta con un sistema coordenado en la punta que luego se coloco como harramienta del robot, luego de esto se calibro la herramienta con el robot real y se pusieron los datos en robot studio, ya con esto se hizo el diseño de un objeto inclinado y de un workobject con el logo a dibujar (En nuestro caso el logo de windows con las iniciales JJ al final) se acomodo el workobject sobre la superficie inclinada y se re crearon las trayectorias punto a punto levantando la herramienta entre cada parte del logo para luego volver a la posicion de home. luego de esto se hizo la sincronizacin con RAPID y se llamo la trayectoria para realizar las primeras pruebas, ya despues de ver que las trayectorias funcionaban tanto en la simulacion como en el robot, se acomodo el WorkObject en el suelo para obtener la segunda trayectoria, ya teniendo ambas trayectorias funcionando por medio de la funcion WAITDI se configuraron las dos entradas digitales para iniciar la escritura a o grados y luego otra para ir a posicion de mantenimiento y tambien se uso la funcion SETDO para prender y apagar las salidas digitales segun el estado del robot como se ve en los videos tanto de simulacion como de el robot real.

Descripcion de funciones:

1.MoveL: se trata de un movimiento que debe ser en linea recta entre dos puntos, se uso para los movimientos de escritura del logo 
2.MoveJ: hace que el robot se mueva de un punto a otro sin la necesidad de ser una linea recta, la cual usamos para realizar los movimientos de levantamiento y posicionamiento de herramienta
3.WaitDI: se revisa si una entrada digital especifica esta activa y en base a eso se realizara una accion, si no simplemente se saltara esa orden del codigo
4.SETDO: se establece el estado de una salida digital entre valores de 1 y 0 es decir encendido o apagado
