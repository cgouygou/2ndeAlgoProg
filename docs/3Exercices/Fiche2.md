# Fiche d'exercices 2

{{ initexo(0) }}

!!! example "{{ exercice() }}"
    === "Énoncé" 
        Voici ci-dessous le code de la fonction `#!py lancer_de_truque` de l'exercice 1 de la fiche d'exercices sur les probabilités:

        ```python linenums='1'
        from random import randint

        def lancer_de_truque():
            face = randint(0, 8)
            if face <= 1:
                return 1
            elif face >= 6:
                return 6
            else:
                return face
        ```
        
        Modifier (en plus simple) ce programme pour que le de truqué:

        - donne un 6 avec une probabilité de $0,5$;
        - donne chacune des autres faces avec la même probabilité.

    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}


!!! example "{{ exercice() }}"
    === "Énoncé" 
        Reprendre l'exemple 2 du cours sur la boucle `#!py while`.

        Ajouter une variable `#!py c`  (comme compteur) qui donnera en fin de programme le nombre de tentatives pour donner la bonne réponse.

        **Questions à se poser:**

        - Quelle est sa valeur initiale, c'est-à-dire avant de commencer à poser la question?
        - De combien augmente-t-elle à chaque tentative?
    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}
!!! example "{{ exercice() }}"
    === "Énoncé" 
        Une feuille de papier à une épaisseur de $0,1$ mm. La tour Eiffel a une hauteur de 324 m.

        En imaginant qu'on puisse plier en deux la feuille de papier autant de fois que souhaité (ce qui n'est pas possible IRL), combien de pliages seraient nécessaires pour que l'épaisseur du papier dépasse la tour Eiffel?

        Compléter et exécuter le programme suivant pour répondre à la question.
        
        ```python linenums='1'
        epaisseur = 
        pliages = 

        while ... :
            epaisseur = 
            pliages = 
        
        print(...)
        ```
        
    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}