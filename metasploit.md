<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](tools.md)</sub>
#METASPLOIT framework

**Utilisation :** Outil ultime qui centralise BEAUCOUP d'exploitations de failles

**CMD :** msfconsole

**Tutorial :** https://h5ckfun.info/tutoriel-metasploit-pour-debutants-maitrisez-en-5-minutes/

**Help :**
- *show exploits* : liste de toutes les failles exploitables
- *show options* : options générales
- *search **EXPLOIT*** : montre tous les exploits en relation : ex : *search winrm_login*
- *use **EXPLOIT*** : sélectionner. ex : *use auxiliary/scanner/winrm/winrm_login*
- *show options* : options du module
- *set **OPTION*** : config une option. ex : *set DOMAIN SUPPORTDESK*
- *run* ou *exploit* : lancer l'exploit

**Options :**
- **LHOST** : lhost est l’adresse IP de l’attaquant
- **LPORT** : C’est le port que vous souhaitez utiliser
- **RHOST** : Ceci est l’adresse IP de la machine victime
- **RPORT** : Le numéro de port de la victime.




 