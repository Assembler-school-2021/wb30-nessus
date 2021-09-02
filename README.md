# wb30-nessus

Descargamos nessus de aquí:
```
curl --output Nessus-8.14.0-debian6_amd64.deb https://www.tenable.com/downloads/api/v1/public/pages/nessus/downloads/12696/download?i_agree_to_tenable_license_agreement=true
dpkg -i Nessus-8.14.0-debian6_amd64.deb
systemctl enable --now nessusd
```

## Sqlmap
¿A qué hace referencia el output nos ha facilitado?
Nos proporciona el usuario de la bdd:
user(): 'acuart@localhost'

> Pregunta 3 : A continuación ejecuta sqlmap, realizando una pequeña modificación en el comando lanzado anteriormente y que saque por pantalla el listado de las db y tablas de nuestro target.
```
	./sqlmap.py -c sqlmap.conf --tables
	./sqlmap.py -c sqlmap.conf --dbs
```
Estas son las bdd encontradas:
	available databases [2]:
	[*] acuart
	[*] information_schema

> ¿Qué podemos ver en el output anterior?
> 
El contenido de las tablas

## openvas

Instalar build-esssentials y seguir este tutorial:
`apt install build-essentials`

https://sadsloth.net/post/install-gvm-20_08-src-on-debian/

## Segundo escaneo Openvas
> Pregunta 3 : Crea un script que acepte un parámetro $1 que sea un hostname. Con ese parámetro debe crear y lanzar un escaneo a el wordpress que aprovisonamos en la pregunta anterior.
