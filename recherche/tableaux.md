forEach

Définition : permet de faire une action sur chaque élément du tableau.
Retour : ne retourne rien.
Quand l’utiliser : quand on veut juste parcourir.
Exemple :

reservations.forEach(function(r) {
    console.log(r.nom);
});

map

Définition : crée un nouveau tableau avec une transformation.
Retour : retourne un nouveau tableau.
Quand l’utiliser : quand on veut modifier les valeurs.
Exemple :

let noms = reservations.map(function(r) {
    return r.nom;
});

filter

Définition : garde seulement les éléments qui respectent une condition.
Retour : retourne un tableau filtré.
Quand l’utiliser : quand on veut sélectionner certains éléments.
Exemple :

let adultes = reservations.filter(function(r) {
    return r.age >= 18;
});

Exemples dans un système de réservation
Exemple forEach

Afficher les destinations :

reservations.forEach(function(r) {
    console.log(r.destination);
});

Exemple map

Créer un tableau avec seulement les prix :

let prix = reservations.map(function(r) {
    return r.prix;
});

Exemple filter

Récupérer les réservations pour Mars :

let mars = reservations.filter(function(r) {
    return r.destination === "Mars";
});

find

Définition : trouve le premier élément qui respecte une condition.
Retour : retourne l’élément trouvé ou undefined.
Quand l’utiliser : quand on cherche un seul élément.

Exemple pour trouver une réservation par ID :

let r = reservations.find(function(item) {
    return item.id === 5;
});

findIndex

Définition : trouve l’index du premier élément qui respecte une condition.
Retour : retourne l’index ou -1.
Quand l’utiliser : quand on veut modifier ou supprimer un élément.

Exemple :

let index = reservations.findIndex(function(item) {
    return item.id === 5;
});

Cas d’utilisation pratiques

Trouver une réservation annulée :

let annulee = reservations.find(function(r) {
    return r.status === "annulée";
});


Trouver l’index d’une réservation pour la mettre à jour :

let pos = reservations.findIndex(function(r) {
    return r.nom === "Ali";
});

reduce

Définition : accumule des valeurs pour obtenir un résultat final.
Retour : retourne une valeur unique.
Quand l’utiliser : pour faire un total, une somme, un calcul.

Calculer le revenu total des réservations
let total = reservations.reduce(function(acc, r) {
    return acc + r.prix;
}, 0);

Exemple avec données de réservation
let reservations = [
    { id: 1, nom: "Ali", prix: 200 },
    { id: 2, nom: "Sara", prix: 300 },
    { id: 3, nom: "Lina", prix: 150 }
];

let total = reservations.reduce(function(acc, r) {
    return acc + r.prix;
}, 0);