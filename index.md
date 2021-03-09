## Introduction

Avec l'avènement des smartphones, l'industrie vidéoludique est de plus en plus florissante, c'est donc logique qu'elle se rapproche d'une nouvelle technologie en développement telle que l'Intelligence Artificielle (IA). Il est cependant important de noter que l'IA y est présente depuis le début du jeux-vidéos, et même avant. En effet, avant Pong (le premier jeu-vidéo), un prémice d'IA avait été publié pour un [jeu de Nim](https://fr.wikipedia.org/wiki/Jeux_de_Nim) en 1952 [[1]](#1). 

Il y a eu ensuite des IA avec un comportement précis, comme dans le cas des fantômes de Pac-Man, où l'un suit Pac-Man, un autre le fuit, le suivant lui coupe la route et le dernier fait parfois des mouvements aléatoires [[2]](#2). 

Mais nous allons nous pencher plutôt sur les robots qui jouent à la place des humains, comme s'ils étaient des humains, c'est-à-dire avec les mêmes informations et les mêmes possibilités d'entrée. Le premier exemple de telles intelligences est celui des robots utilisés dans certains jeux en ligne, comme le MMORPG *World Of Warcraft* avec des *bots* exécutant des tâches répétitives de récoltes, afin d'amasser facilement des ressources.  

Pac-Man                    |  World Of Warcraft
:-------------------------:|:-------------------------:
<img src="https://raw.githubusercontent.com/julienbronner/Veille_Technologique_IA-JV/main/Images_Synthese/pacman.jpg" height="200" >  | <img src="https://raw.githubusercontent.com/julienbronner/Veille_Technologique_IA-JV/main/Images_Synthese/wow_bot.jpg" height="200" >

L'intérêt pour des IA plus complexes est plus récent, et permet souvent d'illustrer des avancées dans la recherche, c'est d'ailleurs le domaine dans lequel l'IA se contonne actuellement, puisqu'elle n'est pas encore utilisée dans des productions réelles. 

### Reinforcement Learning 

Une des méthodes d'apprentissage les plus utilisées dans ce domaine est le Reinforcement Learning. 

Cela consiste en un apprentissage automatique, durant lequel l'agent (c'est-à-dire le robot) agit sur l'environnement, celui-ci va retourner à l'interpréteur un nouvel état, qui va le fournir à l'agent accompagné d'une récompense. Toutefois cette récompense peut être positive ou négative. Ensuite, le robot agit à nouveau. Ainsi il s'améliore en fonction des retours à chaque étape, mais aussi à une échelle plus grande, lorsqu'il meurt ou gagne par exemple, cela lui donne une information sur sa suite d'actions globales. 

<p align="center">
<img src="https://raw.githubusercontent.com/julienbronner/Veille_Technologique_IA-JV/main/Images_Synthese/reinforcement_learning.png" height="200" style="background-color:white" >
</p>

## Développement de l'IA dans les jeux-vidéos

La multiplicité des jeux, et leur complexité très variable donne un éventail de choix très large pour utiliser une IA. Les premiers essais ont été faits avec des jeux simples, qui ont peut d'entrées possibles (notamment en terme de nombre de touches), comme Mario Bros ou des jeux sortis sur la console Atari 2600. Il n'y avait généralement que des touches pour les quatre directions et deux ou trois boutons d'actions. Il n'y a donc que peu de possibilités pour l'IA, ce qui permet de l'entraîner de manière plus importante et plus rapide. 

Il y a eu ensuite un intérêt pour des jeux plus complexes, tels que le jeu de stratégie en temps réel Starcraft II, le jeu "bac à sable" Minecraft ou même le MOBA (type de jeu en ligne où s'affrontent deux équipes de cinq joueurs généralement) Dota II. 

<!-- séparer les parties par ordre chronologique de jeu, d'algorithme, ou alors tri par type d'algorithme, ou par compléxité de jeu -->

### Jeux simples : Mario, Atari

Bat les scores humains
On trouve de nouveau trucs
Motivation à l'exploration uniquement
Mario : s’affranchir des règles, le robot apprend même les règles, on lui donne juste les boutons sur lesquels appuyer (algo genetique)

## Avancée récente “First return, then explore” : Go-Explore
ne prends pas juste le meilleur choix d’après son apprentissage (Reinforcement Learning classique)
“Montezuma's Revenge”
mais son but est de résoudre les problèmes qu’il rencontre


### StarCraft II : AlphaStar de DeepMind
Starcraft II : suite de alphaGO, AlphaStar

### MineRL
Minecraft : compétition avec 4 jours d’entrainements

## Annexe

Un détail sur les méthodes de Veille utilisée est disponible [ici](https://github.com/julienbronner/Veille_Technologique_IA-JV/blob/main/Rapport_Methodologique_Veille_IA_JV.pdf). 

## References
<a id="1">[1]</a> 
Wikipédia (visité le 08/03/2021).
[Artificial Intelligence in video games](https://en.wikipedia.org/wiki/Artificial_intelligence_in_video_games)

<a id="2">[2]</a> 
Wikipédia (visité le 08/03/2021).
[Pac-Man](https://fr.wikipedia.org/wiki/Pac-Man#Personnages)
