## Introduction

Avec l'avènement des smartphones, l'industrie vidéoludique est de plus en plus florissante, c'est donc logique qu'elle se rapproche d'une nouvelle technologie en développement telle que l'Intelligence Artificielle (IA). Il est cependant important de noter que l'IA y est présente depuis le début du jeux-vidéos, et même avant. En effet, avant Pong (le premier jeu-vidéo), un prémice d'IA avait été publié pour un [jeu de Nim](https://fr.wikipedia.org/wiki/Jeux_de_Nim) en 1952 [[1]](#1). 

Il y a eu ensuite des IA avec un comportement précis, comme dans le cas des fantômes de Pac-Man, où l'un suit Pac-Man, un autre le fuit, le suivant lui coupe la route et le dernier fait parfois des mouvements aléatoires [[2]](#2). 

Mais nous allons nous pencher plutôt sur les robots qui jouent à la place des humains, comme s'ils étaient des humains, c'est-à-dire avec les mêmes informations et les mêmes possibilités d'entrée. Le premier exemple de telles intelligences est celui des robots utilisés dans certains jeux en ligne, comme le MMORPG _World Of Warcraft_ avec des _bots_ exécutant des tâches répétitives de récoltes, afin d'amasser facilement des ressources.  

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

C'est pour cela que l'on parle d'apprentissage par renforcement, le robot apprend à chaque itération, et ses actions sont guidées par la récompense, il se **renforce** donc à chaque étape.

## Développement de l'IA dans les jeux-vidéos

La multiplicité des jeux, et leur complexité très variable donne un éventail de choix très large pour utiliser une IA. Les premiers essais ont été faits avec des jeux simples, qui ont peut d'entrées possibles (notamment en terme de nombre de touches), comme Mario Bros ou des jeux sortis sur la console Atari 2600. Il n'y avait généralement que des touches pour les quatre directions et deux ou trois boutons d'actions. Il n'y a donc que peu de possibilités pour l'IA, ce qui permet de l'entraîner de manière plus importante et plus rapide. 

Il y a eu ensuite un intérêt pour des jeux plus complexes, tels que le jeu de stratégie en temps réel Starcraft II, le jeu "bac à sable" Minecraft ou même le MOBA (type de jeu en ligne où s'affrontent deux équipes de cinq joueurs généralement) Dota II. 

<!-- séparer les parties par ordre chronologique de jeu, d'algorithme, ou alors tri par type d'algorithme, ou par compléxité de jeu -->

## Jeux simples : Mario, Atari

Un des jeux les plus utilisés est Mario Bros, puisqu'il est très populaire, cela parle au plus grand nombre lors des démonstrations. Maintenant, la plupart des meilleurs scores sont détenus par des robots, qui peuvent exécuter beaucoup plus d'actions, et bien plus précises, que des humains. De plus, les jeux Atari donnent des styles de jeux très différents, ce qui permet de tester les IA sur des champs d'actions différents. 

Il y a donc beaucoup de modèles et de méthodes différentes pour faire des IA pour les jeux Atari, mais les plus efficaces actuellement sont [DQN](https://www.nature.com/articles/nature14236), [R2D2](https://openreview.net/forum?id=r1lyTjAqYX) (les chercheurs aiment ce genre de référence) et [Agent57](https://arxiv.org/abs/2003.13350) [[3]](#3). Ceux-ci essayent d'apprendre de tout l'environnement, et agissent en fonction de l'état actuel. Il y a des variantes également, comme [MuZero](https://deepmind.com/blog/article/muzero-mastering-go-chess-shogi-and-atari-without-rules), qui ne prend en compte que certaines parties de l'environnement, celles jugées les plus importantes, pour prendre ses décisions. 

### Curiosity-Driven Learning

Il existe également des méthodes dont la récompense n'est plus extrinsèque à l'agent, c'est-à-dire qu'elle ne vient plus de l'environnement, mais elle peut être intrinsèque. Il y a notamment le cas de la curiosité [[4]](#4), qui est modélisée via l'erreur de prédiction comme récompense. Il est possible aussi de "décourager" l'agent à revisiter un état déjà vu, ce qui le fait explorer des états inconnus. L'étude présentée en note a utilisé comme base les jeux Atari, et d'autres jeux, et a été menée par une équipe composée d"unniversitaires de différentes origines, dont Open AI. Il y a toutefois des limites dans le cas de jeux basé sur de l'aléatoire. 

### “First return, then explore” : Go-Explore

Une autre approche trouvée pour améliorer le Reinforcement Learning est celle développée par cette équipe de Uber AI Labs [[5]](#5). L'idée ici est que l'agent résolve les problèmes rencontrés. Pour cela, il apprend et retient les manières qu'il a eu d'aborder un problème et le résultat associé, pour essayer de nouvelles approches. Lors des tests sur une sélection de jeu, ceci a permis d'obtenir de meilleurs résultats que d'autres algorithmes actuels dans 85% des cas. Il a même battu le meilleur score jamais réalisé dans le jeu _Montezuma's Revenge_.

 <iframe width="560" height="315" src="https://www.youtube.com/embed/DFhN7N0Troc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" align="center" allowfullscreen></iframe>


## StarCraft II : AlphaStar de DeepMind

Suite au succès de AlphaGo et de AlphaZero pour les jeux d'échecs, de shogi et de Go, le centre de recherche de Google DeepMind s'est intéressé au jeu-vidéo, et plus particulièrement à StarCraft II, un jeu de stratégie en temps réel. Il y a donc un niveau de complexité bien supérieur aux jeux présentés précédemment, puisque l'on contrôle plusieurs unités ("personnages") à la fois, et qu'il y a une stratégie à l'échelle globale à avoir. L'agent a ainsi su trouver de nouvelles manières de pousser l'adversaire à l'erreur, qui est la première étape de la victoire [[6]](#6). Cela a donc remis en cause la diversité des possibilités explorées par les joueurs professionnels [[7]](#7), puisqu'en s'entrainant contre des clones d'elle-même, AlphaStar dépasse les compétences et les idées utilisées par ces derniers. 

## MineRL
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

<a id="3">[3]</a> 
DeepMing Blog (visité le 12/03/2021).
[MuZero: Mastering Go, chess, shogi and Atari without rules](https://deepmind.com/blog/article/muzero-mastering-go-chess-shogi-and-atari-without-rules)

<a id="4">[4]</a> 
Site personnel (visité le 12/03/2021).
[Large-Scale Study of Curiosity-Driven Learning](https://pathak22.github.io/large-scale-curiosity/)

<a id="5">[5]</a> 
Techxplore.com (visité le 12/03/2021).
[Reinforcement learning algorithms score higher than humans, other AI systems at classic video games](https://techxplore.com/news/2021-02-algorithms-score-higher-humans-ai.html )

<a id="6">[6]</a> 
DeepMind Blog (visité le 12/03/2021).
[AlphaStar: Mastering the Real-Time Strategy Game StarCraft II](https://deepmind.com/blog/article/alphastar-mastering-real-time-strategy-game-starcraft-ii)

<a id="7">[7]</a> 
DeepMind Blog (visité le 12/03/2021).
[AlphaStar: Grandmaster level in StarCraft II using multi-agent reinforcement learning](https://deepmind.com/blog/article/AlphaStar-Grandmaster-level-in-StarCraft-II-using-multi-agent-reinforcement-learning)


