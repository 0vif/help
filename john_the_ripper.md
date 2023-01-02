<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](cryptage.md)</sub>
#John the ripper

**Utilisation :** crack du hash avec une wordlists

**CMD :** john -w=***WORLDLIST*** ***FICHIER_HASH***

**Arguments :**
- **-w :** worldlist

**Help :**
- Soucis avec le *rockyou.txt* utilisé, je l'ai écrasé en dézippant l'ancien et OK

**Procédure :**
- **Pour un [zip](zip.md) :** convertir d'abord avec zip2john. ex : *zip2john **NOM_FICHIER** > **UTPUTFILE***  => ensuite utiliser John the ripper
- **Pour une clé [SSH](ssh.md) :** conversion avec ssh2john . ex : *ssh2john **NOM_FICHIER** > **OUTPUTFILE*** => ensuite utiliser John the ripper