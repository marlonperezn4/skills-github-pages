---
title: "Dominio virtual en XAMPP"
date: 2023-06-07
---

# ¿Cómo crear un dominio virtual en XAMPP?

### Un dominio virtual me permite acceder a mi proyecto de una manera diferente a "localhost"

Normalmente uno accede a una página desde el local con la dirección 

- http://127.0.0.1/nameproject
- http://localhost/nameproject

Con un dominio virtual se puede modificar la ruta de acceso ejemplo:

- midominiovirtual.com

## Paso a paso

### Configuración en XAMMP

Acceder a la carpeta de xammp que normalmente está alojada en discolocal c

En este caso mi ruta es: C:\xampp7\apache\conf\extra

Dentro de la carpeta **extra** debemos entrar a configurar el archivo: *** httpd-vhosts.conf ***

Agregar

```
<VirtualHost *:80>
    DocumentRoot "C:/xampp7/htdocs"
    ServerName localhost
</VirtualHost>

<VirtualHost *:80>
    DocumentRoot "C:/xampp7/htdocs/nameproject"
    ServerName midominiovirtual.com
</VirtualHost>
```

El segundo ``` <VirtualHost *:80> ``` es el nuevo dominio que agregaremos. Es necesario colocar el primero sino se pierde el localhost (creo)

### Configuración en System32

Acceder a la carpeta System32 que normalmente está ubicada en el disco local c

Mi ruta es: C:\Windows\System32\drivers\etc

Dentro de la carpeta **etc** debemos entrar a configurar el archivo *** hosts ***

Agregar

```
# localhost name resolution is handled within DNS itself.
	127.0.0.1       localhost
	127.0.0.1       midominiovirtual.com
#	::1             localhost
```

### Probando que funciona

Apagar el XAMMP y volver a encender. Ahora podremos acceder a nuestro proyecto desde el nuevo dominio agregado. Good Job