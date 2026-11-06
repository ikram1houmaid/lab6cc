# TP C++ : Héritage et Polymorphisme

## Présentation du TP

Ce TP a pour objectif de mettre en pratique les concepts fondamentaux de la programmation orientée objet (POO) en C++.

Les exercices permettent de comprendre et d'utiliser l'héritage, les constructeurs, les méthodes virtuelles, le polymorphisme et la gestion dynamique de la mémoire.

**Langage utilisé :** C++  
**Environnement de développement :** Eclipse IDE  
**Paradigme :** Programmation Orientée Objet (POO)

---

## Structure du projet

Le projet contient quatre exercices indépendants :

```text
TP_Heritage_Polymorphisme/
│
├── Exercice1_Personne_Etudiant/
│   └── main.cpp
│
├── Exercice2_Compte_Bancaire/
│   └── main.cpp
│
├── Exercice3_Hierarchie_Produits/
│   └── main.cpp
│
├── Exercice4_Gestion_Employes/
│   └── main.cpp
│
└── README.md
```

---

## Exercice 1 : Classe Personne et Etudiant

### Objectif
Comprendre le principe de l'héritage simple en C++ et apprendre à réutiliser les attributs et les méthodes d'une classe de base.

### Description
Création de deux classes :

- **Personne :** contient les attributs `nom` et `age`, ainsi qu'une méthode `afficher()`.
- **Etudiant :** hérite publiquement de `Personne` et ajoute l'attribut `niveau`.

La classe `Etudiant` redéfinit la méthode `afficher()` pour afficher toutes les informations de l'étudiant.

### Notions utilisées
- Création de classes et d'objets.
- Héritage public avec `public`.
- Attributs protégés avec `protected`.
- Constructeurs.
- Appel du constructeur de la classe mère.
- Réutilisation des méthodes de la classe de base.

### Résultat attendu
Afficher le nom, l'âge et le niveau d'un étudiant.

---

## Exercice 2 : Compte bancaire

### Objectif
Appliquer l'héritage public et comprendre comment une classe dérivée peut réutiliser les fonctionnalités d'une classe de base tout en ajoutant ses propres méthodes.

### Description
Création de deux classes :

- **Compte :** contient les attributs `numero` et `solde`, ainsi que les méthodes `deposer()` et `retirer()`.
- **CompteEpargne :** hérite de `Compte` et ajoute l'attribut `tauxInteret` et la méthode `calculerInteret()`.

La classe `CompteEpargne` permet d'effectuer des dépôts, des retraits et de calculer les intérêts du compte.

### Notions utilisées
- Héritage public.
- Constructeurs avec paramètres.
- Appel du constructeur de la classe mère.
- Réutilisation des méthodes héritées.
- Calcul et mise à jour du solde.
- Vérification des opérations bancaires.

### Résultat attendu
Créer un compte épargne, effectuer un dépôt, effectuer un retrait, calculer les intérêts et afficher le solde final.

---

## Exercice 3 : Hiérarchie de produits

### Objectif
Comprendre les méthodes virtuelles et leur redéfinition dans les classes dérivées afin d'introduire le polymorphisme en C++.

### Description
Création d'une classe de base et de deux classes dérivées :

- **Produit :** contient les attributs `nom` et `prix`, ainsi qu'une méthode virtuelle `afficherInfos()`.
- **ProduitAlimentaire :** hérite de `Produit` et ajoute l'attribut `dateExpiration`.
- **ProduitElectronique :** hérite de `Produit` et ajoute l'attribut `garantie`.

Chaque classe dérivée redéfinit la méthode `afficherInfos()` pour afficher ses propres informations.

### Notions utilisées
- Héritage simple.
- Méthodes virtuelles avec `virtual`.
- Redéfinition avec `override`.
- Appel d'une méthode de la classe mère avec `Produit::afficherInfos()`.
- Destructeur virtuel.

### Résultat attendu
Créer un produit alimentaire et un produit électronique, puis afficher toutes leurs informations.

---

## Exercice 4 : Système de gestion d'employés

### Objectif
Maîtriser le polymorphisme et la gestion dynamique de plusieurs objets appartenant à différentes classes dérivées.

### Description
Création de trois classes :

- **Employe :** classe de base contenant `nom`, `id` et `salaireDeBase`, avec une méthode virtuelle `afficherInfos()`.
- **Permanent :** hérite de `Employe` et ajoute l'attribut `primeAnnuelle`.
- **Contractuel :** hérite de `Employe` et ajoute les attributs `dureeContrat` et `tauxHoraire`.

La classe `Contractuel` possède également une méthode `calculerSalaireMensuel(int heures)` permettant de calculer le salaire selon le nombre d'heures travaillées.

Dans la fonction `main()`, un tableau dynamique de pointeurs vers `Employe` permet de stocker différents types d'employés et d'afficher leurs informations grâce au polymorphisme.

### Notions utilisées
- Héritage public.
- Constructeurs des classes dérivées.
- Méthodes virtuelles et redéfinition avec `override`.
- Polymorphisme.
- Tableau dynamique de pointeurs avec `Employe**`.
- Allocation dynamique avec `new`.
- Conversion de pointeurs avec `dynamic_cast`.
- Destructeur virtuel.
- Libération de la mémoire avec `delete` et `delete[]`.

### Résultat attendu
Créer plusieurs employés permanents et contractuels, afficher leurs informations, calculer le salaire mensuel d'un contractuel et libérer correctement la mémoire.

---

## Technologies et outils utilisés

- **Langage :** C++
- **IDE :** Eclipse
- **Bibliothèques :** `iostream` et `string`
- **Concepts :** Programmation Orientée Objet (POO)

## Compilation et exécution

Chaque exercice possède son propre fichier `main.cpp`.

Pour compiler un exercice avec un compilateur C++ :

```bash
g++ main.cpp -o programme
```

Pour exécuter le programme :

```bash
./programme
```

Sous Windows :

```bash
programme.exe
```

## Conclusion générale

Ce TP m'a permis de pratiquer les principaux concepts de la programmation orientée objet en C++.

À travers ces quatre exercices, j'ai appris à :

- Créer des classes de base et des classes dérivées.
- Utiliser l'héritage public pour partager les attributs et les méthodes.
- Initialiser les classes dérivées à l'aide des constructeurs des classes mères.
- Redéfinir des méthodes virtuelles.
- Comprendre et appliquer le polymorphisme.
- Manipuler des tableaux dynamiques de pointeurs.
- Gérer correctement l'allocation et la libération de la mémoire.

Ces exercices constituent une introduction pratique à la conception de programmes orientés objet en C++.
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/2c78c847-c000-49d2-87e2-ddaab3c4c6fa" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/da8cf22e-33b0-4110-b994-2db2f0153d55" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/b0631f76-6adc-4493-bd2b-38cfcba47149" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/879dbb54-85e0-4d1c-b759-44de7e40a55b" />
