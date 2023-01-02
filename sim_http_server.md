<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](tools.md)</sub>
#Simuler un serveur HTTP

**Utilisation :** générer un serveur http pour récupérer des fichiers depuis l'extérieur

**CMD :** python3 -m http.server ***PORT***

**Exemple :** *python3 -m http.server **8000***

**Procédure :**
- Ouvrir terminal depuis le dossier où sont les fichiers que l'on veut récupérer
- Lancer le serveur http
- Récupérer le/les fichier/s avec un wget. ex : *wget 'http://**LHOST**:**LPORT**/**FILE.txt**'*