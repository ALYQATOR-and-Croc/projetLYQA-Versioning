# Notes de cours et rapport - Arthur Hervé
**Comme convenu par message Discord, mon rapport personnel sera remis plus tard dans la semaine du 26 septembre. Le message sera retiré quand j'aurai terminé.**  
**Le rapport de groupe est de son côté rendu le 25 septembre**
## Qu'est-ce que le versionning
C'est la pratique de conserver des copies ou clones d'un même projet pour avancer en parallèle sur des tâches différentes. Ce travail est sécurisé par le traçage de chaque étape réalisée.
## Rapide présentation de Git et de GitHub
Git permet d'avoir une traçabilité d'un projet. Chaque modification peut faire l'objet d'un **commit**. Le commit est une étape dans l'évolution du projet, on peut revenir à une étape, une copie antérieur grâce à l'ID associé à chaque commit. S'il y a un problème le développeur peut revenir à une version fonctionnelle. Dans un projet collaboratif cela permet de conserver la version de chaque développeur et de les fusionner sans perdre les améliorations de chacun. S'il y a un problème des outils permettent de régler les conflits, VS Code en propose un par exemple.  
Autre avantage déterminant de Git est le stockage du code. Celui-ci est de base en peer to peer, chaque membre du projet possède une copie. La multiplicité des stockages protège des défaillances isolées.  
  
GitHub est une plateforme en ligne de développement collaboratif qui suppléé Git. GitHub Rajoute un cloud sur lequel laisser le repo en plus du peer to peer de Git., accessible à des développeurs désignés. Elle est aussi utilisée comme plateforme de documentation avec sa visualisation des MarkDown et la création d'un Wiki. Le site propose gratuitement un workflow avec un suivi de projet, des issues, des insights. 

## Le suivi de changements dans le dépôt local

