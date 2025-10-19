## Rappel

Pour un ensemble donné de n éléments distincts, le 
nombre de sous-ensembles possibles de p éléments
est donné par le coefficient binomial p parmi n $\binom{n}{p}$.

Par exemple... 
 * Dans l'ensemble E = { a,b,c,d }
 * Il existe 6 paires: ab, ac, ad, bc, bd, cd ( on considere que ba = ab )
 * Donc $\binom{4}{2}=6$

## Formule binomiale

On note n factoriel $n!$ la quatite $n*(n-1)*...*1$

Le coefficient binomial p parmi n  est $\binom{n}{k} = \frac{n!}{p!(n-p)!}$

### Verification

Dans cette section on va verifier la formule du coefficient
binomial sur un exemple precis, en repondant à la question:
Combien de mains de 4 cartes existe-t-il dans un jeu de 32.

Allons-y pas a pas... Reponds aux questions par une expression
numérique, mais sans faire le calcul.

1) Combien de sequences de tirages de 4 cartes sont possibles ?
<details>
<summary>Soluce</summary>
    
* Pour choisir la 1ere carte on a 32 possibilites
* Pour choisir la 2eme carte on a 31 possibilites
* Pour choisir la 3eme carte on a 30 possibilites
* Pour choisir la 4eme carte on a 29 possibilites
* Le nombre de sequences de tirage est donc :
```math
32*31*30*29  = \frac{32!}{(32-4)!}
```
</details>

2) Combien de permutations de chaque main existe-t-il ?
<details>
<summary>Soluce</summary>
    
* Pour choisir la 1ere carte on a 4 possibilites
* Pour choisir la 2eme carte on a 3 possibilites
* Pour choisir la 3eme carte on a 2 possibilites
* Pour choisir la 4eme carte on a 1 possibilite
* Le nombre de permutaions est donc :
  ```math
  4*3*2*1 = 4!
  ```
</details>

4) En deduire combien de mains sont possibles ?
<details>
<summary>Soluce</summary>

```math
\binom{32}{4} = \frac{32!}{(32-4)!*4!}
```
</details>

Remarque:  Le calcul naïf de cette formule en commencant par 32!
est impossible sur une machine courante car 32! est un nombre énorme:
`263130836933693530167218012160000000`

## Formule du triangle de Pascal

$\binom{n}{p} = \binom{n-1}{p-1} + \binom{n-1}{p}$

Cette formule permet de calculer de proche 
en proche tous les coefficients binomiaux!
Il suffit de construire un tableau des coefficients. $\binom{n}{p}$
étant sur la ligne n et la colonne p. Chaque coeffiencient est
la somme des 2 cases Nord et Nord-Ouest.

n \ p| 1 | 2 | 3 | 4 | 5 |
--|---|---|---|---|---|
1 | 1 | - | - | - | - |
2 | 1 | 1 | - | - | - |
3 | 1 | 2 | 1 | - | - |
4 | 1 | 3 | 3 | 1 | - |
5 | 1 | 4 | 6 | 4 | 1 |

### Démonstration par le calcul

Vérifie cette formule par le calcul. Il est conseillé
de faire la difference des parties et simplifier jusqu'à
obtenir 0. C'est plus simple que d'essayer de faire apparaître
les bons termes.

### Démonstration par le raisonement

Imaginons que l'on cherche à former une équipe de 10 joueurs 
alors qu'il y a 15 volontaires.

1) Combien y-a-t'il d'équipes possibles?
<details><summary>Soluce</summary>
<ul>
<li> Il faut tirer 10 joueurs (p=10) 
     parmi tous les joueurs (n=15) </li>
<li> Réponse: $\binom{15}{10}$ </li>
 </ul>
</details>

Il se trouve que parmi les cadidats, il y a un certain Legolas. 

2) Combien y-a-t'il d'équipes possibles avec Legolas ?
<details><summary>Soluce</summary>
<ul>
<li> Il faut tirer 9 joueurs (p=9) en plus de Legolas, 
     parmi tous les joueurs restant disponibles (n=14) </li>
<li>Réponse: $\binom{14}{9}$</li>
</ul>
</details>

3) Combien y-a-t'il d'équipes possible sans Legolas ?
<details><summary>Soluce</summary>
<ul>
<li> Il faut tirer 10 joueurs (p=10), 
     parmi tous les joueurs en excluant Legolas (n=14) </li>
<li>Réponse: $\binom{14}{10}$</li>
</ul>
</details>

L'ensemble de toutes les équipes peut être vu comme la somme de toutes
les équipes avec Legolas plus toutes les équipes sans Legolas.

En deduire la formule de Pascal, dans ce cad d'étude.
<details><summary>Soluce</summary>
<ul>
<li>Réponse: $\binom{15}{10} = \binom{14}{9} + \binom{14}{10}$</li>
</ul>
</details>

## Utilisation du triangle

1) Ecris un program python qui calcule le coefficient binomial
de proche en proche. Profites-en pour donner la valeur $\binom{32}{4}$.

2) Modifie le program pour effectuer les calculs jusqu'à n=80,p=80.
Et pour chaque position affiche soit un "*" si le coefficient
est pair, soit un espace " " si le coefficient est impair.



   


