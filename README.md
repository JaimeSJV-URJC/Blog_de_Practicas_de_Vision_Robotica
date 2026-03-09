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

## Estructura de la solución
