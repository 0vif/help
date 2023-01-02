<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#Burp Suite

**Présentation :** web crawler : sert à intercepter des appels serveurs HTTP, à modifier les requêtes, à encoder des arguments dans l'url

**Help :**
- Ctrl + R : copier la requête interceptée dans le Repeater
- Ctrl + U : Encoder les caractères sélectionnés

**Procédure :**
- pour l'interception : 
  - soit utiliser l'explorateur fourni avec BurpSuite
  - soit configurer son explorateur pour ajouter manuelement un proxy : 127.0.01 : 8080
- passer en *Intercep ON*
- rappeler l'url
- on modifie les paramètres (penser à les encoder en URL)
- et on renvoie la requête modifiée

