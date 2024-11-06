# La boucle bornée (for)


L'un des grands principes de la programmation est le fait de pouvoir **répéter** un certain nombre de fois des instructions (on parle alors de *boucle* d'instructions), ce qui se faisait en Scratch avec:

![](../../../images/RepeterForVide.png){: .center} 

En Python, l'équivalent est la boucle `for` que l'on a rencontrée dans l'activité **Pyrates**. Elle utilise la fonction `range` qui génère un ensemble d'entiers consécutifs commençant par 0.



!!! abstract "Modèle"
    **Pour répéter 10 fois des instructions:**

    ```python linenums='1'
    for k in range(10):
        instructions
    ```
    
    **L'équivalent en Scratch:**

    ![](../../../images/RepeterFor.png){: .center width=240} 

!!! info "Remarques"
    - Dans cette instruction, `k` est une variable «compteur» : elle est automatiquement augmentée de 1 à chaque passage dans la boucle (on dit *incrémenter* en programmation).
    - Ainsi, l'instruction `for k in range(10)` peut se traduire par « pour `k` allant de 0 à 9», ce qui fait bien 10 répétitions.
    - On peut évidemment nommer comme on le souhaite cette variable: `i`, `compteur`, `x`, `toto`, `jean_claude`...
    - Les instructions à répéter doivent être indentées (décalées par rapport à la marge).
    - On peut utiliser la variable «compteur» dans les instructions de la boucle. Ou pas.

!!! example "Exemples"
    Tester chacun des exemples suivants dans l'IDE ci-dessous.

    {{ IDEv() }}
    
    === "Exemple 1"
        ```python linenums='1' title='Sans utilisation de la variable'
        for k in range(10):
            print("We're up all night to get lucky")
        ```
        
    === "Exemple 2"
        ```python linenums='1' title='Avec utilisation de la variable'
        for i in range(5):
            j = 2 * i
            print(j, " est le double de ", i)
        print("cette instruction n'est pas répétée puisqu'elle n'est pas indentée")
        ```
    
    === "Exemple 3"
        ```python linenums='1' title='En décalant le départ à 1 au lieu de 0'
        for n in range(1, 6):
            print(n)
        ```