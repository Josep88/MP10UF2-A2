## 1. Crea un fitxer de configuració a on:  
### Quins són els logs activats per defecte? Com ho has fet per comprovar-ho?  

L'únic log activat per defecte es el log d'errors.
Per comprovar-ho amb la comanda:  
> mysql -se "SHOW VARIABLES" | grep -e log_error -e general_log -e slow_query_log -e log_bin  
>  ![11](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/11.PNG)  


### Activa si no ho estan i indica les configuracions necessàries per activar-los. Indica les rutes dels fitxer de log de Binary, Slow Query i General. Quins paràmetres has modificat?

Per activar els altres logs hi ha que afegir a la configuració:  
> ![12](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/12b.PNG)

Per a que funcioni tot, hi ha que donar permisos al usuari mysql d'escriptura als fitxers de log:
> chown mysql:mysql /var/log/mysql/mysql-gen.log  
> chmod g+w /var/log/mysql/mysql-gen.log

També hi ha que obrir el SELinux per a que agafi el fitxer de log general, per això hi ha que modificar el fitxer /etc/selinux/config  
> ![13](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/13.PNG)

***
[Torna enrere](https://github.com/Josep88/MP10UF2-A2)
