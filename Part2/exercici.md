## Creació de la clau del certificat i la clau privada  

Primer de tot creem la carpeta on volem que es posin els fitxers:  
> ![1]()  
Ara executem les comandes per crear les claus:  
> ![2]()  
Ara hi ha que crear una clau privada pel servidor:  
> ![3]()  
I ara tenim que exportar la clau privada del servidor a una de tipus RSA:  
> ![4]()  
I per últim generar un certificat de servidor utilitzant el certificat CA:  
> ![5]()  

## Configurar SSL a MySQL Server  

Primer de tot hem de comprovar que l’opció SSL no esta activada al MySQL, per això fem aquesta comanda per veure si esta DISABLED o ENABLED:
> ![6]()
El següent pas es introduir aquestes línies al fitxer de configuració, sota l’apartat [mysqld]:
> ![7]()
I ara reiniciem el servei de MySQL.
I ja podem tornar a comprovar si apareix en ENABLED:
> ![8]()

## Crear un usuari amb privilegis d’SSL

Tenim que entrar al MySQL i crear l’usuari:
> ![9]()



## Configurar SSL al client de MySQL

Tenim que executar aquestes comandes a la carpeta on estan els certificats i les claus anteriors:
> ![10]()
També tenim que convertir la clau generada pel client a RSA:
> ![11]()
I per últim, hi ha que crear un certificat pel client:
> ![12]()
Ara tenim que transferir els fitxers creats: _ca-cert.pem_, _client-cert.pem_ i _client-key-pem_ a on s’hagi d’executar el client de MySQL.
> mysql --ssl-ca=ca-cert.pem --ssl-cert=client-cert.pem --ssl-key=client-key.pem -h <mysql-server-ip-address> -u ssluser -p
Si fas la connexió per mitja de SSL, si fas un _status;_ t’ha de donar una clau _cipher_:
> ![13]()


***
[Torna enrere](https://github.com/Josep88/MP10UF2-A2)
