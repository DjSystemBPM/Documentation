![Instalacion](https://doc.octoperf.com/monitoring/img/oracledb-logo.png)

# Instalacion

### Fedora
* Descarga la base desde la página de oracle
* Descomprime el ZIP y te creara una carpeta llamada Disk1
* Ejecuta el rpm de la carpeta Disk1:
```sh
$ sudo dnf install oracle-xe-11.2.0-1.0.x86_64.rpm
```
* Al terminar Configura la Base de Datos:
```sh
$ sudo /etc/init.d/oracle-xe configure
```
* Ejecuta el Siguiente comando:
```sh
$ ./u01/app/oracle/product/11.2.0/xe/bin/oracle_env.sh
```
* Ingresa a la base de datos:
```sh
$ sqlplus system
```

### Instalacion de SQLDeveloper
* Descarga desde la página e Instala el RPM:
```sh
$ sudo dnf install sqldeveloper.rpm
```
* Ejecutarlo por primera vez de la siguiente manera
```
$ /usr/local/bin/sqldeveloper
```
* Te pedirá que cambies un archivo para especificar el $JAVA_HOME:
```
$ gedit /home/acuevas/.sqldeveloper/4.2.0/product.conf

Descomenta la siguiente línea:
    SetJavaHome /usr/java/jdk1.8.0_131
```
* Ejecuta el programa de manera normal
