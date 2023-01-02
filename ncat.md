<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](tools.md)</sub>
#ncat

**Utilisation :** mettre un port en écoute, principalement utilisé pour le [reverse shell](reverse_shell.md)

**CMD :** nc ***LPORT***

**Exemple :**  nc -nvlp ***1337***

**Procédure :**
- si interception réussie, on stabilise la console avec : *python3 -c 'import pty;pty.spawn("/bin/bash")'*
- si possible faire évoluer le terminal avec [STTY](stty.md)
