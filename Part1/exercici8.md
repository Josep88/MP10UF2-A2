## 8. Assegura't que el Binary Log estigui activat i borra tots els logs anteriors mitjançant la sentència RESET MASTER.

> ![80](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/80.PNG)  

### Crea i borra una base de dades anomenada foo. Utilitza la sentències:  
### &nbsp;&nbsp;&nbsp;&nbsp;mysql> CREATE DATABASE foo;  
### &nbsp;&nbsp;&nbsp;&nbsp;mysql> DROP DATABASE foo;  

> ![81](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/81.PNG)  

### Mitjançant la sentència _SHOW BINLOG EVENTS_ llista els events i comprova les sentències anteriors en quin fitxer de log estan.  

> ![82](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/82.PNG)  

Les sentencies estan guardades al fitxer _/var/lib/mysql/mysql-bin.000001_:  

> ![83](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/83.PNG)  

### Realitza un Rotate log mitjançant la sentència FLUSH LOGS  

> ![84](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/84.PNG)  

### Crea i borra una altra base de dades com l'exemple anterior del _foo_. Però en aquest cas anomena la base de dades _bar_  

> ![85](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/85.PNG)  

### Llista tots els fitxers de log i els últims canvis mitjançant la sentència SHOW. Quina sentència has utilitzat? Mostra'n el resultat.

Llistat dels fitxers:  
> ![86](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/86.PNG)

Últims canvis:
> ![87](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/87.PNG)

### Borra el primer binary log. Quina sentència has utilitzat?

Sentència _PURGE BINARY LOGS_ (es posa el 2 ja que vol dir "borrar tot lo que va abans del 2"):  
> ![88](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/88.PNG)

### Utilitza el programa mysqlbinlog per mostrar el fitxer _mysql-bin.000002_  
### Quin és el seu contingut?  

> ![89](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/89.PNG)

### Quin número d'event ha sigut el de la creació de la base de dades bar?

El número 310.  

***
[Torna enrere](https://github.com/Josep88/MP10UF2-A2)
