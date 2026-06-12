Exploration de données CatNat


Projet perso pour apprendre à manipuler des données réelles de pertes 
catastrophe naturelle via Python

Ce que j'ai fait dans ce premier notebook

J'ai pris des données réelles NOAA (ncei.noaa.gov) (événements météo USA 2023, 
~75k événements), filtré uniquement la grêle (~11.7k), puis isolé 
les événements avec des pertes assurées déclarées (850 au final).

Les montants de pertes étaient en texte ("100.00K", "1.00M"), 
j'ai écrit une fonction pour les convertir en vrais nombres.

En traçant la distribution dans un histogramme, on voit clairement que la plupart des 
événements ont des pertes faibles, mais quelques-uns sont énormes 
(plusieurs millions), ce qui donne une distribution asymétrique à droite. 
C'est exactement le genre de comportement qu'on attend des risques 
cat nat (peu d'événements concentrent l'essentiel des pertes).

Plus de la moitié des événements grêle n'ont aucun dégât déclaré. Soit parce qu'il n'y 
a vraiment rien eu, soit parce que ça n'a pas été reporté.

## Stack
Python, pandas, numpy, matplotlib

## Et après ?
Maintenant que je sais manipuler les données, j'ai envie d'aller plus 
loin et d'essayer de fitter une vraie loi statistique sur ces pertes 
(Pareto/Weibull) pour voir si ça colle avec ce que j'observe.