![changements1](https://github.com/LYQA-Corporation/projetLYQA-Versioning/blob/main/notes_arthur/images/changements1.png)
![changements2](https://github.com/LYQA-Corporation/projetLYQA-Versioning/blob/main/notes_arthur/images/changements2.png)
<div style="text-align:center"><img src="https://github.com/LYQA-Corporation/projetLYQA-Versioning/blob/main/notes_arthur/images/branches.png" /></div>.
![branches](https://github.com/LYQA-Corporation/projetLYQA-Versioning/blob/main/notes_arthur/images/branches.png)
## Les commandes
Pour connaître les commandes Git les plus communes il suffit d'écrire dans le shell :  
```
git --help
```  
Sur GitBash cela donne :  
```bash
$ git --help
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]    
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]       
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one   

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
```  
  
Nous allons voir seulement les commandes que j'ai pu utiliser en cours :    
  
```bash
git init
```  
Cette commande créé un nouveau dépôt Git. ou en réinitialise un.  
  
```bash
git status
```  
Montre l'état actuel du dépôt Git. local.  
  
```bash
git pull
```  
Récupère les évolutions du dépôt distant et les intègre au dpôt local.  
  
```bash
git commit
```  
Créé une instance du dépôt local à partir des modifications enregistrées dans l'index. Le commit est toujours suivi d'un message.  
  
```bash
git commit -m ""
```  
Créé un commit avec un message associé écrit à la suite.
  
```bash
git fetch
```  
Récupère l'historique des évolutions du projet sans pour autant le merge.  
  
```bash
git push
```  
Envoie les commits locaux dans le dépôt distant.
  
```bash
git clone
```  
Récupère un autre dépôt ainsi que toutes ses évolutions dans un nouveau dossier.  
  
```bash
git add
```  
Ajoute les récents changements dans l'index.  
  
```bash
git branch
```  
Sert à gérer les branches, les créer, les lister ou les effacer. Il est possible de créer une branche avec ***git checkout***  
  
```bash
git diff
```  
Sert à montrer les différents changements, très utile pour résoudre les conflits entre le dépôt distant et le dépôt local.  
  
```bash
git remote
```  
Permet de gérer la connexion avec d'autres dépôts.  
  
```bash
git push -u origin main
```  

```bash
echo "#texte" >> README.md
```  
Créé un fichier README.md dans lequel est écrit un texte.  
  
```bash
rm -rf .git/
```  
Efface le dossier .git et toutes les données conservées en local. Le -r sert est pour recursive, cela permet d'effacer tout le contenu, le f permet de forcer la commande.  
  
```bash
git log
```  
Montre les commits. La commande peut être agrémentée pour rendre plus lisible le résultat comme par exemple montrer l'évolution des branches:  
```bash
git log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
```  
```bash
* 693e3a6 - (3 days ago) mergin - arthur-herve (HEAD -> main)
* 88b64f2 - (4 days ago) ^Z^Z^Z² - arthur-herve (origin/main, feature-2)
* 9016979 - (4 days ago) .gitignore added - arthur-herve
* 9c010a9 - (4 days ago) "deleted created text.txt file" - arthur-herve
* 578575b - (4 days ago) commit message - arthur-herve
* fa064ed - (4 days ago)  src refspec main does not match any - arthur-herve
* 315680a - (4 days ago) modified README.md - arthur-herve
* 234000b - (4 days ago) Create README.md - arthur-herve
*   58fb377 - (4 days ago) Merge branch 'main' of github.com:arthur-herve/projetGroupeVersioning - arthur-herve
|\
| * e57d62f - (7 days ago) Initial commit - arthur-herve
* f7c863d - (7 days ago) first commit - arthur-herve
```  
Ou bien simplement mettre en ligne les commits :  
```bash
git log --pretty=oneline
693e3a64a9f7878c0a1ef5ef5b4c0a1b4ca6f063 (HEAD -> main) mergin
88b64f213bf908fb51c947a3d4a6f8c12d914e3d (origin/main, feature-2) ^Z^Z^Z²
9016979e33ad295f2d1388c73d1d09e19adce41a .gitignore added
9c010a93916be99b43abfce888d0da02ec856da3 "deleted created text.txt file"
578575b04f4c331cc5d32a981cae367aeb000631 commit message
fa064ed2ce5d187c138c6ac93949a5d7e429031c  src refspec main does not match any
315680aa6f1f38bf11a870a46ccfd2cd1470a988 modified README.md
234000be2eede7f87e14da99c43530219284c2dd Create README.md
58fb377725caf3e4d499b8f19dc7a3c4727bfc1b Merge branch 'main' of github.com:arthur-herve/projetGroupeVersioning
f7c863d8681713e04a7e5109dcb1ac153667309f first commit
e57d62f58b21a9be3b0a77dc0ef777ed4142ce34 Initial commit

```  
## Création d'un reposite sur GitHub
Après avoir terminé la création du dépôt distant en suivant les formulaires de GitHub, il est conseillé par le site de réaliser les commandes suivantes en local sur Git Bash:  
```bash
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/arthur-herve/test.git
git push -u origin main
``` 
Cela créé un fichier markdown contenant un texte, initialise le dépôt git en local, ajoute à l'index la création du markdown, fait un premier commit, force à renommer une branche en *main*, récupère en https le lien vers le dépôt distant sous le nom d'*origin*, envoie les changements à la branche *main* du dépôt distant identifié par *origin* tout en demandant un suivi de la branche *main* distante. 
```bash
git remote add origin https://github.com/arthur-herve/test.git
git branch -M main
git push -u origin main
```
Reprend les trois dernières étapes des commandes précédentes en commençant par la connexion pour renommer après coup la branche *master* en branche *main*.

## Documentation :  
 [Documentation Git en anglais - site officiel] (https://git-scm.com/docs/git)  
> *Cette documentation est accessible pour chaque commande grâce à la commande ***git #nom_de_la_commande# --help***.*  

 [Documentation Git en français] (https://www.hostinger.fr/tutoriels/commandes-git#Git_config)

