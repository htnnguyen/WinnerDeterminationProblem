###Presentation:
This is an agent-based (thread-based) implementation of a solution to the winner determination problem (WDP) in combinatorial auctions. It is based on the methode proposed in [2]. 
It was tested with [StacklessPython](http://www.stackless.com/) wich gave better results then the conventional CPython.

###Definition:
As explained in [1] :
*"The combinatorial auction is a type of auctions in which agents (bidders) can place bids on combinations of items (goods), called packages, rather than just individual items.
The combinatorial auctions have been used in solving resource and task allocation problems in multi-agents system [7, 23]. They play an important role in various domains such as economics, game theory and the sale of spectrum licenses in America’s Federal Communications Commissions (FCC) auctions."*

###Algorithme:
The algorithme proposed in [2] is as follows : 

![Image Alt](https://duckduckgo.com/assets/badges/logo_square.64.png)

We made few changes:
- We implemented different agets working in parallel.
- Each agent starts with a random solution, writes it in a *Blackboard* if it's better then the solution already there (or if there is no solution written) otherwise, he takes that better solution found in the *Board*.
- Then, he goes to a random neighbor (if this later is not *Tabou*).

###Execution:
The code is executed as follows:
```bash
python sls.py benchmarkfile
```
One can find some examples of benchmark files in the **benchmarks** folder.

###Ref: 
- [1] X.-S. Yang (Ed.): Artif. Intell., Evol. Comput. and Metaheuristics, SCI 427, pp. 775–791.
c Springer-Verlag Berlin Heidelberg 2013
springerlink.com

- [2] Dalila Boughaci, Belaid Benhamou et Habiba Drias : Une recherche locale stochastique pour le problème de la détermination du gagnant dans les enchères combinatoires. Gilles Trombettoni. JFPC 2008- Quatrièmes Journées Francophones de Programmation par Contraintes, Jun 2008, Nantes, France. pp.59-68. https://hal.inria.fr/inria-00290789/document
- 
###License:
This is published under GNU GPL Lisence.
For more informations about the terms: https://www.gnu.org/licenses/gpl.html

![Image Alt](https://www.gnu.org/graphics/gplv3-127x51.png)

