<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#MS-RPC

**Port par défaut :** 135

**Présentation :** MS-RPC est un protocole propriétaire Windows basé sur le standard DCE / RPC. C’est un protocole à port dynamique comme rpcbind ou portmap sous Linux. C’est à dire que la première connexion est effectuée sur le port 135 puis le client est redirigé vers un autre port ouvert dynamiquement dans la plage autorisée (par défaut 49152 à 65535). Ce mode de fonctionnement n’est plus à la mode actuellement. Il nécessite d’ouvrir des plages de ports assez larges sur les pares-feu des serveurs et des routeurs inter-sites.
Ce protocole est notamment utilisé pour la réplication des annuaires LDAP entre les serveurs Active Directory.

**Help :**
- https://secybr.com/posts/msrpc-pentesting-best-practices
  
**Procédure :**
- tenter [rpcclient]() : ex => *rpcclient -U "" -N **RHOST***
- tenter bruteforce avec [enum4linux](enum4linux.md)
- tenter *python3 /usr/share/doc/python3-impacket/examples/rpcdump.py **RHOST***
- Si on a **MDP** et **USERNAME** : 
  - bruteforce rcp pour avoir une énum des users: impacket *lookupsid.py* performs bruteforcing of Windows SID’s to identify users/groups on the remote target. ex :*python3 lookupsid.py ./**USER**@**RHOST***
  - [METASPLOIT](metasploit.md) : 
    - *winrm_login* : tests des users avec des passwords et sans passwords
      - Faire un fichier avec les users trouvés
      - Faire un fichier avec les passwords trouvés
      - Configurer msf et run
  - Si on trouve une association user/admin, alors utiliser [evil_winrm](evil_winrm.md)
    - on peut regarder un peu les process qui tournent: ps

