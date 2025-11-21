Fonctions

Une fonction est un bloc de code qu’on peut réutiliser.
Il existe plusieurs manières d’écrire une fonction.

Déclaration de fonction :

function calculPrix(nb, prix) {
  return nb * prix;
}


Expression de fonction :

const calculPrix = function(nb, prix) {
  return nb * prix;
};


Fonction fléchée :

const calculPrix = (nb, prix) => nb * prix;


Exemple dans un système de réservation :

function creerReservation(nom, destination) {
  return { nom: nom, destination: destination };
}