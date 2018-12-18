# ESP8266-at-command
Command AT for module ES8266 Arduino

El modulo ES8266 se puede utilizar en arduino para controlar distintos dispositivos desde http. Aquí están algunos ejemplos y comandos AT que se puede utilizar.
Para conectar el modulo ESP8266 en Arduino es necesario utilizar los comandos AT.
En esta lista estan los comandos mas confusos, hay muchos sitios donde se puede encontrar todos los comandos pero nadie explica que hay comando que son validos de acuerdo a la versión del fireware.

Modo de cliente y servidor:
> AT+CWMODE=3

1 = Modo estación (Cliente) - Station mode (client)

2 = Punto de acceso (Servidor) - AP mode (host)

3 = Punto de acceso (servidor) + Modo estación (Cliente) - AP + Station mode (Yes, ESP8266 has a dual mode!)

Cambia el nombre a la red des dispositivo estando en modo 3
> AT+CWSAP="nombreRed","contraseñaRed",Canal,3

AT+CWSAP=ssid,pwd,ch,ecn
ssid: String, ESP8266’s softAP SSID
pwd: String, Password, no longer than 64 characters
ch: channel id
ecn:
0 = OPEN
2 = WPA_PSK
3 = WPA2_PSK
4 = WPA_WPA2_PSK

Establece IP estatica - Solo fireware versión 0.9.5:
> AT+CIPSTA="192.168.100.5"

Establece IP estatica - Solo fireware versión 1.1.1:
> AT+CIPSTA="192.168.100.5","192.168.100.1","255.255.255.0"

AT+CIPSTA=address,gateway,netmask

Listado completo de comandos aquí. https://room-15.github.io/blog/2015/03/26/esp8266-at-command-reference/
Como conectar el modulo ESP8266 en Arduino Uno aquí. http://kio4.com/arduino/57modulowifi_2.htm

