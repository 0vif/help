<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#FTP : File transfer protocol

**Port par défaut :** ???

**Utilisation :** échange/téléchargements de fichiers

**CMD :** ftp ***IP***

**Exemple :** ftp 10.10.10.10

**Help :**
- get : télécharger fichier => *get **FILE***

**Procédure :**

Si le ftp est mal configuré, sur [nmap](nmap.md) on verra : ftp-anon: Anonymous FTP login allowed (FTP code 230).
Alors login = *anonymous* et mdp = *vide*