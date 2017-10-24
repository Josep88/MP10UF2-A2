## Creació de la clau del certificat i la clau privada  
  
Primer de tot creem la carpeta on volem que es posin els fitxers:  
> ![1](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/1.PNG)  

Ara executem les comandes per crear les claus:  
> ![2](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/2.PNG)  

Ara hi ha que crear una clau privada pel servidor:  
> ![3](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/3.PNG)  

I ara tenim que exportar la clau privada del servidor a una de tipus RSA:  
> ![4](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/4.PNG)  

I per últim generar un certificat de servidor utilitzant el certificat CA:  
> ![5](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/5.PNG)  
  
## Configurar SSL a MySQL Server  
  
Primer de tot hem de comprovar que l’opció SSL no esta activada al MySQL, per això fem aquesta comanda per veure si esta DISABLED o ENABLED:  
> ![6](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/6.PNG)  

El següent pas es introduir aquestes línies al fitxer de configuració, sota l’apartat [mysqld]:  
> ![7](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/7.PNG)  

I ara reiniciem el servei de MySQL.  
I ja podem tornar a comprovar si apareix en ENABLED:  
> ![8](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/8.PNG)  
  
## Crear un usuari amb privilegis d’SSL  
  
Tenim que entrar al MySQL i crear l’usuari:  
> ![9](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/9.PNG)  
  
## Configurar SSL al client de MySQL  
  
Tenim que executar aquestes comandes a la carpeta on estan els certificats i les claus anteriors:  
> ![10](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/10.PNG)  

També tenim que convertir la clau generada pel client a RSA:  
> ![11](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/11b.PNG)  

I per últim, hi ha que crear un certificat pel client:  
> ![12](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/12b2.PNG)  

Ara tenim que transferir els fitxers creats: _ca-cert.pem_, _client-cert.pem_ i _client-key-pem_ a on s’hagi d’executar el client de MySQL.  
Amb aquesta comanda pots fer la connexió:  
> mysql --ssl-ca=ca-cert.pem --ssl-cert=client-cert.pem --ssl-key=client-key.pem -h <mysql-server-ip-address> -u ssluser -p  

Si fas la connexió per mitja de SSL, fent un _status;_ t’ha de donar una clau _cipher_:  
> ![13](https://raw.githubusercontent.com/Josep88/MP10UF2-A2/master/img/13b2.PNG)  


***
[Torna enrere](https://github.com/Josep88/MP10UF2-A2)
