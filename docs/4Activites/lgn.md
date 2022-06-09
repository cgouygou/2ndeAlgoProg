# Loi des grands nombres

1. Que fait le programme suivant (sans se soucier des instructions commençant par `plt.`) ?
    ```python linenums='1'
    from random import randint
    from math import sqrt
    import matplotlib.pyplot as plt

    n = 50
    compteur = 0
    p = 1/6

    plt.figure()
    for k in range(1, n + 1):
        de = randint(1, 6)
        if de == 6:
            compteur = compteur + 1
        f = ...
        plt.plot(k,f, "or", markersize=1)

    plt.show()
    ```
    
2. Compléter la ligne 14 pour que la variable `f` contienne la valeur de la fréquence (proportion) de 6 au bout du k-ième lancer.

3. Ajouter dans la boucle une instruction pour placer le point de coordonnées $(k ; p)$ en vert.

4. Ajouter dans la boucle deux instructions pour placer les points de coordonnées $(k ; p-\frac{1}{\sqrt{k}})$  et $(k ; p+\frac{1}{\sqrt{k}})$ en bleu.

5. Exécuter le programme pour plusieurs valeurs de `n`.