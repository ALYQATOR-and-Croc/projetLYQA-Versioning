# projetLYQA-Versioning

## Participants :
- Yoann VINCENT
- Quentin MOREL
- Arthur HERVE
- Luigi AUBRY--POUGET

## But du projet

Ajouter quelques features à un site vitrine (copie d'Amazon).

## Fonctionnement du site



## Démarche
### Prise d'informations
- Lecture du sujet
- Lecture des articles :  
> [A Beginner’s Guide to Git] (https://www.freecodecamp.org/news/a-beginners-guide-to-git-what-is-a-changelog-and-how-to-generate-it/)  
> [Conventional commits : Détails & examples pratiques] https://les-enovateurs.com/conventional-commits-details-exemples-pratiques  
> [Conventional Commits, a specification for adding human and machine readable meaning to commit messages] https://www.conventionalcommits.org/en/v1.0.0-beta.4/  
### Installation du workflow et prise en main du GitHub
- Création du repo sur le GitHub de Luigi
- Recherche du template
- Création d'une organisation regroupant les 4 membres du groupe : **LYQA-Corporation**
- Import du template sur le repo du GitHub de Luigi avec les commantes ***git add***, ***git commit***, ***git pull*** et ***git push***
- La création de l'organisation terminée, import du repo de Luigi sur **LYQA-Corporation**
- Création du Projects **@arthur-herve - LYQA web** renommé plus tard **Suivi - LYQA web**
- Disposition du Projects sous forme de Board comme Trello et non de Table car l'équipe trouvait cela plus évocateur.
- Mise en place de l'onglet General en 4 colonnes **Todo**, **In Progress**, **To Merge** et **Done** pour le suivi des actions de chacun.

### Répartition des tâches et création des branches
- Récupération d'une copie locale du repo pour chaque membre de l'équipe avec ***git clone***
- Lecture du code et division du travail entre changement du style dans le css pour Luigi, création d'une nouvelle page pour Quentin, traduction de la page pou Yoann et changement d'images et génération d'une bannière promotionnelle pour Arthur.
- A l'aide de la commande ***git checkout -b #nom_de_la_nouvelle_branche***, création de nouvelles branches. Cette commande en particulier permet de créer une nouvelle branche à partir de la branche dans laquelle la commande a été effectuée.
- Création d'une branche de développement **develop**, de trois branches de travail, une pour la nouvelle page **dev_new_page**, une pour traiter css **dev_stylesheet** et une pour la traduction et la modification des médias **dev_mainpage**.

### Add, commit, pull et push
- La mise à jour régulière de nos branches de travail sur nos repo locaux passe par un ***git add*** puis un ***git commit*** pour conserver nos changements. Puis nous effectuons un ***git pull*** de mise à jour avant de push pour détecter et gérer les conflits depuis notre repo local.
- Utilisation de l'interface de résolution des conflits de **VS Code** pour faire correspondre les changements de Yoann et Arthur.
- Lorsque nous avons convenu d'un nombre suffisant de modifications sur le template pour en faire une version nous avons débuté la fusion des branches.

### Fusion et version
- Fusion de la branch **dev_mainpage** avec la branche **develop** avec la commande ***git merge***.
- Après un pull sur le repo local de Luigi, merge de la branche **dev_stylesheet** avec la branche **develop**.
- Après un pull sur le repo local de Quentin, merge de la branche **dev_new_page** avec la branche **develop**.
- Utilisation de l'interface de résolution des conflits de **VS Code** pour faire correspondre les changements de la branche **develop** avec la branche **dev_new_page**.
- A chaque étape vérification de la présence des changements.
- Merge de la branche de production **main** avec la branche **develop**.
- Tag de la nouvelle version de production avec la commande ***git tag v1.0*** puis ***git push v1.0*** pour que celui-ci soit effectif.  
> *Le tag permet d'étiqueter des points d'arrêt dans le versionning.*  
> *La commande ***git push*** seule ne permet de mettre à jour la version sur le repo distant, il est nécessaire de la compléter en faisant : ***git push #nouveau_tag#*** *   

### Fichier traçant les log avec le fichier CHANGELOG.md
- L'ensemble des commits fait par les membres du groupe est tracé sous forme de log. La commande **git log** permet de les voir, il est intéressant de rajouter des paramètres pour que l'affichage soit plus lisible.
- Recherche d'une librairie automatisant la création du fichier CHANGELOG.md.
- Npm propose un package auto-changelog permettant de répondre à notre besoin.
- Installation du package avec la commande ***npm install -g auto-changelog***.
- Dans la page main création du fichier CHANGELOG.md avec la commande ***autochangelog -l 100***  
> *La commande ***autochangelog*** ne retrace que les trois derniers commit, il faut ajouter le ***-l #nombre de log#*** pour en obtenir plus. pour plus d'informations voir la documentation sur [NPM - auto-changelog] (https://www.npmjs.com/package/auto-changelog/)*

## Outils
> *Pour toute information la première référence est la documentation de git que l'on peut ouvrir avec la commande ***git #commande spécifique# --help***.*  
> *Les autres informations viennent principalement de [stack overflow] (https://stackoverflow.com)*


***nb: le README.md a reçu des commits en même temps que nous avancions sur la documentation.***