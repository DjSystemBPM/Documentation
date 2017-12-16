![Comandos](https://doc.octoperf.com/monitoring/img/oracledb-logo.png)

# Comandos

### Cambiar puerto de Oracle DB
```sql
EXEC dbms_xdb.sethttpport(8081);
SELECT dbms_xdb.gethttpport() FROM dual;
```

### Creacion de TableSpaces
```sql
/* Tablespaces para datos*/
CREATE TABLESPACE sats_tum LOGGING 
DATAFILE 'C:/DataBases/Oracle11g/app/oracle/oradata/XE/SATS_TUM.dbf' SIZE 1024M 
EXTENT MANAGEMENT LOCAL SEGMENT SPACE MANAGEMENT AUTO; 

/* Tablespaces para indices*/
CREATE TABLESPACE SATS_TUM_IDX LOGGING 
DATAFILE 'C:/DataBases/Oracle11g/app/oracle/oradata/XE/SATS_TUM_IDX.dbf' SIZE 512M 
EXTENT MANAGEMENT LOCAL SEGMENT SPACE MANAGEMENT AUTO; 
```

### Creacion de usuario para el tablespace
```sql
CREATE USER alfcueba PROFILE DEFAULT IDENTIFIED BY "Dj.130189" 
DEFAULT TABLESPACE SATS_TUM TEMPORARY TABLESPACE TEMP ACCOUNT UNLOCK; 
```

### Permisos al usuario del tablespace
```sql
GRANT CONNECT TO alfcueba; 
GRANT RESOURCE TO alfcueba; 
GRANT ALTER ANY INDEX TO alfcueba; 
GRANT ALTER ANY SEQUENCE TO alfcueba; 
GRANT ALTER ANY TABLE TO alfcueba; 
GRANT ALTER ANY TRIGGER TO alfcueba; 
GRANT CREATE ANY INDEX TO alfcueba; 
GRANT CREATE ANY SEQUENCE TO alfcueba; 
GRANT CREATE ANY SYNONYM TO alfcueba; 
GRANT CREATE ANY TABLE TO alfcueba; 
GRANT CREATE ANY TRIGGER TO alfcueba; 
GRANT CREATE ANY VIEW TO alfcueba; 
GRANT CREATE PROCEDURE TO alfcueba; 
GRANT CREATE PUBLIC SYNONYM TO alfcueba; 
GRANT CREATE TRIGGER TO alfcueba; 
GRANT CREATE VIEW TO alfcueba; 
GRANT DELETE ANY TABLE TO alfcueba; 
GRANT DROP ANY INDEX TO alfcueba; 
GRANT DROP ANY SEQUENCE TO alfcueba; 
GRANT DROP ANY TABLE TO alfcueba; 
GRANT DROP ANY TRIGGER TO alfcueba; 
GRANT DROP ANY VIEW TO alfcueba; 
GRANT INSERT ANY TABLE TO alfcueba; 
GRANT QUERY REWRITE TO alfcueba; 
GRANT SELECT ANY TABLE TO alfcueba; 
GRANT UNLIMITED TABLESPACE TO alfcueba; 
```

### Eliminar permisos por objeto de usuario
```sql
REVOKE DELETE ON tabla FROM alfcueba;
```

### Eliminar permisos por nivel de sistema de determinado usuario
```sql
REVOKE DROP ANY TABLE FROM alfcueba; 
```

### Eliminar del sistema al usuario
```sql
DROP USER "alfcueba" CASCADE; 
```

### Muestra a los usuarios del sistema
```sql
SELECT * FROM ALL_USERS; 
```





