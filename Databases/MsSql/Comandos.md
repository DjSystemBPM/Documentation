![Comandos](http://vignette3.wikia.nocookie.net/logopedia/images/c/cd/MicrosoftSQLServer.png/revision/latest?cb=20150614233628)

# Comandos SQL Server

### Crear Base de Datos
```sql
USE master;   
SELECT * from sys.databases WHERE name='TestData'; 
DROP DATABASE TestData; 
CREATE DATABASE TestData;   
USE TestData;
```

### Crear Tabla
```sql
CREATE TABLE dbo.Products  (ProductID int PRIMARY KEY NOT NULL,  ProductName varchar(25) NOT NULL,  Price money NULL,  ProductDescription text NULL); 
SELECT * FROM dbo.Products; 
INSERT INTO products (ProductID, ProductName, Price, ProductDescription)  
	VALUES (1,'COCA', '5.00', 'REFRESCO DE COLA'); 
```
 
### Version de la base de datos
```sql
SELECT @@version; 
```

### Cierra conexiones abiertas de la base
* Opcion Uno:
```sql
ALTER DATABASE TestData SET SINGLE_USER WITH ROLLBACK IMMEDIATE; 
```
* Opcion Dos (Mejor Opcion):
```sql
SELECT * FROM master..sysprocesses WHERE dbid = DB_ID(‘multivaDesarrollo’);
KILL <spid>;
```
 
### Ejecutar Stored Procedure
```sql
EXEC dbo.app_ConsultaFondosNBE '116448';
```

### Ver el contenido del Stored Procedure
```sql
USE multiva 
sp_helptext [dbo.prueba]; 
```


### Crear Schema
```sql
CREATE SCHEMA Nómina; 
```
### Crear Sequence
```sql
CREATE SEQUENCE Nómina.Foliador  
START WITH 0 INCREMENT BY 1;  

SELECT NEXT VALUE FOR Nómina.Foliador;    

INSERT Test.Orders (OrderID, Name, Qty)  
VALUES (NEXT VALUE FOR Nomina.Foliador, 'Tire', 2) ;  
```
    
	

