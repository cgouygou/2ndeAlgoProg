# Fonctions

{{ initexo(0) }}

## 1 - Définir une fonction


Comme on l'a vu dans les activités précédentes, on peut définir des fonctions Python qui permettent de regrouper plusieurs instructions et qui, à partir d'un paramètre, renvoie une valeur déterminée par ces instructions.

Par exemple, dans l'activité [Arithmétique](https://cgouygou.github.io/2ndeAlgoProg/4Activites/arithmetique/){:target="_blank"} on a écrit la fonction suivante:

```python linenums='1'
def somme_diviseurs(n):
    s = 0
    for k in range(1, n+1):
        if n % k == 0:
            s = s + k
    return s
```

Cette fonction teste pour tous les nombres compris entre 1 et n si le nombre `n` est divisible par `k` et, si oui, l'ajoute à une variable `s`. Cette variable contient donc à la fin de la boucle `#!py for`  la somme des diviseurs de `n` et la fonction renvoie cette valeur avec le mot-clé `#!py return`.

En mathématiques, une fonction $f$ fait exactement la même chose: elle prend une valeur en paramètre (souvent noté $x$) et renvoie une valeur $f(x)$ après calculs. En plus simple, c'est-à-dire sans boucle ni test.

On peut donc utliser une fonction Python pour représenter une fonction mathématique, comme par exemple celle du cours, $f(x)=x^2-4x+1$:

```python linenums='1'
def f(x):
    return x**2 - 4*x + 1
```

!!! example "{{ exercice() }}"
    === "Énoncé" 
        1. Dans un nouveau fichier, avec Thonny, écrire les fonctions suivantes en langage Python:

            - $f(x) = 3x^2-1$
            - $g(x) = -2x+7$
            - $h(x) = \dfrac{2x+1}{x-4}$

        2. Calculer à la main l'image de 2 par chacune de ces trois fonctions.
        3. Exécuter le programme puis vérifier les calculs en console. Par exemple:

            ```python
            >>> f(2)
            ```
            
    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}


## 2 - Faire un tableau de valeurs

Pour obtenir un tableau de valeurs, il suffit d'appeler plusieurs fois la fonction pour des valeurs de $x$ qui augmentent d'un *pas* défini à l'avance.

!!! example "{{ exercice() }}"
    === "Énoncé" 
        Ajouter  la fin du programme suivant le code suivant et le compléter (remplacer les points de suspension) pour qu'il affiche les valeurs de $f(x)$ pour x allant de $-5$ à $10$ avec un pas de $1$.

        ```python linenums='1'
        pas = ...
        x = ...
        while x < 10:
            print(x, ...)
            x = x + ...
        ```
        
    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}

!!! example "{{ exercice() }}"
    === "Énoncé" 
        1. Modifier le programme précédent pour qu'il affiche les valeurs des fonctions $f$ et $g$ en même temps.

        2. Que remarque-t-on? Comment l'interpréter en ce qui concerne les courbes des fonctions $f$ et $g$?

        3. Modifier à nouveau le programme pour qu'il n'affiche **que** la valeur remarquée.


    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}

!!! example "{{ exercice() }}"
    === "Énoncé" 
        1. Afficher les courbes des fonctions $f$ et $g$ sur votre calculatrice. Que remarque-t-on?
        2. Comment modifier le programme précédent pour le deuxième point?
    === "Correction" 
        {{ correction(False, 
        "
        "
        ) }}