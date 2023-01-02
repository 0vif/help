<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#gobuster

**Utilisation :** outil de bruteforce, utile notamment pour les directories, subdirectories, domaines et sous-domaines.

**CMD :** 
- gobuster vhost ***ARG*** pour les sous-domaines
- gobuster dir ***ARG*** pour les directories

**Arguments :**
- **-exemple :** exemple

**Exemple :**
- gobuster dir --url htt<span>p://10.10.10.10/ --wordlist /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -x php,html
-  gobuster vhost -w /opt/useful/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -u  ht<span>tp://thetoppers.htb

**Help :**
-   --url / -u => url
-   --worldlist / -w => worldlist
-   -x => chercher des types de fichiers


