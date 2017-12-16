# MySQL

## 1. Sentencias

### DROP TABLE
```sql
DROP TABLE IF EXISTS <Tabla>;
```
### CREATE TABLE
```sql
CREATE TABLE  <Tabla> (
     ID int NOT NULL AUTO_INCREMENT,
     <columna> VARCHAR(100) NOT NULL,
  PRIMARY KEY( ID )
);
```

### SELECT
```sql
SELECT * FROM <Tabla>; 
SELECT <columna>, <columna>  FROM <Tabla>; 
```

### DISTINCT
```sql
SELECT DISTINCT <columna> FROM <Tabla>; 
```

### WHERE 
```sql
SELECT * FROM <Tabla> WHERE <Columna> = 'PERFIL 1'; 
SELECT * FROM <Tabla> WHERE <Columna> = ‘ANTONIO’ AND <Columna> = ‘GARCIA’;
SELECT * FROM <Tabla> WHERE <Columna> = ‘ANTONIO’ OR <Columna> = ‘GARCIA’;
```

### ORDER BY 
```sql
SELECT <Columna> FROM <Tabla> ORDER BY <Columna> ASC|DESC;
```

### INSERT 
```sql
INSERT INTO <Tabla> VALUES (<Valor1>, <Valor2>, <Valor N>);
INSERT INTO <Tabla> (<Columna1>, <Columna2>, <Columna N>) VALUES (<Valor1>, <Valor2>, <Valor N>);
```

### UPDATE
```sql
UPDATE <Tabla> SET <Columna1> = <Valor1>, <Columna2> = <Valor2> WHERE <Columna3> = <Valor3>;
```

### DELETE
```sql
DELETE FROM <Tabla> WHERE <Columna1> = <Valor1>;
```

### JOIN 
```sql
SELECT * FROM <Tabla> JOIN <Tabla> JOIN <Tabla> WHERE <Columna> = 'PERFIL 1'; 
```

### ADD AND DROP COLUMNS 
```sql
ALTER TABLE <Tabla> ADD ( <Columna> BIT(1) NOT NULL, <Columna> NUMERIC(19, 0)); 
ALTER TABLE <Tabla> ADD <Columna> NUMERIC(19, 0) NOT NULL AFTER <Columna>; 
ALTER TABLE <Tabla> DROP <Columna>; 
```
