# Notes de cours et rapport - Arthur Hervé
**Comme convenu par message Discord, mon rapport personnel sera remis plus tard dans la semaine du 26 septembre.**  
**Le rapport de groupe est de son côté rendu le 25 septembre**
## Rapide présentation de GitHub

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
  
Nous allons voir seulement les commandes que j'ai pu utiliser en cours.  
  
```bash
git init
```  
```bash
git status
```  
```bash
git pull
```  
```bash
git commit
```  
```bash
git commit -m ""
```  
```bash
git fetch
```  
```bash
git push
```  
```bash
git clone
```  
```bash
git add
```  
```bash
git branch
```  
```bash
git diff
```  
```bash
git remote
```  
```bash
git push -u origin main
```  
```bash
git 
```  
```bash
echo "#texte" >> README.md
```  
```bash
rm -rf .git/
```  
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
  


> Documentation :  
> [Documentation Git en anglais - site officiel] (https://git-scm.com/docs/git)  
>> *Cette documentation est accessible pour chaque commande grâce à la commande ***git #nom_de_la_commande# --help***.*
> [Documentation Git en français] (https://www.hostinger.fr/tutoriels/commandes-git#Git_config)
#### Remarques

