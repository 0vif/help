<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#wfuzz

**Utilisation :** outil de bruteforce, utile notamment pour les fichiers

**CMD :** wfuzz -c -w ***WORDLIST*** -z **TYPES** --hc **EXCLUDED** **URL**/FUZZFUZ2Z

**Arguments :**
- **-c :** ????
- **-w :** ????
- **-z :** ne récupérer que certains formats. ex : *-z list,-.php-.html-.txt*
- **--hc :** ne pas afficher certains retours. ex : *--hc 404, 403*
- **-c :** ????

**Exemple :** *wfuzz -c -w /usr/share/dirb/wordlists/common.txt -z list,-.php-.html-.txt --hc 404,403 h<span>ttp://10.10.10.10/FUZZFUZ2Z* : va tester et trouver tous les fichiers php, html, txt et ignorer les 404 et 403 en retour