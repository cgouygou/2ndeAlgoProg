# 02 L'instruction conditionnelle


![](../../images/SiAlorsSinon.png){: .center} 

Un langage de programmation permet d'effectuer des tests sur les valeurs contenues dans les variables et d'exécuter (ou pas) certaines instructions selon le résultat de ces tests. On parle d'*instruction conditionnelle* qui s'écrit en Python avec le mot-clé `if`.

!!! abstract "Modèle"
    ```python linenums='1'
    if condition :
        instructions à exécuter si condition est vraie
    else:
        instructions à exécuter si condition est fausse
    ```

    **Remarques:**

    - Une condition est le plus souvent le résultat de la comparaison de deux valeurs avec les opérateurs: `>`, `>=`, `<`, `<=`, `==` (égal), `!=` (différent) ou `in` (appartient à).
    - On remarquera à nouveau les `:` en fin de ligne et l'indentation des instructions.
    - la partie du `else` n'est pas obligatoire.

!!! example "Exemples"
    Tester chacun des exemples suivants dans l'IDE ci-dessous (exécuter plusieurs fois en changeant la valeur des variables).

    {{ IDEv() }}
    
    === "Exemple 1"
        ```python linenums='1'
        heure = 13
        if heure >= 12:
            print("j'ai faim")
        else:
            print("j'ai sommeil")
        ```

    === "Exemple 2"
        Sans `else`.

        ```python linenums='1'
        mot = "abracadabra"
        if "a" in mot:
            print(mot, " contient au moins un a.")
        ```
    
    === "Exemple 3"
        On peut *imbriquer* les instructions conditionnelles.

        ```python linenums='1'
        age = 15
        if age <= 6:
            print("gratuit")
        else:
            if age > 18:
                print("plein tarif")
            else:
                print("tarif réduit")
        ```
    
    === "Exemple 4"
        :warning: Il ne faut pas confondre `=` (affectation d'une valeur à une variable) et `==` (test d'égalité entre deux valeurs).
        ```python linenums='1'
        print("Combien fait 7 fois 8?")
        rep = 42
        if rep == 56:
            print("bonne réponse")
        else:
            print("révise les tables")
        ```
        