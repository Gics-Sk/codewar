## Explication de l'exercice
Fonction dnaStrand : Cette fonction prend une chaîne de caractères dna en entrée et renvoie une chaîne de caractères correspondant à la séquence complémentaire.

Initialisation du tableau result : Un tableau vide est créé pour stocker les caractères de la séquence complémentaire.

Boucle for : La boucle parcourt chaque caractère de la chaîne dna à l'aide de l'indice index.

Instruction switch : Elle est utilisée pour comparer chaque caractère (dna[index]) avec les caractères valides "A", "T", "C", "G".

Cas pour chaque nucléotide :

- Si le caractère est "A", on ajoute "T" à result.
- Si le caractère est "T", on ajoute "A" à result.
- Si le caractère est "C", on ajoute "G" à result.
- Si le caractère est "G", on ajoute "C" à result.
- Si le caractère est autre que ceux-ci, un message d'erreur est affiché dans la console.
Transformation et retour : À la fin de la boucle, result est transformé en une chaîne de caractères à l'aide de join("") et cette chaîne est retournée comme résultat de la fonction.
````js
// Définition de la fonction dnaStrand qui prend une chaîne de caractères DNA en entrée
function dnaStrand(dna) {
    // Initialisation d'un tableau vide pour stocker le résultat final
    let result = [];

    // Parcours de chaque caractère de la chaîne DNA en utilisant une boucle for
    for (let index = 0; index < dna.length; index++) {
        // Utilisation d'une instruction switch pour vérifier chaque caractère
        switch (dna[index]) {
            // Si le caractère est "A", on ajoute "T" au tableau result
            case "A":
                result.push("T");
                break;
            // Si le caractère est "T", on ajoute "A" au tableau result
            case "T":
                result.push("A");
                break;
            // Si le caractère est "C", on ajoute "G" au tableau result
            case "C":
                result.push("G");
                break;
            // Si le caractère est "G", on ajoute "C" au tableau result
            case "G":
                result.push("C");
                break;
            // Si le caractère est autre que les lettres valides (A, T, C, G), on affiche un message d'erreur dans la console
            default:
                console.log("Caractère invalide trouvé dans la chaîne DNA");
                break;
        }
    }

    // Transformation du tableau result en une chaîne de caractères et retour de cette chaîne
    return result.join("");
}



