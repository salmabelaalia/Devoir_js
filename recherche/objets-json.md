Méthodes des Objets
Object.keys()

Définition : récupère toutes les clés d’un objet dans un tableau.
Syntaxe :

Object.keys(objet);


Exemple :

let reservation = { nom: "Ali", destination: "Mars", prix: 200 };
let cles = Object.keys(reservation); // ["nom", "destination", "prix"]


Cas pratique : afficher toutes les propriétés d’une réservation.

Object.values()

Définition : récupère toutes les valeurs d’un objet dans un tableau.
Syntaxe :

Object.values(objet);


Exemple :

let valeurs = Object.values(reservation); // ["Ali", "Mars", 200]


Cas pratique : calculer ou afficher les informations d’une réservation.

Object.entries()

Définition : récupère les paires clé-valeur d’un objet dans un tableau de tableaux.
Syntaxe :

Object.entries(objet);


Exemple :

let entrees = Object.entries(reservation); 
// [["nom","Ali"], ["destination","Mars"], ["prix",200]]


Cas pratique : parcourir un objet pour créer un tableau HTML avec toutes les infos.

JSON
Qu’est-ce que JSON ?

Définition : JSON (JavaScript Object Notation) est un format de texte pour stocker et échanger des données.
Exemple :

{"nom": "Ali", "destination": "Mars", "prix": 200}


Cas pratique : stocker les réservations dans le navigateur.

JSON.parse()

Définition : convertit une chaîne JSON en objet JavaScript.
Syntaxe :

let obj = JSON.parse(chaineJSON);


Exemple :

let data = '{"nom":"Ali","prix":200}';
let obj = JSON.parse(data);
console.log(obj.nom); // "Ali"


Cas pratique : récupérer les réservations depuis le localStorage.

JSON.stringify()

Définition : convertit un objet JavaScript en chaîne JSON.
Syntaxe :

let chaine = JSON.stringify(objet);


Exemple :

let reservation = { nom: "Ali", prix: 200 };
let json = JSON.stringify(reservation);
console.log(json); // '{"nom":"Ali","prix":200}'


Cas pratique : stocker un objet réservation dans le localStorage.

Utilisation dans le localStorage

localStorage ne peut stocker que des chaînes.

On utilise JSON.stringify() pour stocker et JSON.parse() pour récupérer.

Exemple :

let reservations = [
    { nom: "Ali", prix: 200 },
    { nom: "Sara", prix: 300 }
];

// Stocker
localStorage.setItem("mesReservations", JSON.stringify(reservations));

// Récupérer
let data = JSON.parse(localStorage.getItem("mesReservations"));
console.log(data[0].nom); // "Ali"


Cas pratique : sauvegarder et charger les réservations sur le navigateur pour que l’utilisateur retrouve ses données même après un rechargement de page.