<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](index.md)</sub>
#SSTI : Server Side Template Injection

**Utilisation :** Une série de tests à effectuer pour identifier le template utilisé côté serveur et analyser si une injection est possible.

**Procédure :** 
- pour identifier le template engine => https://book.hacktricks.xyz/pentesting-web/ssti-server-side-template-injection#identify
- on récupère l'envoi de l'input avec [burpsuite](burp_suite.md) puis on envoie un script encodé en url en modifiant un argument
- on commence par tester dans un input **${7*7}** puis on suit le schéma.
- jusqu'à afficher on cherche le template engine utilisé :
  - si issu de [Node.js](node_js.md)
