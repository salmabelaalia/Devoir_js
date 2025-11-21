Sélection d'Éléments:

getElementById

Définition : permet de prendre un élément avec son id.
Syntaxe : document.getElementById("id");
Quand l’utiliser : quand l’élément a un id unique.
Exemple : let titre = document.getElementById("titre");

querySelector

Définition : permet de prendre le premier élément qui correspond à un sélecteur.
Syntaxe : document.querySelector("selecteur");
Quand l’utiliser : quand on veut une classe, une balise ou un id.
Exemple : let champ = document.querySelector(".input-nom");

querySelectorAll
Définition : permet de prendre tous les éléments qui correspondent à un sélecteur.
Syntaxe : document.querySelectorAll("selecteur");
Quand l’utiliser : quand il y a plusieurs éléments pareils.
Exemple : let tous = document.querySelectorAll(".passager");

Gestion des Événements
addEventListener

Définition : sert à écouter un événement.
Syntaxe : element.addEventListener("evenement", fonction);
Exemple : btn.addEventListener("click", function() {});

Événements courants

click : quand on clique.
btn.addEventListener("click", function() {});
submit : quand on envoie un formulaire.
form.addEventListener("submit", function(e) {});
input : quand on écrit dans un champ.
nom.addEventListener("input", function() {});
change : quand la valeur change.

select.addEventListener("change", function() {});

Empêcher le comportement par défaut

On utilise preventDefault sur l’événement.
Syntaxe :

form.addEventListener("submit", function(e) {
    e.preventDefault();
});

Création et Modification d’Éléments
createElement

Définition : crée un élément HTML.
Syntaxe : let div = document.createElement("div");

appendChild

Définition : ajoute un élément dans un autre.
Syntaxe : parent.appendChild(enfant);

innerHTML

Définition : change le contenu HTML.
Syntaxe : element.innerHTML = "texte";

Exemple : ajouter des passagers dans un formulaire de réservation
let zone = document.getElementById("zonePassagers");
let bouton = document.getElementById("ajoutPassager");

bouton.addEventListener("click", function() {
    let div = document.createElement("div");
    div.className = "passager";

    div.innerHTML = `
        <input type="text" placeholder="nom du passager">
        <input type="number" placeholder="age">
    `;

    zone.appendChild(div);
});