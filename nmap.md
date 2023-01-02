<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#nmap

**Utilisation :** parcourir un serveur et chercher les ports ouverts dessus

**CMD :** nmap ***IP***

**Arguments :**
- **-sC :** Performs a script scan using the default set of scripts. It is equivalent to script=default. Some of the scripts in this category are considered intrusive and
    should not be run against a target network without permission.
- **-sV :** Enables version detection, which will detect what versions are running on what port.
- **-p- :** tous les ports de 0 à 65535
- **-v :** verbose
- **-vv :** plus de verbose
- **--min-rate :** This is used to specify the minimum number of packets Nmap should send per second; it speeds up the scan as the number goes higher ex --min-rate=1000
- **-Pn :** Treat all hosts as online => permet de prévenir les blocages de pare feu windows
- **-sU :** ports udp
- **-A :** os version
- **-p :** port en particulier

**Exemple :** nmap -sC -sV -Pn  10.10.10.10 -p- --min-rate 1000

