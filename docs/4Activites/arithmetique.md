# Arithmétique
{{ initexo(0) }}


## 1- Diviseurs

!!! abstract "Notion de diviseur"
    En arithmétique, la notion centrale est la notion de divisibilité: un nombre $k$ est un diviseur d'un nombre $n$ si et seulement s'il existe un nombre $q$ tel que $n = k \times q$.

    Autrement dit, $k$ est un diviseur de $n$ si la division «tombe juste», c'est-à-dire si le reste dans la division euclidienne de $n$ par $k$ est égal à $0$.

!!! info "Opérateur `%` (modulo)"
    En Python, on obtient le reste de la division euclidienne avec l'opérateur `#!py %`.

    Par exemple: 

    ```python
    >>> 42 % 2
    0
    >>> 15 % 2
    1
    >>> 161 % 13
    5
    ```

En général, le reste en lui-même n'est pas intéressant, seul importe de savoir s'il est nul (et alors on est en situation de divisibilité). On peut donc seulement tester l'égalité entre le reste et 0, et Python donnera une réponse `#!py True` (si l'égalité est vraie) ou `#!py False`:

```python
>>> 8 % 2 == 0
True
>>> 47 % 5 == 0
False
```

!!! example "{{ exercice() }}: à la main"
    === "Énoncé" 
        En utilisant la console Python ci-dessous, déterminer:

        1. le reste dans la division de 2024 par 47.
        2. si 198 est divisible par 11
        3. si 7 est un diviseur de 356.


        {{ terminal() }}

    === "Correction" 
        {{ correction(True, 
        "
        On tape les instructions:
        ```python
        >>> 2024 % 47
        3
        >>> 198 % 11 == 0
        True
        >>> 356 % 7 == 0
        False
        ```
        
        "
        ) }}

!!! example "{{ exercice() }} : automatisation avec Python"
    === "Énoncé" 
        Pour obtenir tous les diviseurs d'un nombre $n$, on teste tous les nombres inférieurs ou égaux à $n$ pour savoir si ce sont des diviseurs.

        En Python, on va donc faire une boucle `#!py for` pour passer en revue tous les nombres $k$ inférieurs ou égaux à $n$ et tester la divisibilité de $n$ par $k$ comme fait précédemment.

        Copier-coller le code suivant dans le mini-IDE ci-dessous et le compléter. Vérifier en changeant la valeur de $n$ (avec les exemples faits dans la leçon par exemple).

        ```python linenums='1'
        n = 40
        for k in range(..., ...):
            if ... :
                print(...)
        ```

        {{ IDEv() }}
        
        
    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}



## 2- Nombres premiers

!!! abstract "Notion de nombre premier"
    Pour rappel, un nombre entier est dit **premier** s'il possède **exactement deux** diviseurs: 1 et lui-même.

    Pour déterminer si un nombre est premier, on cherche des diviseurs... et on s'arrête dès qu'on en a trouvé un (autre que 1 et lui-même bien entendu).
    
    On rappelle qu'on arrête la recherche à la **racine carrée** du nombre.


!!! example "{{ exercice() }} : à la main"
    === "Énoncé" 
        Déterminer si $391$ et $1249$ sont des nombres premiers.

        Vous pouvez utiliser la calculatrice ou la console Python ci-dessous pour faire la recherche des diviseurs.

        {{ terminal() }}

    === "Correction" 
        {{ correction(False, 
        "
        $391 = 17\times23$ donc 391 n'est pas premier.

        $1249$ est un nombre premier.
        "
        ) }}

!!! example "{{ exercice() }} : automatisation avec Python"
    === "Énoncé" 
        On veut désormais construire une **fonction** appelée `#!py est_premier` qui va prendre un nombre entier `#!py n` en paramètre et qui va renvoyer `#!py True` ou `#!py False` selon que le nombre `#!py n` est premier ou non.

        L'idée est de faire à peu près la même chose que dans le programme de recherche (et d'affichage) des diviseurs de la première partie, à la différence près qu'on ne souhaite pas *afficher* les diviseurs, mais renvoyer une valeur dès qu'un diviseur est trouvé.

    === "Indications/aides"
        - on commence la recherche à 2 et on s'arrête à $n-1$, attention donc à bien paramétrer le `#!py range` de la boucle `#!py  for` . On ne s'embête pas ici avec la racine carrée, tant pis si on fait faire trop de calculs à l'ordinateur, il est là pour ça, ne vous inquiétez pas il ne râlera pas.
        - remplacer dans le programme précédent l'instruction `#!py print(k)` par `#!py return False`.
        - **après la boucle**, si le programme en arrive là, c'est qu'aucun diviseur n'a été trouvé... que faut-il alors que la fonction renvoie?
    === "Correction" 
        {{ correction(False, 
        "
        def est_premier(n):
            for k in range(2, n):
                if n % k == 0:
                    return False
            return True
        "
        ) }}

    {{ IDEv() }}
    


