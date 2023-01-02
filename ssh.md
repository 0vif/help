<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#SSH : Secure Shell

**Présentation :** 
Programme informatique et un protocole de communication sécurisé. Le protocole de connexion impose un échange de clés de chiffrement en début de connexion. Par la suite, tous les segments TCP sont authentifiés et chiffrés. Il devient donc impossible d'utiliser un sniffer pour voir ce que fait l'utilisateur.
Le protocole SSH a été conçu avec l'objectif de remplacer les différents protocoles non chiffrés comme rlogin, telnet, rcp et rsh.

**Utilisation :** si on a une connexion provisoire alors qu' on a le password d' un user et que le serveur possède ssh => autant passer par une connexion SSH

**CMD :** ssh **USER**@**IP**

**Arguments :**
- **-i :** se connecter via le fichier de clé privée.  ex : *ssh -i file_rsa user@<span>10.10.10.10*
  
**Exemple :** ssh user@10.10.10.10

**Procédure :**
- Pour cracker si on a la clé privée : [john](john_the_ripper.md)
- Si en utilisant clé on a : *WARNING: UNPROTECTED PRIVATE KEY FILE!* alors : *chmod 600 *FILE**

????? psexec.py => permet de se connecter à une ip en admin si on a le mdp
 python3 psexec.py administrator@{TARGET_IP}

