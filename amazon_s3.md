<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](index.md)</sub>
#Amazon S3 : Amazon Simple Storage Service

**Présentation :** Amazon S3 est un service de stockage d'objets qui offre une capacité de mise à l'échelle, une disponibilité des données, une sécurité et des performances de pointe.
Les fichiers stockés sur un Amazon S3 bucket sont appelés des S3 objects

**Help :**
- **configurer** : pour configurer. ex: *aws configurer*
- aws --endpoint=**DOMAINE** s3 **ls** => pour lister ts les fichiers sur un s3
- aws --endpoint=http://s3.**DOMAINE** s3 ls s3://**DOMAINE**=> pour lister ts les fichiers sur un sous domaine s3
- cp : copier un fichier sur le s3. ex : *aws --endpoint=http://s3.**DOMAINE** s3 cp *FICHIER* s3://**DOMAINE***
 
**Procédure :**
 - Pour la configuration, mettre nom bidon partout. ex : *temp*
 
 
 

