
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

<h2>Configuración mecánica con ejes X e Y aislados</h2>
<p>El acortamiento del eje Y no fue suficiente para evitar las oscilacines, en parte porque los deslizadores de las impresoras no estan hechos para soportar peso y además que no son de lata calidad. Son realizados con bujes de cobre que se deslizan sobre una barra de metal y eso trae fricciones y desgastes. Además, el sistema de trasmisión es por cintas dentadas de goma que funcina similar a los sitemas de polea y correa simples. Por este motivo, se decidió adoptar una configuración de estructura con los ejes X e Y aislados. para lograr esto, el eje X mueve una bandeja que soporta el objeto que se va a grabar y el eje Y se coloca sobre un puente fijo y mueve solo al cabezal emisor del Laser. Se colocó el "cerebro" del CNC dentro de una caja metálica para que este protegido y se instaló correctamente el driver del emisor laser.</p>
<img width="360" alt="20190523 estructura v4 con laser b" src="https://github.com/user-attachments/assets/e1c51f7c-9ac5-4e98-af9a-16482f874dd9" /> 
<img width="360" alt="20190523 estructura v4 con laser" src="https://github.com/user-attachments/assets/647dd309-2831-4014-a854-6dd6b65f8a2c" />

<h2>Terminación de la estructura mecánica de la máquina</h2>
<p>Con el sistema de ejes aislados se lograron eliminar las oscilaciones y se pudo verificar una mejora en la calidad del grabado. Entonces se procedió a terminar la estructura mecánica colocando los protectores contra la luz laser, colocando las tapas metálicas que protegen los circuitos, se colocaron los interruptores de final de carrera en los ejes X e Y, se colocaron los sujetadores en la bandeja  que soporta los objetos que se graban, se fijó la fuente de alimentación y se colocó un sistema de extracció de humos. Finalmente la máquina CNC quedó así:</p>
<img height="454" alt="20200210 estructura v5 con final de carrera y protector b" src="https://github.com/user-attachments/assets/7b61bca2-ae49-42c0-aac7-9031d797296e" /> 
<img height="454" alt="20200210 estructura v5 con final de carrera y protector" src="https://github.com/user-attachments/assets/156acf31-b4ea-492f-bcef-b80d1513d124" />

<h2>Resultados</h2>
<p>Con la máquina CNC terminada, se procedió a realizar pruebas de grabado con diferentes materiales entre los cuales se incluyen distintos tipos de maderas, acrílico rojo, cartulina, papel, tela de mezclilla... </p>
<img height="300" alt="resultado1" src="https://github.com/user-attachments/assets/b4c3f44f-0f15-4d3c-9724-ba4e6897e9b6" />
<img height="300" alt="resultado2" src="https://github.com/user-attachments/assets/fc456e62-5f50-4ec0-bc10-cae113bf3c77" />
<br>
<img width="300" alt="resultado3" src="https://github.com/user-attachments/assets/6ccc819e-8da9-424e-a4e3-aafef39e09c8" />
<img width="300" alt="resultado4" src="https://github.com/user-attachments/assets/96acb5ac-5381-41d0-9575-7e1ad2fdf739" />

<br>
<img height="300" alt="resultado6" src="https://github.com/user-attachments/assets/7a848fab-dd7f-4888-b246-a1862f55ba16" />  
<img height="300" alt="resultado7" src="https://github.com/user-attachments/assets/77504350-77c7-4054-b5d0-3d23bd9bea3f" />
<br>
<img height="300" alt="resultado8" src="https://github.com/user-attachments/assets/60123b3b-1578-4386-bd8b-691f5e68eea5" />
<img height="300" alt="resultado5" src="https://github.com/user-attachments/assets/1774ca7d-f535-4c40-8674-536ed9cb70ad" />

<br><br>
La Habana, Cuba, 2018 - 2020















