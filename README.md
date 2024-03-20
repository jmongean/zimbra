CLONAR
git clone https://github.com/jmongean/zimbra.git

Crear Imagen
docker build -t NOMBRE_IMAGEN .

Crear contenedor
docker run -p 25:25 -p 80:80 -p 465:465 -p 587:587 -p 110:110 -p 143:143 -p 993:993 -p 995:995 -p 443:443 -p 8080:8080 -p 8443:8443 -p 7071:7071 -p 9071:9071 -h HOSTNAME.MAIL_DOMINIO.com --dns 127.0.0.1 --dns 8.8.8.8 -it -e PASSWORD=PAS123 NOMBRE_IMAGEN

HOSTNAME = Hostname del Servidor

MAIL_DOMINIO.com = dominio de Correo con el cual se creará Zimbra

docker ps
docker exec -ti ID_CONTENEDOR bash
  su - zimbra
  zmcontrol status
  zmcontrol restart

Valida en el Browser
Zimbra admin = https://tuip:7071
Zimbra Web Mail= https://tuip

