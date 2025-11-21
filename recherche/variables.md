Variables : var, let, const

Les variables servent à stocker des valeurs.
Il existe trois façons de déclarer des variables en JavaScript : var, let et const.

var : ancienne façon de déclarer. La variable peut changer et elle est accessible dans toute la fonction. On évite souvent de l'utiliser.

let : permet de déclarer une variable qui peut changer. Sa portée est limitée au bloc où elle est écrite.

const : permet de déclarer une variable qui ne change pas. On doit lui donner une valeur dès le début.

Exemples :

var destination = "Mars";
let passagers = 3;
const prix = 1500;


Types de données

En JavaScript, il y a deux catégories :
types primitifs et types référence.

Types primitifs : string, number, boolean, null, undefined, bigint, symbol.
Types référence : object, array, function.

Pour vérifier un type, on utilise typeof.

Exemples :

typeof "Mars";     // string
typeof 42;         // number
typeof true;       // boolean
typeof [];         // object
typeof {};         // object
typeof function(){};
// function

Instructions conditionnelles

if/else : permet d’exécuter du code selon une condition.

if (age >= 18) {
  console.log("ok");
} else {
  console.log("refusé");
}


switch : utile pour comparer plusieurs valeurs.

switch(destination) {
  case "Mars":
    prix = 5000;
    break;
  case "Lune":
    prix = 2000;
    break;
}


Opérateur ternaire : version courte de if/else.

const message = passagers > 0 ? "valide" : "invalide";


Utilisation dans un formulaire :

if (form.nom.value === "") {
  alert("nom obligatoire");
}