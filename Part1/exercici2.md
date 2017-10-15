## 2. Comprova l'estat de les opcions de log que has utilitzat mitjançant una sessió de mysql client.  

Amb la comanda:
> mysql -se "SHOW VARIABLES" | grep -e log_error -e general_log -e slow_query_log -e log_bin
> ![2]()
