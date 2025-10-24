
<h1>CNC Laser 15W con Arduino NANO</h1>

<h2>Experimento con puerto paralelo del PC</h2>
<p>Con el objetivo de crear una máquina CNC para grabar sobre madera, plásticos y materiales blandos, para construir y comercializar artesanías, se empezó a experimentar con el puerto paralelo LPT1 del PC de escritorio. Se lograron recuperar motores PAP (paso a paso) de impresoras viejas y el carro y carril deslizante de algunas viejas impresoras de cinta. Con ello se construyó una estructura mecánica para mover en los ejes X e Y.</p>
<img width="416" alt="20181106_estructura v1" src="https://github.com/user-attachments/assets/c4f99e0a-94a8-42bb-99f0-3f10297a9356" />

<h2>Compra del Arduino NANO y placa base con drivers POLOLU</h2>
<p>Utilizar el puerto paralelo del PC permitió verificar el funcionamiento de los motores PAP y los sistemas deslizantes de las impresoras que se emplearon en la estructura de la máquina CNC, pero hacía muy complejo la implementación del software de control y la construcción de los drivers para motores PAP bipolares, por lo que se decidió utilizar una placa de Arduino NANO con su respectiva Shield y Drivers POLOLU para el control de motores bipolares. Como software se decidió utilizar el software libre GRBL que es una librería C++ que con una pequeña modificación se instala en el Arduino NANO y lo convierte en el cerebro de la CNC. Así el Arduino NANO puede recibir los códigos G por el puerto USB. Así fue posible instalar un marcador como herramienta en el CNC y probar el software haciendo un dibujo en papel. Se pudo apreciar que la estructura no era suficientemente estable y oscilaba.</p>
<img width="360" alt="20190516 arduino nano con shield y drivers pololu" src="https://github.com/user-attachments/assets/6d623867-f4f1-43f5-9541-e20fff5340b1" /> 
<img height="360" alt="resultado prueba 2" src="https://github.com/user-attachments/assets/f41684db-ebd7-465f-b153-2e2f72a2c1d8" />

<p>Luego se probó tambien agregar el tercer eje Z a la máquina CNC utilizando un deslizador de impresora al que se le acortó la longitud. Con las pruebas realizadas se pudo detectar que las configuraciones mecánicas con ejes X, Y y luego Z de la estructura no era muy sólida y permitían oscilaciones que deterioraban la precisión del trabajo.</p>
<img width="432" alt="ejeY 3" src="https://github.com/user-attachments/assets/4809ed81-cac6-4f55-95d9-c6b3107781a2" />
<img height="340" alt="20190127 estructura v2" src="https://github.com/user-attachments/assets/463cd4f8-a1b9-48cc-b37c-306f12204397" />

<h2>Compra del emisor laser</h2>
<p>Una vez que ya era seguro el funcionamiento del software, se procedió a comprar un emisor LASER de 15 W de potencia para trabajar con madera, plásticos y materiales blandos. Para evitar las oscilaciones mecánicas se regresó a la configuración de eje X e Y, pero esta vez se utilizó un eje Y corto para evitar la soscilaciones al final del eje.</p>
<img width="350" alt="laser 15w 12v" src="https://github.com/user-attachments/assets/fc947720-6d02-41ed-a349-30e707dd7d8e" />
<img height="380" alt="20190516 estructura v3 con laser" src="https://github.com/user-attachments/assets/d1a558e5-9c81-4c19-9dac-6d24768b7f1f" />


Primer sistema mecánico con eje Y sobre eje X

Acortamiento del eje Y para evitar vibraciones

Segundo sistema mecánico aislando el eje Y del eje X para evitar vibraciones

Mejoras finales al sistema y terminación

Resultados






Modificado para que funcione con Arduino NANO y el Shield para CNC con NANO.

Modificaciones:

1 - Cambio en los pines que controlan los drivers de los motores.
2 - El ciclo de Homing para eliminar el movimiento en el eje Z que no se utiliza.








