function analyzeSentence(sentence) {
       // Initialiser les compteurs
    let length = 0;
    let wordCount = 0;
    let vowelCount = 0;
    
    // Parcourir chaque caractère de la phrase
    for (let i = 0; i < sentence.length; i++) {
        // Incrémenter le compteur de longueur pour chaque caractère
        length++;
        
        //  Vérifier si le caractère est un espace pour compter les mots
        if (sentence[i] === ' ') {
            wordCount++;
        }
        
        // Vérifier si le caractère est une voyelle (en considérant les majuscules et minuscules)
        if (/[aeiou]/i.test(sentence[i])) {
            vowelCount++;
        }
    }
    
    // Incrémenter le nombre de mots pour le dernier mot (puisque la phrase se termine par un point)
    wordCount++;
    
    // Afficher les résultats
    console.log("Length of the sentence:", length);
    console.log("Number of words in the sentence:", wordCount);
    console.log("Number of vowels in the sentence:", vowelCount);
}

// Tester la fonction
const sentence = "Hello, this is a test sentence.";
analyzeSentence(sentence);


/*Ce code JavaScript définit une fonction analyzeSentence() 
qui prend une phrase en entrée. Il parcourt chaque caractère de la phrase, 
incrémentant les compteurs appropriés en fonction des conditions spécifiées. 
Enfin, il affiche la longueur de la phrase, le nombre de mots 
et le nombre de voyelles dans la console. */
