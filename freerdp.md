<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](index.md)</sub>
#freeRDP

**Présentation :** FreeRDP is a free implementation of the Remote Desktop Protocol (RDP), released under the Apache license


**CMD :** xfreerdp /v: ***RHOST***

**ARGS :**
- **/cert:ignore** : Specifies to the scrips that all security certificate usage 
- **/u:Administrator** : Specifies the login username to be "Administrator"

**Exemple :**

- *xfreerdp /v:**RHOST*** 
- *xfreerdp /v:**RHOST** /cert:ignore /u:Administrator*