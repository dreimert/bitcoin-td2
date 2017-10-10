# TD2 Bitcoin

## Docker

## Comprendre ce qu'il se passe

Lisez l'ancienne version de ce TD à l'adresse suivante https://sfrenot.jumplyn.com/install/ ainsi que le fichier Dockerfile de ce dépôt.

### Q1.* : Répondez aux questions de l'ancienne version.

## Ma première compilation des sources de Bitcoin

Vous ne connaissez pas Docker ?

* le site : https://www.docker.com/
* la doc en ligne : https://docs.docker.com/
* via le CLI : `docker --help`

### Q2 : Qu'est ce que Docker ?

### Q3 : À votre avis, pourquoi pour ce TD je vous fais utiliser Docker ?

### QBonus 1 : Pourquoi dans le Dockerfile à la ligne 45, j'ai écrit : exit 0 ?

Vous avez un ficher Dockerfile qui décrit une chaine de compilation. Il faut maintenant construire l'image.

    docker build -t bitcoin .

### Q4 : Décrivez ce qu'il se passe.
### Q5 : Que fait `docker build` ? Vous avez le temps de creuser et détailler la question normalement :)

### QBonus 2 : J'aurais pu être plus sympa avec vous et vous faire gagner du temps. Comment ?

## Jouer avec Docker

Votre build est fini ? Maintenant, il faut lancer un *container* avec votre image !

    docker run -it dreimert/bitcoin-td2:main bash

### Q6 : Que fait `docker run` ?
### Q7 : À quoi sert les options `-it` ?

Vous êtes dans la matrice, pardon... le *container*. Vous devez voir le code source  de bitcoin et les exécutables.

### Q8 : Où sont les exécutables de Bitcoin ?
### Q9 : Comment lancer le démon Bitcoin ?

Lancer le démon, n'oubliez pas les options qui vont bien pour voir ce qu'il se passe.

Vous avez envi d'avoir plusieurs terminaux sur votre machine ?

### Q10 : À quoi sert `docker ps` ?
### Q11 : Comment utiliser `docker exec` pour obtenir plusieurs terminaux ?

## Préparer le TP

Le but de ce TD est de préparer le TP où vous allez modifier le code source de Bitcoin pour créer votre propre blockchain.

Vous aimez vim ou emacs comme IDE ? Tant mieux ! Vous n'aimez pas ? Arf... Ya peut-être une solution, ça s'appelle les volumes mais ça ne fonctionne pas comme vous voulez dans ce cas. Enfin, il y a un moyen simple de contourner le problème, simple comme `cp`.

### Q12 : À quoi sert l'option `-v` de `docker run ` ?

## Jouons avec nos voisins comme au TD 1

Maintenant, vous avez envie de vous connecter à votre voisin ? Essayer !

### Q13 : Pourquoi cela ne marche pas ?
### Q14 : Dans `docker run` à quoi sert l'option `-p` ?

## Jouons tout seul

L'avantage avec docker, c'est que s'est facile de faire plusieurs machines et de les communiquer entre elles. Mais la syntaxe pour le faire est un peu chiante. Du coup, il y docker-compose qui permet dans un fichier de décrire les différentes machines, binder des volumes ou encore de toutes les mettre sur le même réseau.

Vous avez fini le TD ? Vous avez lu le paragraphe précédent ? Bonne chance ^^
