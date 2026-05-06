Expérience proposée n°1 :

=========================



Objectif : Comprendre l'évolution de l'estimation d'une matrice de covariance sur un échantillon de taille n, n constant puis n croissant.



Données : (fournit, fixe)

&#x20;- Une matrice C\* de référence. 

(matrice théorique

simulation N(mu,sigma) avec sigma= C\* la cible

covariances empirique se rapproche de la covariance de C\*, qd le cardinal (E) grandit

idée: Quel est l'influence des methodes sur l'estimateur que je produit?)

notion de cardinal (E): long?=> c'est pour cela qu'on a le beta



&#x20;- Une série de données avec $n\_0$ grand distribuée selon une loi normale et log-normale avec une covariance asymptotiquement égale à C\*







Expériences : 

1\. Mettre en place un code R qui permet d'obtenir la matrice de covariance empirique d'un échantillon de taille $n \\leq n\_0$ ;

2\. Comparer votre estimation avec une estimation faite par une méthode de référence en R (renseigner sur R => Cov() et faire le calcul moi meme);

3\. Soit un échantillon E, on estime la matrice $cov\_{emp}(E)$ avec la procédure 1. ou 2.. Mettre en place une comparaison quantitative entre $cov\_{emp}(E)$ et $C\*$. Décrire les propriétés de l'opéarateur de comparison proposé.

4\. Estimer la variabilité de $cov\_{emp}(E)$ lorsque le cardinal de E vérifie, $\\mid E\\mid = n$ avec $n$ constant ? ;

5\. Estimer la notion de convergence asymptotique de $cov\_{emp}(E)$ vers C\* sur l'échantillon considéré.



Questions théoriques à résoudre : 

**1. Comment calculer cov\_{emp}(E) ?**







**2. Comment comparer cov\_{emp}(E) et C\* ?**



la distance

les espaces métriques= les espaces normes (d(X,Y) = ||X-Y|| => norme associé a la disatnec (racine(dX,Y))

norme matricielle (recherche): laquelle choisir: decision (sont equivalentes mais seuil diff, vitesses et tailles diffèrent)

une fois quon a la norme: critere pour savoir si elles sont poches: boules: d(O,X)= ||x||^2 <= eps

(mes(A)=0 ne veut pas dire que A est nulle)



vitesse de convergence plus grande si l'ech est pass totalement aléatoire pour faire baisser la variance grace a la cov.

estimateur non nul est non biais de moindre variance (VUMSB)



blue noise (estimateur "truqué" pour methode monte carlo: points pas forcment aletaoire)

obj: la vitesse de convergence de l'estimateur, pas l'alétoirité des points







**3. Comment mesurer la distribution de $cov\_{emp}(E)$ à de taille card(E) fixé ?**



(qd on fixe card: c'est plus insymptotique)(ds la réalité, card(E) borné (<= n )

variablité par le choix de l'échantillon. 



Bootstrap(se renseigner): on prend des chantillon alétaioire de taille n AVEC REMISE parmis n0, on claculoe cov\_emp(E): on fait une boucle 

on clacule la moyennne et la variance/ou ecart type (sigma^2\_covemp(E)) de cov\_emp(E)

parfois on a pas n0, on a ech bcp plus petit (n+1) (si c n, on peut rien faire)



Jackknife (ou leave one out): on en enleve un et on a un ech de n: ca nous donne n+1 ech de taille n. Diff entre bookstrap et Jackknife est la remise.

le fait que n+1 depend de n: corrélation

bookstrap: c'est décorélé (depend plus de n): plus fort mais plus couteux



=> c'est comme ca qu'on def moyenne et variance (les mesures qui m'interesse) mais on fait pas les 2 dans le code



moyenne de cov: 1/n = somme Ai (ai les matrices) pour n fixe





**4. Comment caractériser la convergence asymptotique ?**









Approfondissement :

Comment générer les données ? 

apres: generation des donnes





il existe des packages mais faire aussi a la main pour comprendre comment ca marche



