<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#DNS : Domain Name System

**Linux :** /etc/hosts => **IP** **URL**

**Windows Remote Management :** ?????? ../../../../../../../../windows/system32/drivers/etc/hosts => **IP** **URL**

**Procédure :** 
- Si pas de DNS, on peut l'anticiper en ajoutant une ligne dans le fichier /etc/hosts . ex : *"10.10.10.10  h<span>ttp://mon-url.com"* , 
- Avant d'appeler le dns, linux se servira dans ce fichier pour trouver ce dns
- Si on trouve de nouveaux sous-domaine on les rajoute à nouveau
