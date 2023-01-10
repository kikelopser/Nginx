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
