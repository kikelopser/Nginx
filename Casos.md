# Casos practicos
## :one: Versión de Nginx instalado.
```
nginx -v
```
![4](https://github.com/kikelopser/Nginx/blob/main/Nginx/4.PNG)

## :two: Ficheros de configuración.
Fichero principal
```
/etc/nginx/nginx.conf
```
![5](https://github.com/kikelopser/Nginx/blob/main/Nginx/5.PNG)

HTML por defecto
```
/var/www/html/index.nginx-debian.html  
```
![6](https://github.com/kikelopser/Nginx/blob/main/Nginx/6.PNG)

## :three: Modificamos la página web que lanza por defecto.
Modificamos en /var/www/html/index.html
![7](https://github.com/kikelopser/Nginx/blob/main/Nginx/7.PNG)
![8](https://github.com/kikelopser/Nginx/blob/main/Nginx/8.PNG)

Reiniciamos el servicio
```
systemctl restart nginx.service
```
![9](https://github.com/kikelopser/Nginx/blob/main/Nginx/9.PNG)

Comprobamos los cambios
![10](https://github.com/kikelopser/Nginx/blob/main/Nginx/10.PNG)

## :four: Balanceo de carga HTTPS Nginx

Queremos que nuestro servidor web ofrezca balanceo de carga desde https a dos sitios web que tengan también https.

Para ello necesitaremos 3 máquinas:

- Una con una web HTTPS.
- Otra con otra web HTTPS.
- Una tercera que haga el balanceo de carga entre las dos anteriores.

## Maquina 1
1.- Modificamos una maquina Debian 11 con Nginx instalado y modificamos su pagina por defecto

![11](https://github.com/kikelopser/Nginx/blob/main/Nginx/11.PNG)

```
systemctl restart nginx.service
```
2.- Le añadimos una red interna y le configuramos red estatica

![12](https://github.com/kikelopser/Nginx/blob/main/Nginx/12.PNG)
![13](https://github.com/kikelopser/Nginx/blob/main/Nginx/13.PNG)
![14](https://github.com/kikelopser/Nginx/blob/main/Nginx/14.PNG)

3.- Añadimos el host en el fichero de configuracion

![15](https://github.com/kikelopser/Nginx/blob/main/Nginx/15.PNG)

4.- Comprobamos que funcione

![16](https://github.com/kikelopser/Nginx/blob/main/Nginx/16.PNG)

## Maquina 2
1.- Añadimos una red interna a una Maquina con Debian 11 y le añadimos IP estatica

![17](https://github.com/kikelopser/Nginx/blob/main/Nginx/17.PNG)
![18](https://github.com/kikelopser/Nginx/blob/main/Nginx/18.PNG)

2.- Instalamos el servicio Nginx

![19](https://github.com/kikelopser/Nginx/blob/main/Nginx/19.PNG)

3.- Modificamos la pagina por defecto

![20](https://github.com/kikelopser/Nginx/blob/main/Nginx/20.PNG)

4.- Añadimos el host en el fichero de configuracion

![21](https://github.com/kikelopser/Nginx/blob/main/Nginx/21.PNG)

5.- Comprobamos el funcionamiento

![22](https://github.com/kikelopser/Nginx/blob/main/Nginx/22.PNG)

6.- Comprobamos el funcionamiento de la pagina modificada en la Maquina 1

![23](https://github.com/kikelopser/Nginx/blob/main/Nginx/23.PNG)

## Maquina 3
## Servidor de Balanceo
1.- Añadimos una red interna a una Maquina con Debian 11 y le añadimos IP estatica

![24](https://github.com/kikelopser/Nginx/blob/main/Nginx/24.PNG)
![25](https://github.com/kikelopser/Nginx/blob/main/Nginx/25.PNG)
![26](https://github.com/kikelopser/Nginx/blob/main/Nginx/26.PNG)

2.- Instalamos el servicio Nginx

![27](https://github.com/kikelopser/Nginx/blob/main/Nginx/27.PNG)

3.- Borramos el siguiente archivo y creamos uno nuevo

![28](https://github.com/kikelopser/Nginx/blob/main/Nginx/28.PNG)
![29](https://github.com/kikelopser/Nginx/blob/main/Nginx/29.PNG)

Comprobamos el fichero

![30](https://github.com/kikelopser/Nginx/blob/main/Nginx/30.PNG)

4.- Añadimos el host en el fichero de configuracion

![31](https://github.com/kikelopser/Nginx/blob/main/Nginx/31.PNG)

5.- Reiniciamos el servicio Nginx
```
systemctl restart nginx.service
```

4.- Añadimos el host en el fichero de configuracion

![32](https://github.com/kikelopser/Nginx/blob/main/Nginx/32.PNG)

5.- Hacemos las comprobaciones

![33](https://github.com/kikelopser/Nginx/blob/main/Nginx/33.PNG)

6.- Vamos a crear un certificado SSL. Creamos el siguiente directorio y ejecutamos el siguiente comando

![34](https://github.com/kikelopser/Nginx/blob/main/Nginx/34.PNG)

7.- Modificamos el fichero de balanceo

![35](https://github.com/kikelopser/Nginx/blob/main/Nginx/35.PNG)

8.- Reiniciamos el servicio Nginx
```
systemctl restart nginx.service
```

9.- Comprobamos que funciona HTTPS

![36](https://github.com/kikelopser/Nginx/blob/main/Nginx/36.PNG)
