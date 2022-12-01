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

Nous permet de remettre un git à jour 
```
git pull (dans le repo git)
```

montre les branches de disponible
```
git branch (il suffit d'appuyer sur 'q' pour finaliser)
```

pour créer une branch 
```
git branch test
```
si nous relançons git nous aurons le resultat suivant
```
* main (la branch déjà existante)
  test (celle que nous avons créer)
```

si nous souhaitons passer à une autre branch nous devons taper cette commande 
```
git checkout <nom_de_la_branch>
```
une fois dans cette branch nous allons push un fichier 

```
git add textDeTest.txt
git commit -m 'envoie du text'
git push --set-upstream origin test
```

une fois fait ceci nous pouvons changer de branch est voir que notre main est vide alors que nous venons d'envoyer un fichier

