<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#SMB : Server Message Block

**Port par défaut :** 445

**Utilisation :** échange de message et communication [windows](windows.md)

**CMD :** smbclient ***IP***

**Arguments :**
- **-L :** liste les utilisateurs => *smbclient -L 10.10.10.10*
- **-U :** liste les utilisateurs => *smbclient -L 10.10.10.10*

**Exemple :** smbclient ***10.10.10.10***

**Help :**
- help : aide
- get : télécharger fichier => *get **FILE***

**Liste des dossiers principaux :**
*Si $ présent dans le nom => partage administratif*
-  Admin$
-  C$ => lecteur C
-  IPC$ => ????
-  workShares => espaces de travail

**Utilisateurs :**
- Administrator

**Procédure :**
- **voir si outil d'énumération possible !**
- on commence par essayer de lister les utilisateurs => *smbclient -L **IP***
- si pas de résultats on peut tenter => *smbclient -L ***IP*** -U Administrator*
- on peut tenter connexion sans password avec chacun des principaux dossiers  => *smbclient \\\\\\\\**IP**\\\\**FOLDER***
- tenter la même chose en tant qu'Administrator ou autres utilisateurs => *smbclient \\\\\\\\**IP**\\\\**FOLDER** -U **USER*
- tenter d'intercepter l'authentification avec [Responder](responder.md)
- Si accès admin => impacket psexec.py => psexec.py administrator@ip

**Infos :**
SMB peut être ouvert dans les dossiers windows du genre => *\\\\\\\\**IP**\\\\**FOLDER***
