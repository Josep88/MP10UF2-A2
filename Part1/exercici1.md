## 1. Crea un fitxer de configuració a on:  
### Quins són els logs activats per defecte? Com ho has fet per comprovar-ho?  

L'únic log activat per defecte es el log d'errors.
Per comprovar-ho amb la comanda:  
> mysql -se "SHOW VARIABLES" | grep -e log_error -e general_log -e slow_query_log -e log_bin  
>  ![1]()  


### Activa si no ho estan i indica les configuracions necessàries per activar-los. Indica les rutes dels fitxer de log de Binary, Slow Query i General. Quins paràmetres has modificat?



***
[Torna enrere](https://github.com/Josep88/MP10UF2-A2)
