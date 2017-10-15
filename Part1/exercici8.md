## 8. Assegura't que el Binary Log estigui activat i borra tots els logs anteriors mitjançant la sentència RESET MASTER.
### Crea i borra una base de dades anomenada foo. Utilitza la sentències:  
### &nbsp;&nbsp;&nbsp;&nbsp;mysql> CREATE DATABASE foo;  
### &nbsp;&nbsp;&nbsp;&nbsp;mysql> DROP DATABASE foo;  

### Mitjançant la sentència _SHOW BINLOG EVENTS_ llista els events i comprova les sentències anteriors en quin fitxer de log estan.  

### Realitza un Rotate log mitjançant la sentència FLUSH LOGS  

### Crea i borra una altra base de dades com l'exemple anterior del _foo_. Però en aquest cas anomena la base de dades _bar_  

### Llista tots els fitxers de log i els últims canvis mitjançant la sentència SHOW. Quina sentència has utilitzat? Mostra'n el resultat.

### Borra el primer binary log. Quina sentència has utilitzat?

### Utilitza el programa mysqlbinlog per mostrar el fitxer _mysql-bin.000002_  
### Quin és el seu contingut?  
### Quin número d'event ha sigut el de la creació de la base de dades bar?



***
[Torna enrere](https://github.com/Josep88/MP10UF2-A2)
