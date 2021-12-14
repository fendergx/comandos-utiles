# Debian 

## [Cómo apagar y reiniciar en consola](https://www.debian.org/releases/stable/s390x/ch08s01.es.html)

**systemctl poweroff**, reiniciar - **systemctl reboot**

## [Instalar Sudo y convertir al usuario en superUsuario](https://profesorweb.es/2017/03/instalar-sudo-en-debian/)

Para esto hay 2 caminos, uno corto y otro largo

loguearse como usuario root y ejecutar 

````
apt-get install sudo
````



**Forma corta**

Ejecutar el comando siendo root y reemplazando "tuUsuario" por el nombre  de usuario
```
sudo useradd -m -s /bin/bash -G sudo tuUsuario
```

**Forma larga**

 abrir el archivo  /etc/sudoers

```
nano  /etc/sudoers
```

se verá algo así

```
#User privilege specification
root ALL=(ALL) ALL
```

entonces se agrega al final la línea para tu usuario "usuario" 

```
tu_usuario ALL=(ALL) ALL
```

luego se guarda con *control+o* y salir con *control+x*

Una vez configurado esto, ya podremos ejecutar acciones de administrador desde una terminal común, anteponiendo el sudo a la acción a realizar.



