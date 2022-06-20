# Fiche d'exercices 1

{{ initexo(0) }}

## Préquel : Affichage

En général, lorsqu'un développeur apprend un nouveau langage de programmation, la première chose qu'il fait, c'est d'afficher le texte "Hello World!"...

=== "Version 1"
    ```python linenums='1'
    print("Hello World!")
    ```

=== "Version 2"
    ```python linenums='1'
    texte = "Hello World!"
    print(texte)
    ```

## S01E01: la variable

La différence entre les deux programmes précédents, c'est qu'au premier on a affiché directement un texte (on dit plutôt une *chaîne de caractères*) à l'aide de la fonction `print()`, alors que dans le deuxième on a d'abord stocké cette chaîne de caractères dans une variable nommée `texte` (on dit qu'on a *affecté* la valeur `"Hello World!"` à la variable `texte` à l'aide de l'opérateur `=`).

!!! warning "Attention"
    Notez la présence **indispensable** de guillemets pour différencier une chaine de caractères d'un nom de variable (ou d'un mot-clé du langage).

    Tester et observer le code suivant:
    ```python linenums='1'
    groot  = "toto"
    print("Je s'appelle", "groot")
    print("Je s'appelle", groot)
    ```
    

!!! example "{{ exercice() }}"
    === "Énoncé" 
        Affecter à la variable `prenom` la chaîne de caractère correspondant ... à votre prénom, puis exécuter la cellule.

        ```python linenums='1'
        prenom = 
        print("Je m'appelle", prenom)
        ```
        
    === "Indication" 
        {{ correction(True, 
        "
        Si vous avez eu une erreur de type `NameError`, c'est que vous avez oublié les guillemets. Ils sont essentiels, pour faire la différence entre une chaîne de caractères et le nom d'une variable.
        "
        ) }}

!!! example "{{ exercice() }}"
    === "Énoncé" 
        La plupart du temps, on n'utilisera pas des chaînes de caractères, mais plutôt des nombres.

        ```python linenums='1'
        a = 18         # on affecte la valeur (numérique) 18 à la variable nommée a
        b = 4 + 2 * 10 # on affecte le résultat du calcul 4 + 2 * 10 à la variable b (* signifie 'fois')
        print(a)
        print(b)
        ```

        Écrire un programme où:

        - on affectera la valeur 10 à une variable `x`;
        - on affectera la valeur 20 à une variable `y`;
        - on affichera la somme des deux variables

        En changeant ensuite **uniquement la valeur de `x`**, et en éxécutant à nouveau la cellule, la somme doit s'actualiser automatiquement.
        
    === "Correction" 
        {{ correction(True, 
        "
        ```python linenums='1'
        x = 10
        y = 20
        print(x+y)
        ```
        
        "
        ) }}

!!! example "{{ exercice() }}"
    === "Énoncé" 
        Lire les programmes ci-dessous, et essayer de deviner ce qu'ils afficheront lors de l'exécution. Vérifier en les exécutant.

        === "Programme 1"
            ```python linenums='1'
            a = 7
            b = a + 3
            c = 2 * a
            print(c / b)
            ```

        === "Programme 2"
            ```python linenums='1'
            a = 5
            a = a + 1
            a = 2 * a
            print(a)
            ```
        
    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}

!!! tip "Incrémentation"
    Dans le **programme 2** précédent, l'instruction `a = a + 1` mérite toute notre attention...

    Observée avec des yeux de mathématicien, la précédente instruction est une horreur.

    ![](../images/memex.png){: .center width=480} 

    Vue avec des yeux d'informaticien, voilà comment est interprétée la commande :

    1. On évalue la **partie droite de l'égalité**, c'est-à-dire l'expression `a + 1`.
    2. On va donc chercher le contenu de la variable `a`. Si celle-ci n'existe pas, un message d'erreur est renvoyé.
    3. On additionne 1 au contenu de la variable `a`.
    4. On *écrase* le contenu actuel de la variable `a` avec la valeur obtenue au 3.

    À la fin de ces opérations, la variable `a` a bien augmenté de 1.

    Cette procédure, appelée **incrémentation**, est très très classique, il faut la maîtriser parfaitement car on va la retrouver très souvent!

!!! example "{{ exercice() }}"
    === "Énoncé" 
        Trouver à quoi correspondent les opérateurs `//` et `%` en exécutant plusieurs fois la cellule suivante en modifiant les valeurs des variables `a` et `b`:

        ```python linenums='1'
        a = 42
        b = 5
        print(a // b)
        print(a % b)
        ```
        
    === "Correction" 
        {{ correction(True, 
        "
        - l'opérateur `//` donne le **quotient** dans la division euclidienne;
        - l'opérateur `%` donne le **reste** dans la division euclidienne.
        "
        ) }}