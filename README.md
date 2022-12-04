# Qu'est ce que Git ? 

un logiciel / un outil permettant de contrôler les versions d'un projet informatique

# Commande de base


Pour pouvoir récupérer un **repo** git il nous suffit d'utiliser cette commande ;
```
git clone <le lien du repo git>

```

le lien alors récuperé nous donne accès au repo et son contenu

une fois dans le **repo** nous allons rajouter un fichier *text.txt* puis nous allons l'ajouter à notre repo :
```
git add text.txt  || git add . (importe tout sans les fichiers cachés) || git add * (importe tout avec les fichiers cachés)

```
nous allons commenter puis push
```

git commit -m "add new text"

git push

```

maintenant que nous avons vu les étapes d'utilisations *simple* de git nous pouvons voir quelque utilisation plus *subtile est complexe* 

Nous permet de remettre une branche de mon dossier git à jour 
```
git pull (dans le repo git)
```

Nous permet de remettre toutes les branches de mon dossier git à jour 
```
git fetch
```


montre les branches de disponible
```
git branch (il suffit d'appuyer sur 'q' pour finaliser)
```

pour créer une branche
```
git branch test
```
si nous relançons git nous aurons le resultat suivant
```
* main (la branche déjà existante)
  test (celle que nous avons créer)
```

si nous souhaitons passer à une autre branche nous devons taper cette commande 
```
git checkout <nom_de_la_branch>
```
une fois dans cette branche nous allons push un fichier 

```
git add textDeTest.txt
git commit -m 'envoie du text'
git push --set-upstream origin test
```

le git push ici est bien différent de celui qu'on a l'haibtude d'utiliser car nou

une fois fait ceci nous pouvons changer de branche est voir que notre main est vide alors que nous venons d'envoyer un fichier
```
$>  Tuto_Git git:(test) ls
README.md        text_de_test.txt
$>  Tuto_Git git:(test) git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
$>  Tuto_Git git:(main) 

```

maintenant nous voulons envoyer contenu de la branche **main** dans la branche **test**, nous pouvons utiliser git merge 

```
➜  Tuto_Git git:(test) ls
README.md
➜  Tuto_Git git:(test) git merge main 
Updating b1a0754..a89b89c
Fast-forward
 README.md  | 7 +++++++
 text_de_test.txt | 0
 3 files changed, 7 insertions(+)
 create mode 100644 text_de_test.txt
➜  Tuto_Git git:(test) ls
README.md  text_de_test.txt 
```

une autre méthode d'utiliser le git add / git commit -m 'commentaire' / git push est de faire ceci :
```
git commit -am 'commentaire à rajouter'

```
il permet de combiner deux action en une (sinon evidemment il reste git de VScode)

