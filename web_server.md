<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#Serveur web http

##Procédure générale
- Si accès impossible sur domaine ou sous-domaines, tenter en fixant le [DNS](dns.md)
- Avec [wappalyzer](wappalyzer.md), identifier les languages utilisés
- Parcourir les dossiers, les fichiers et/ou sous-domaines [gobuster](gobuster.md)
- Recommencer avec [wfuzz](wfuzz.md) au cas où.

##Procédure Web

- **[Login](web_login.md)** : tenter de s'authentifier 
- **[Injection SQL](sql_injection.md)** 
- **[XEE](xee.md)** : tester une faille dans les inputs
- **[LFI](lfi.md)** : si on détecte l'appel d'un fichier. ex : *http://*RHOST*?file=index.php*

##Languages
- **[PHP](php.md)**

##CMS et Interfaces
- **[Joomla](joomla.md)**
- **[Jenkins](jenkins.md)**
- **[Cisco](cisco.md)**
- **[Apache](apache.md)**
- **[Unifi](unifi.md)**
