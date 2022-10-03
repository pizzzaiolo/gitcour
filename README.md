# Exemple pour le cours versioning de code - l'outil Git
## EFREI 03/10/2022

# Titre H1
## Titre H2
### Titre H3
#### Titre H4
##### Titre H5
###### Titre H6

_Je suis un super paragraphe en italique_\
_avec retour à la ligne_\
**Je suis un paragraphe en gras.**

| Syntax    | Description | Test  |
| :-------- | :---------: | ----: |
| Header    | Title       | Texte |
| Texte exemple aligné à gauche | Texte exemple centré | Texte exemple aligné à droite |

## Fonctionnement

Afin de pouvoir faire fonctionner ce projet, vous devrez créer, à la racine du dossier parent, un fichier secret.txt contenant les client_secret et client_key.

## Résumé matinée

| Commande | Options | Fonction |
| :------ | :-----: | :------: |
| git init | | Initialiser un projet Git |
| git config user.email | | Définir l'e-mail de l'utilisateur courant pour Git |
| git config user.name | | Définir le nom de l'utilisateur courant pour Git |
| git status | | Afficher le statut actuel de la branche courante |
| git add | | "Stage" un ou plusieurs fichiers |
| git commit | --amend | Modifier le message du dernier commit |
| git commit | -m | Ajouter un message au commit en ligne de commande |
| git tag | [-a, -m, -d, -f] [commit or tag number] | Ajouter, supprimer ou déplacer un tag sur un commit donné |
| git show | [commit number] | Afficher les informations relatives à un commit donné |
| git diff | [file] | Afficher les changements entre maintenant et le dernier commit sur un ou tous les fichiers |
| git log | | Afficher la liste des commits sur la branche actuelle |
| git reset | --soft, --hard | Revenir à un état précédent de notre code projet |
| git ls-files | | Liste les fichiers suivis par Git |
| git rm | --cached | | Retirer un ou plusieurs fichiers de l'historique de suivi de Git |
| git restore | --staged | | Unstage un ou plusieurs fichiers |
| git branch | -M, -d, -a (--all) | Créer ou renommer une branche de travail |
| git checkout | -b | (Créer si l'option -b a été donnée et) Se positionner sur une branche de travail |
| git merge | | Permet de fusionner l'historique Git de deux branches |
| git remote add <alias> <url dépôt distant> | | Ajoute un alias lié à une URL de dépôt distant |
| git remote | -v | Lister les différentes origines distantes |
| git pull [<alias> <branche>] | -u (--set-upstream) | Récupérer les infos d'une branche distante et les fusionner avec la branche courante (équivalent git fetch + git merge) |
| git push [<alias> <branche>] | -u (--set-upstream) | Envoi le code source et l'historique des versions sur le dépôt distant mentionné
| git stash | | Retire et stocke en mémoire les changements non commités de la branche actuelle |
| git stash apply | | Applique les changements du dernier patch sur la branche courante |

## Création d'un compte GitHub

Aller sur [github](https://github.com/) et cliquer sur "Sign up" pour lancer le processus de création de compte.

## Génération d'une clé SSH
```bash
ssh-keygen
```

Laisser les valeurs par défaut (appuyer plusieurs fois sur la touche Entrée.

Localiser la clé publique (par défaut : C:\Users\<username>\.ssh\) et copier le contenu du fichier id_rsa.pub.

Aller sur github dans les paramètres du compte (icône du compte en haut à droite de l'écran d'accueil >> settings >> SSH and GPG keys >> New SSH Key) et ajouter la clé nouvellement créée et copiée.

## Exercice 

Dans une autre branche que main, appliquer des modifications sur le fichier README.md ou tout autre fichier.

Envoyer les modifications sur votre dépôt distant.

Revenir sur la branche 'main', et utiliser les commandes suivantes :

```
git fetch origin <branche>
git merge FETCH_HEAD
```

Les deux commandes suivantes sont équivalentes à utiliser la commande :

```
git pull origin <branche>
```
