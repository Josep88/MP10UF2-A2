## 8. Assegura't que el Binary Log estigui activat i borra tots els logs anteriors mitjançant la sentència RESET MASTER.

> ![80]()  

### Crea i borra una base de dades anomenada foo. Utilitza la sentències:  
### &nbsp;&nbsp;&nbsp;&nbsp;mysql> CREATE DATABASE foo;  
### &nbsp;&nbsp;&nbsp;&nbsp;mysql> DROP DATABASE foo;  

> ![81]()  

### Mitjançant la sentència _SHOW BINLOG EVENTS_ llista els events i comprova les sentències anteriors en quin fitxer de log estan.  

> ![82]()  

Les sentencies estan guardades al fitxer _/var/lib/mysql/mysql-bin.000001_:  

> ![83]()  

### Realitza un Rotate log mitjançant la sentència FLUSH LOGS  

> ![84]()  

### Crea i borra una altra base de dades com l'exemple anterior del _foo_. Però en aquest cas anomena la base de dades _bar_  

> ![85]()  

### Llista tots els fitxers de log i els últims canvis mitjançant la sentència SHOW. Quina sentència has utilitzat? Mostra'n el resultat.

Llistat dels fitxers:  
> ![86]()

Últims canvis:
> ![87]()

### Borra el primer binary log. Quina sentència has utilitzat?

Sentència _PURGE BINARY LOGS_ (es posa el 2 ja que vol dir "borrar tot lo que va abans del 2"):  
> ![88]()

### Utilitza el programa mysqlbinlog per mostrar el fitxer _mysql-bin.000002_  
### Quin és el seu contingut?  

> ![89]()

### Quin número d'event ha sigut el de la creació de la base de dades bar?

El número 310.  

***
[Torna enrere](https://github.com/Josep88/MP10UF2-A2)
