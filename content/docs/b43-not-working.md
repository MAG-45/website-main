# Introduction

J'écris ce petit doc après avoir galéré à remettre en marche mon ancien PC Portable qui possède une carte Wi-Fi Broadcom, qui nécessite le driver b43 (le nom varie selon la distribe, mais appelons le b43), donc en essayant d'installer Fedora 38 sur mon ancien pc portable, je remarque que le driver n'est pas installé, ayant l'habitude car ce driver est un non free et donc très peu souvent dans les repos de base des distributions Linux. Je lance une petite recherche Google pour trouver le bon driver sur les distributions basées sur Red Hat, j'installe le paquet et je redémarre sauf que pouf, rien ne marche ! Mais pourquoi ? Les driver pour B43 n'est pas compatible avec les kernels Linux 6 et supérieure !

# Vérification du kernel

Suffit de lancer un terminal et lancer cette commande

```bash
uname -r
```

Si celui-ci retourne un kernel supérieur ou égal au kernel 6, vous pouvez oublier le Wi-Fi;
Si inférieure, vous pouvez installer le bon driver en suivant les recommandations de votre distribution.

# Résolution

Si vous avez vraiment envie de résoudre ce souci, plusieurs choix s'offre à vous, Juste je ne parlerai **pas** d'installer un kernel inférieur sur une distribution, même si dans beaucoup de cas, le risque est minimum, je trouve ça assez instable surtout d'installer une version inférieure en plus majeur !

## Installer une autre distribution

Chose la plus simple, installer une autre distribution qui supporte encore les kernel Linux 6.0 inférieure voici une liste non exhaustive :

- Linux Mint Victoria
- Ubuntu Jammy
- Debian 11

Je ne mets que des distributions **assez importantes**, mais gardez dans l'esprit qu'il faut qu'une distribution qui se base sur *Debian* ou *Ubuntu* doit être basé sois sous Debian **11** ou inférieure ou Ubuntu **Jammy** ou inférieure.

Pour les distribution *"Rolling Release"*, c'est-à-dire sans numéro de version, vous pouvez **oublier**, elles ont souvent une politique de mise a jours assez vers le plus **récent**, donc basé souvent sur un Kernel 6 ou supérieure. 

Pour l'instant, je remarque que dans les distributions *"grand public"*, uniquement celle sous *Debian ou *Ubuntu* est encore **maintenue** sous un kernel inférieur au 6.

## Méthode non recommandée

Installé une version plus ancienne d'une distribution, sachez que même si certaine distribution font le choix de maintenir pendant X temps après la sortie d'une nouvelle version, souvent celle-ci se limite aux mises à jour de sécurité et peut dépendre de la communauté derrière celle-ci. En plus de poser des soucis de sécurité d'ici quelques années, où il n'aura plus de distribution sous un kernel 6 ou inférieure.

# Conclusion 

Malheureusement, il n'y a pas beaucoup de solution pour nous, a part si un membre de la communauté décide de rendre les drivers b43 compatibles avec les kernels 6 et supérieure. Peu d'espoir car nous sommes déjà au kernel 6.6 lorsque j'écris cet article, on peut se consoler car le kernel 5 rentre en LTS donc encore quelques années mais à voir si la communauté suit derrière au niveau des paquets.