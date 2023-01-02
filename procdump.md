<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#Procdump

**Utilisation :** Permet de faire une analyse d'un process et d'en faire un dump

**CMD :** ./procdump.exe -mp **PROCESS_ID**

**Exemple :** ./procdump.exe -mp 1234

**Help :**
- La première fois on doit accepter conditions ex : -accepteula
- *-m* : commit_usage
- *-p* : counter treshold ?

**Procédure :**

- Exécuter en donnant le process ID.
- on récup donc un dump .dump
- on peut récup fichier avec le [Evil Winrm](evil_winrm.md) download 
- puis on peut tenter le strings sur le fichier de dump