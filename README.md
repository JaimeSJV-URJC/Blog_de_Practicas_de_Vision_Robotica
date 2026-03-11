# Blog de Prácticas de Visión Robotica de Jaime San José Villar
## FollowLine
### 25/02/2026
Primeros pasos de la práctica. Puesto en funcionamiento el docker y aprendido como se acelera y se gira el vehiculo.
### 1/03/2026 
Mascara para detectar la linea en imagen binaria. Como no consigo extraer la imagen guardandola desde unibotics me guiaré por sus dimensiones para realizar la busqueda de donde se encuentra la linea en un momento dado.
### 4/03/2026 
Primera verisón funcional con controlador proporcional. Oscila en las curvas. Tiempo de vuelta: 150.36 segundos 
### 8/03/2026 
Implementado controlador PD. Mejores tiempos cerca del minuto. También implemento velocidades diferentes para curva y recta. Cambio del aspecto del blog para mayor legibilidad.
### 9/03/2026
Ajustando varibles para intentar mejorar marcas. El mejor tiempo conseguido a sido 62,65 segundos en el simple circuit, pero el controlador es inestable por lo que he reducido las velocidades para probar los distintos circuitos.

![61 65seg](https://github.com/user-attachments/assets/450a15c0-d115-4a48-ac64-9d2d3125df64)

Nurburgring me da problemas a la salida. No se porque pero nada más empezar el coche se dispara para la izquierda y no se recupera. Esto da un caso de uso al recuperador más complejo si lo llego a implementar mañana. En Montmelo me dan problemas las ultimas curvas. Probar el circuito es una tortura dada la lentitud y el hecho de que solo falla en el ultimo cuarto del circuto. A duras penas, el coche ha completado una vuelta de Montmelo, pero no es repetible.

<img width="1021" height="367" alt="imagen_2026-03-09_204621746" src="https://github.com/user-attachments/assets/756879c7-fb30-45c2-add5-5fee052b0677" />

### 10/03/2026
Otra vuelta completada en Montmelo. Si el controlador va con velocidad unica parece capaz de terminar la vuelta de forma consistente. Hay algo en las ultimas curvas, algún tipo de variación inperceptible al ojo humano, que hace fallar el controlador. Me es claro empiricamente al ver funcionar al coche que no se comporta de la misma manera en las ultimas curvas de Montmelo como en el resto del circuito.

![Monrmelo2](https://github.com/user-attachments/assets/ff8a59c5-d3df-422f-a999-d4b656d1e1db)

También he estado probando un frenado brusco al entrar en curva para reducir el tiempo en el circuito simple, pero sin buenos resultados. Parece que me voy a quedar con un tiempo real de algo más de un minuto.

https://github.com/user-attachments/assets/976574b9-46c7-4dbe-b0f3-217b6eedc9c6

https://github.com/user-attachments/assets/f94e9f7e-2edd-4c58-a98d-8c4c3bd13e9d

Es obvio que aunque se completa la vuelta al circuito simple en un tiempo razonable hay margen de mejora para el controlador. 

## Estructura de la solución
Para realizar FollowLine he probado controladores P y PD, siendo la implementación final PD. El controlador utiliza una velocidad varible para rectas y curvas determinada por un punto superior en la visualización en la linea al punto utilizado para controlar el giro. Utilizo este punto superior para que la curva sea detectada antes, y así poder reducir la velocidad a tiempo para tomar la curva sin perder la linea. Al probar controladores he obtenido tiempos inferiores al de la solución final, controladores con menor oscilación que eran también más lentos. Con la solución pretendo tener un equilibrio entre velocidad y reducción de oscilación. 

## Recontrucción 3D
### 11/03/2026
Primeros pasos en clase. Entendiendo lo que es necesario para realizar el ejercicio y las funciones especificas de camara y dibujo.
