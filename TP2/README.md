# Rapport du TP 2 : Wireshark

## HTTP Session 

On identifie l'interface qu'on utilise, en l'occurence sous linux, la command "ip a" donne la liste des interfaces.
On choisi wlan0, car je suis connecté en Wi-Fi.

![ip a](screenshots/ip.png)

Avec la commande ci-dessus on ouvre wireshark en spécifiant l'interface, et on le sélectionne lors du démarrage.

![wireshark](screenshots/select-interface.png)

En triant avec les protocoles et en regardant les échanges DNS, on trouve que l'ip du serveur du serveur web est : 156.18.19.133

![dns](screenshots/dns-ip.png)

L'IP de la machine avec laquelle on échange les données de la page web est aussi : 156.18.19.133

![dns](screenshots/http-ip.png)

Ces échanges sont effectué grace au protocole HTTP.

On compte 11 connections TCP :

![tcp connections](screenshots/tcp-connections.png)

Le diagramme pour les échanges au niveau du protocole http entre le client et le serveur nous avons  cela :

![diagram client](screenshots/diagram-client.png)

La méthode HTTP utilisée pour télécharger la page Web est "GET".

Le code de retour du serveur est "301 Moved Permanently". Cela signifie que la ressource demandée a été déplacée de manière permanente vers un nouvel emplacement.

Les informations spécifiées par le client (le navigateur) sont les suivantes :

User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/111.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Connection: keep-alive
Pragma: no-cache
Cache-Control: no-cache

La taille de la réponse est de 231 octets. La version du protocole utilisée par le serveur est "HTTP/1.1".


