Trop long trop cher  
==================
Tel que pr�sent� sur HackerRank lors de la comp�tition informatique CEGInfo 2016 � l'�cole Polytechnique de Montr�al [(lien)](https://www.hackerrank.com/contests/competition-informatique-ceginfo-cegl-2016/challenges/trop-long-trop-cher-1).

Contexte
------------------
Polytron Lt�e, une compagnie de t�l�communication qu�b�coise, dispose d'un large r�seau de t�l�communication rejoignant les r�gions les plus �loign�es de la province. B�ti essentiellement � l'aide de c�bles en cuivre, Polytron d�sire d�sormais le remplacer par un r�seau � fibres optiques de mani�re � demeurer comp�titif face � son plus grand concurrent, Bets Inc.

Toutefois, apr�s avoir consult� maints ing�nieurs, il appara�t que le projet n'est pas aussi abordable que pr�vu. En effet, une partie significative du r�seau de Polytron provient de concurrents ayant �t� acquis au fil des ann�es. Ainsi, par certains endroits, le r�seau est fortement redondant; plusieurs chemins sont possibles entre deux m�mes endroits. Consid�rant le co�t �lev� reli� � l'installation d'un c�ble de fibre optique, Polytron vous demande d'�laborer un programme permettant d'indiquer la quantit� minimale de fibre optique � installer de mani�re � rejoindre un ensemble de lieux finis et ce, en limitant l'installation des nouveaux c�bles aux chemins emprunt�s pr�c�demment (ex: si auparavant A n'�tait pas directement connect� � B par le biais d'un c�ble en cuivre, il ne pourra pas plus l'�tre par un c�ble de fibre optique).

#####Input Format

La premi�re ligne contient le nombre n de lieux connect�s par le biais de c�ble en cuivre que l'on d�sire remplacer.

Pour chaque lieu, on compte ensuite une ligne comportant n valeurs. Deux types de valeurs sont possibles:

+ Un entier positif
+ -

Consid�rons la i�me valeur d'une ligne quelconque. Une valeur num�rique indique la distance entre ce lieu et le lieu repr�sent� par la (i + 1)�me ligne. Un tiret quant � lui indique qu'il n'y aucune connexion.

#####Output Format

Chaque paire de lieu qui devront �tre connect� avec de la fibre optique. Ces paires doivent �tre, � l'interne, ordonn�es en ordre croissant (l'indice repr�sentant le lieu du premier �l�ment de la paire doit �tre inf�rieur � celui du second �l�ment de la paire). Aussi, elles doivent �tre ordonn�e en ordre croissant entre elles (le premier �l�ment de la premi�re paire doit �tre sup�rieur au premier �l�ment de la seconde paire; si les deux premiers �l�ments sont �gaux, la m�me r�gle doit s'appliquer aux seconds �l�ments).

#####Exemple:

    1 4
    2 3
    2 6
    4 5
    4 6
    6 8
 
#####Sample Input

    3  
    - 3 1
    3 - 2
    1 2 -

#####Sample Output

    1 3
    2 3
#####Explanation

La situation d�crite par le fichier d'entr�e d�note un triangle. Ainsi, seuls deux liens de fibre optiques sont n�c�ssaires si l'on d�sire inclure l'ensemble des lieux dans le r�seau. Consid�rant les trois distances suivantes:

+ 1 (du lieu 1 � 3)
+ 2 (du lieu 2 � 3)
+ 3 (du lieu 1 � 2)

L'installation de fibre optique entre les lieux 1 et 3 et entre les lieux 2 et 3 est la solution qui minimise au maximum la quantit� de fibre n�cessaire.