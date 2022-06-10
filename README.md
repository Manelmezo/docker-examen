# docker-examen
Para empezar con el proyecto hay que primero abrir tanto la terminal como docker desktop

![](images/image1.png)

![](images/image10.png)Hay que esperar a que inicie. Una vez iniciado hay que revisar el documento del dockercompose.yml

![](images/image5.png)Ver que las configuraciones están correctas y los puertos bien establecidos. Una vez confirmado que el docker compose está bien y sus versiones son correctas, iniciamos la construcción de la imagen de la siguiente manera.

![](images/image7.png)

Con este comando empezará a montarse la imagen y no debería dar ningún error![](images/image6.png)

Ahora comprobemos que de verdad se ha montado correctamente. Primero entraremos en localhost8081 que es el de php y vemos que va perfectamente

![](images/image16.png)

Iniciamos sesión en el usuario ![](images/image12.png)Y confirmamos que la base de datos se ha formado correctamente.

Ahora vamos a visualizar la página web con el ![](images/image18.png) Recordar poner el mismo nombre del archivo

![](images/image17.png)Y vemos que se visualiza correctamente. Al entrar pero, sale el siguiente error![](images/image4.png)

Para arreglarlo hay que ir a php de nuevo y crear una nueva tabla de la siguiente forma

![](images/image11.png)

![](images/image3.png)

Y darle a guardar tras poner esos datos

![](images/image20.png)Ahora funciona (nota, no poner un correo electrónico entero, sino sale el siguiente mensaje![](images/image15.png))

![](images/image13.png)Comprobamos que se ha generado correctamente.

Apagamos la imagen y lo subimos a docker. Para apagarlo hacemos lo siguiente![](images/image19.png)

Y se cerrará solo sin ningún problema![](images/image9.png)

Ahora solo falta subir el proyecto a DockerHub, para hacerlo debemos realizar lo siguiente

Ponemos el comando docker build -t (nombreusuario/nombreimagen)

![](images/image21.png)

![](images/image14.png)Una vez realizado el docker build, debería salir el FINISHED ese blanco indicando que todo ha ido bien. Ahora solo faltaría el push y lo haremos de la siguiente manera.

![](images/image2.png)

docker push (nombreusuario/nombreimagen)

Y con eso ha finalizado de subirse al dockerhub ![](images/image8.png)

Enlace al dockerhub donde se puede descargar la imagen:

[https://hub.docker.com/repository/docker/manelmezo/examen-docker](https://www.google.com/url?q=https://hub.docker.com/repository/docker/manelmezo/examen-docker&sa=D&source=editors&ust=1654882181106876&usg=AOvVaw2owfbC_tp8s61cy7tqHGiu)
