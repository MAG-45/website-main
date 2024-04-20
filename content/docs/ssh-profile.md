# Introduction

Avant de commencer, il faut savoir à quoi sert un profil SSH, un profil SSH permet de faire comme les raccourcis de MobaXTerm, avoir ses serveurs sous la main facilement, plutôt pratique sous Linux étant donné qu'il n'existe pas d'alternative GUI aux logiciels comme MobaXTerm, RoyalTS ou Termius !

# Création du fichier

Première chose, c'est de créer un fichier dans le *.ssh* de son user.

### Sous Linux 

```bash
touch ~/.ssh/config
```

### Sous Windows 

```shell
notepad ~/.ssh/config 
```
> **Attention !** Lors de l'enregistrement, retirer le point TXT.

# Modification du fichier

### Sous Linux 

```bash
nano ~/.ssh/config
```

### Sous Windows

Suffit d'utiliser le **Notepad** qu'on a ouvert.

### Template

Voici une template qui je trouve, couvre tous les besoins de base d'un Profil SSH.
```shell
Host localhost // Ici rentre le nom de ton profile, utilise des nom ou une nomenclature que tu connais !
    HostName localhost // Ici c'est l'ip de ta machine distance, ça peut être sa résolution DNS
    User root // Le user avec lequel tu veux te connecter
    Port 22 // Le port
    IdentityFile ~/.ssh/tasupercléprivée // Si tu utilise des clé privée pour te connecter, attention ceci est optionel
```

> N'oubliez pas de le **modifier** pour votre utilisation, sachez que vous pouvez avoir plusieurs profile, suffit de refaire un ""Host"".

# Utilisation

Suffit de faire : ``` ssh lenomdetonhost```

Et pouf, il te demandera le password, si tu n'as pas de clé privée, sinon il te connectera !

# Astuce

Dans ton "Host", tu peux retirer le user, lors de la connexion tu pourras faire : 

```shell
ssh tonuser@tonhost
```

Pratique non ?