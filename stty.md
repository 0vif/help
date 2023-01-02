<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](tools.md)</sub>
#STTY

**Présentation :** outil de stabilisation de la console. Modifier et afficher la configuration de la ligne de terminal  

**Procédure :**
  - Si pas fait : *python3 -c 'import pty;pty.spawn("/bin/bash")'*
  - *Ctrl + Z*
  - *stty raw -echo;* si Kali Linux image is using zsh => rajouter *fg* à la suite de cette commande
  - *Enter* 2 fois
  - *export TERM=xterm*
  - *export SHELL=bash*
  - *stty rows 32 cols 128*
  - on a une console stable.

