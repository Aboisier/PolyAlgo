Le passeur  
==================
Tel que pr�sent� sur HackerRank lors de la comp�tition informatique CEGInfo 2016 � l'�cole Polytechnique de Montr�al [(lien)](https://www.hackerrank.com/contests/competition-informatique-ceginfo-cegl-2016/challenges/le-passeur).
Contexte
------------------

Un vieux passeur vivant pr�s d'une rivi�re �loign�e s'est converti en consultant en logistique de passage de rivi�re lorsque des passeurs plus jeunes sont arriv�s dans son village grandissant. Bien qu'il aime son nouvel emploi, il est souvent approch� par des gens qui lui proposent des �nigmes qu'il trouve moqueuses. Ce sont de simples probl�mes de passage de rivi�re qu'il souhaite r�gler une fois pour toute.

Passage de rivi�re
------------------
Les [probl�mes de passages de rivi�re](https://fr.wikipedia.org/wiki/Probl%C3%A8mes_de_passage_de_rivi%C3%A8re) ([en](https://en.wikipedia.org/wiki/River_crossing_puzzle)) consistent � devoir faire passer un nombre d'individus d'une rive � l'autre de la rivi�re avec un nombre limit� de places sur un bateau. � cela s'ajoutent des contraintes formul�es de la fa�on suivante: une paire d'individus donn�e ne peut pas �tre mise ensemble sans qu'un troisi�me individu donn� ne soit pr�sent.

Le bateau est sur la rive de d�part pour commencer et fait ensuite des trajets en alternant de sens jusqu'� la fin, lorsqu'il finit sur la rive d'arriv�e (oppos�e � celle de d�part) avec tous les individus. Il n'est pas n�cessairement plein pour chaque trajet. Cependant, il doit toujours y avoir quelqu'un � bord du bateau.

Probl�me
------------------
Vous devez aider le consultant en faisant un programme qui va r�soudre n'importe quel probl�me de passage de rivi�re de la forme d�crite ci-haut.

Exemples
------------------
Un probl�me de travers�e souvent pos� � l'ancien passeur est celui du loup, de la ch�vre et du chou. Dans ce probl�me, un fermier doit traverser � bord d'un bateau � deux place un rivi�re en emmenant son loup, sa ch�vre et un chou. Le fermier et chacune de ses choses prennent une place chacuns � bord du bateau. Si le loup et la ch�vre sont pr�sents sans le fermier (que ce soit sur une rive ou � bord), alors le loup mangera la ch�vre et il en est de m�me pour la ch�vre et le chou.

Un autre probl�me d�j� rencontr� est celui des dompteurs et de leurs singes. Trois dompteurs sont chacun accompag�s d'un singe de leur cirque. Les six individus doivent traverser la rivi�re � bord d'un radeau � deux places. Si un singe n'est pas surveill� par son dompteur, alors il sera tent� d'attaquer n'importe quel autre dompteur pr�sent.

�videmment, dans ces deux probl�mes, tous les individus doivent traverser la rivi�re sains et saufs. (Note: Par simplicit�, tous les individus peuvent conduire le bateau dans notre sc�nario g�n�ral. Cela fait que le chou pourrait faire un mouvement � bord du bateau � lui seul.)

#####Input Format

Le nombre d'individus voulant traverser N et le nombre de places maximal B dans le bateau sur la premi�re ligne, s�par�s par un espace.

Sur les autres lignes, les contraintes. Chaque contrainte est une liste de trois identifiants s�par�s par des espaces. Les individus correspondant au deux premiers identifiants ne peuvent pas �tre ensembles � moins que le troisi�me ne soit pr�sent aussi. Pour simplifier, les identifiants des individus sont des entiers entre 1 et le nombre d'invividus N.

#####Output Format

Le minimum du nombre de travers�es n�cessaires � faire passer tous les individus de l'autre c�t�.

Si aucune solution n'est possible, mettre ':(' en sortie.

#####Sample Input

    2 
    1 5 4 
    1 6 4 
    2 4 5 
    2 6 5 
    3 4 6 
    3 5 6

#####Sample Output

    11

#####Explanation

Ce probl�me correspond � celui des singes et des dompteurs, avec les singes �tant les individus 1, 2 et 3 et les dompteurs 4, 5 et 6. Le singe x appartient au dompteur x+3.

Il est possible de faire les travers�es suivantes:

(Aller: A, Retour: R) + identifiants des individus � bord

    A: 1 2 
    R: 2
    
    A: 2 3 
    R: 3
    
    A: 4 5 
    R: 2 5
    
    A: 5 6 
    R: 1
    
    A: 1 2 
    R: 2
    
    A: 2 3

Cela fait un total de 11 mouvements de bateau, ce qui est le minimum pour ce probl�me.