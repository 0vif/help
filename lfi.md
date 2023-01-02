<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#LFI : Local file inclusion

**Présentation :** Accéder de manière détournée à des fichiers locaux comme le *etc/passwd*


**Procédure :**
- si on trouve une URL ou autre qui fait appel à un fichier du serveur. ex : *http://*RHOST*?file=index.php*
  - Le fichier ***/etc/passwd*** peut fournir pas mal d'informations sur les utilisateurs et les protocoles utilisés
  -  Le chemin exact du */etc/passwd* est */var/www/html/etc/passwd*
  -  on peut tenter : *curl 'http://*RHOST*/?file=/etc/passwd'* (ne marche pas tout le temps)
  -  tenter aussi : *curl 'http://*RHOST*/?file=../../../etc/passwd'*
  -  Il peut y avoir une restriction sur l utilisateur.
  -  Si on accède à ce fichier, on peut obtenir des informations importants.
-  On peut facilement passer d'une LFI à un RCE si protocole disponible comme [TFTP](tftp.md)