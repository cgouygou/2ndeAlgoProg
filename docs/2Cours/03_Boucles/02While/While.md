# La boucle non bornée (while)

La boucle `for` s'utilise lorsqu'on connaît à l'avance le nombre de répétitions à effectuer (un nombre entier). On parle de boucle **bornée**.

Mais il arrive fréquemment qu'on doive répéter des instructions un *certain* nombre de fois, qui n'est pas connu à l'avance. On a donc besoin d'une boucle **non bornée**,qui est en Scratch:

![](../../../images/RepeterForVide.png){: .center} 


En Python, c'est l'instruction `while`,  qui s'éxécutera tant qu'une condition est vraie et qui stoppera dès que cette condition ne le sera plus.


!!! abstract "La boucle `while`"

    **Syntaxe générale:**
    ```python linenums='1'
    while condition:
        *instructions à répéter*
    ```

!!! info "Remarques"

    - Une condition est le plus souvent le résultat (vrai ou faux) de la comparaison de deux valeurs avec les opérateurs: `>`, `>=`, `<`, `<=`, `==` (égal), `!=` (différent) ou `in` (appartient à).
    - `while` repète le bloc d'instructions à répéter **tant que** cette expression est vraie (égale à `True`) ;
    - il faut terminer la ligne commençant par `while` par `:` ;
    - le bloc d'instructions à répéter (le corps de la boucle) doit être indenté.

!!! example "Exemples"

    Tester chacun des exemples suivants dans Thonny.

    === "Exemple 1"
        ```python linenums='1'
        rep = "oui"
        while rep == "oui":
            rep = input("voulez-vous que je repose la question? ")
        ```
    
    === "Exemple 2"
        ```python linenums='1'
        from random import randint

        a = randint(1, 10)
        b = randint(1, 10)
        rep = 0
        while rep != a*b:
            rep = int(input(f"Combien font {a} fois {b} ?"))
        print('Bravo')
        ```
        