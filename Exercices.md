# Neufplate™

Vous travaillez pour l'entreprise `Neufplate™` . 

C'est votre 1er jours et vous travailler en tant que developpeur dans cette entreprise et vous avez envie de faire vos preuves. 
Armé de vos connaissance vous avez à coeur de programmer de la façon la plus propre possible. 
C'est pourquoi dès que possible vous utilisez les design patterns et autres bonne pratique de developpement.

L'entreprise vous lance un challenge de taille :

En effet, jusqu'a maintenant l'entreprise se contenté de simplement voler les illustrations des autres, mais on lui récémment appris que cette pratique est illégale.
 
C'est alors que `Neufplate™` à une idée totalement inédite !
Elle va générer des avatars unique de façon aléatoire en fonction d'une chaine de caractères appellé `seed`.

Avec un peu de chance elle pourra même vendre ses avatars comme-ci ils étaient côté en bourse.

## 1 - Le singleton

Vous devez créer pour votre entreprise une classe qui fera des appels à une API de façon régulière.

Voici la documentation de l’api : `https://avatars.dicebear.com/docs`

L’objectif est de créer une classe `DiceBearApi` avec une méthode `getRandomAvatar()` qui permet d’afficher une url qui ressemble à : 

`https://avatars.dicebear.com/api/:sprites/:seed.svg`

Le type de sprite doit être choisi une et une seule fois à l’initialisation de la classe.
Ainsi, tous les appels à la classe `DiceBearApi` doivent retourner le même type de sprite. 
La classe `DiceBearApi` peut être appelé de n’importe ou sans initialisation et sans aucun paramêtre.

L’élement ‘seed’ quant à lui est alétoirement généré à chaque appel de la fonction `GetRandomAvatar()`.

Utilisez le design pattern du singleton pour résoudre ce problème.

## 2 - Factory 


La 1er version de votre générateur d’avatar vous convenait très bien jusque la.
D’ailleurs cela à tellement de succès que l’on vous demande si il est possible d'ajouter d’autre fournisseur d’avatar.

Nous ne pouvons pas ajouter du code à la classe déjà existante car ce n’est pas la même API et que ne nous voulons pas complexifier le code existant.

En utilisant le patron de conception Factory vous devez créer le code qui permettra indifféremment de généré un avatar quel que soit le fournisseur que l’ont choisi.

`https://robohash.org/:seed.png`

## 3 - Builder

Vous décidez de créer des profils utilisateurs afin de mieux trairer les demande de génération d'avatar.

Problème : Tous les champs sont optionnels sauf le nom et le prénom !

```java
public class User {
    private String firstName;    //required
    private String lastName;    //required
    private int age;    //optional
    private String phone;    //optional
    private String address;    //optional
...
}
```

Utilisez le design pattern builder pour résoudre ce problème.
