# Chunk Stories: Extension du projet en 2019: Collaboration et Stagiaires

But de ce document: mettre en place les lignes directives pour faire de Chunk Stories un projet capable de prendre en charge un certain nombre de contributeurs. Également, pitcher l'idée au responsable IT de CSLabs.

## Qu'est-ce que Chunk Stories ?

Chunk Stories est un clone de Minecraft sous license LGPL, plus précisément c'est un moteur de jeu spécialisé dans les jeux "voxels" ( avec des mondes faits de cubes individuellement modifiables ). Chunk Stories est un vrai moteur de jeu, il est extrêmement flexible: il est possible de charger au runtime des différents contenus ("mods") et le moteur gérera tout, y compris leur intéraction.

Le moteur de Chunk Stories est écrit de zéro en en Java/Kotlin (portage en cours), et utilise les standards dans le domaine (Vulkan, OpenGL, OpenAL, VMA, LWJGL etc). Le moteur implémente et permet l'implémentations de techniques modernes, voire *state of the art* en matière de rendu 3D, et est optimisé constament pour tirer le meilleur parti possible du hardware visé.

Chunk Stoiries se décline en trois sous-projets: une API ouverte, une implémentation de cette API en client/serveur et du contenu de base minimal qui sert de démo et de socle pour construire de nombreux éléments de gameplay. Le projet est développé depuis 2015 !

## Ambitions du projet 

En 2019 l'objectif sera de passer d'un modèle de dévelopmement avec un lead dev qui fait tout et qui reçoit quelques pull-requests et assets à l'occasion, à un vrai projet Open source, avec une vraie organisation, une équipe et une meilleure direction. Le but final est double: il s'agit autant de créer un produit finit que d'assembler une équipe et un réseau de personnes enthousiastes et compétentes.

En particulier il est important de mettre en place une politique de recrutement et d'accompagnement des recrues. Il est essentiel de s'assurer que ces nouveaux arrivants et le projet recevoient chacun un bénéfice, il ne sera pas ici question d'obtenir du travail gratuit au seul bénéfice des chefs de projet.

### TL;DR

 * Gagner de l'expérience dans le monde du jeu vidéo
 * Gagner de l'expérience dans le domaine du travail en équipe
 * Obtenir un produit finit jouable et joué
 * Bien se marrer (c'est rigolo de dev des jeux)

## Rôle potentiel du CSlabs

Une collaboration à deux sens est envisageable: Chunk Stories est un projet sérieux, viable et déjà bien en route, qui pourrait tout à fait servir de faire-valoir pour le département IT, qui y gagnerait également une publicité non-négligeable sur les plateformes Internet où Chunk Stories entretient une présence. De plus, il existe de nombreuses personnes motivées dans CSLabs qui ne demandent qu'a travailler sur un jeu.

De l'autre coté, le projet Chunk Stories manque cruellement de dévelopeurs et de contributeurs de façon générale, de nombreux aspects comme le site, le gameplay et plein de sous-systèmes requièrent une attention supérieure à celle qu'un seul étudiant peut apporter sur son temps libre. Le fait de bénéficier, sur site (!), de contributeurs motivés est un luxe que peu de projet opensource auront la chance d'avoir.

## Principe des "Stagiaires"

Des personnes motivées à contribuer, qui sont soit amateurs et peuvent aider directement grâce à certaines de leurs compétences ( ex: Graphiste, compositeur, web dev etc ). En particulier dans ce contexte il s'agirait d'adhérents/membres de CSLabs (voir section précédente), de simples étudiants de l'Unamur, voire de n'importe qui dans le monde. 

Évidement la proximité sociale, physique et linguistique seront toujours un plus mais si la motivation et les conditions y sont, tout est possible :)

### Prérequis

 * Pour les missions de programmation, une familiarité préalable avec la technologie utilisée est préférée, le projet sera ravit de former des gens à maitriser une technologie, mais apprendre à programmer de zéro ne rentre pas vraiment dans ce qui est raisonnable pour l'équie de Chunk Stories
 * Un minimum d'anglais histoire de pouvoir lire et écrire la documentation officielle du projet
 * Un ordinateur relativement récent; pour des raisons technologiques le choix est fait de se concentrer sur des APIs graphiques récentes, si bien qu'une machine bas de gamme où très ancienne (+5 ans) aura peu de chances de faire tourner le jeu dans son backend Vulkan (un backend OpenGL classique est prévu mais pas encore commencé, voir "missions")
     * De manière générale il est inefficace et problématique de travailler avec du matériel dépassé dans le contexte du jeu vidéo: temps de compilation, lourdeur des IDEs etc.
     * Hugo adore collectionner les ordinateurs, vous pouvez toujours lui demander une machine de prêt :p


 * Avoir utilisé Git avant est un énorme plus

## Besoins du projet

De manière large, des compétences qui seraient utiles à la réalisation du projet de manière non-spécifique

Pour des demandes spécifiques, voir les missions disponibles

 * Programmeurs Java/Kotlin
 * Programmeurs/designers gameplay (pour le core)
 * Expertise web
 * Programmeurs réseau (netcode du jeu)
 * Artistes 2D, 3D
 * Des gens qualifiés en son
 * Éventuellement compositeur ( musique menu & ambience )

## Principe des "Missions": 

*  Une mission est une tâche non-bloquante à réaliser sur ou à coté du jeu qui l'améliore d'une façon ou d'une autre.
* Peut être assignée à quelqu'un pour travailler dessus à son rythme
* Un superviseur (typiquement Hugo, dans un premier temps) est assigné pour surveiller, guider et évaluer le Stagiaire dans sa réalisation de sa tâche

## Missions disponibles

 * Refaire le site vitrine au propre
 * Refaire le système de comptes/login du site (actuellement c'est un truc bricolé en PHP recyclé d'un vieux projet datant de tout début 2014!)
 * Faire passer le "Core" d'un stub servant de démo technique à une bonne immitation de Minecraft, aussi bien sur le mode survie que créatif
 * Refaire le lanceur du jeu au propre
 * Écrire/maintenir un backend graphique OpenGL (en complément du nouveau backend Vulkan)
 * Plein d'autres sont envisageables! Voir https://github.com/Hugobros3/chunkstories-docs/blob/master/engine_tour/roadmap.md
 * Et https://github.com/Hugobros3/chunkstories-docs/blob/master/engine_tour/planned_features.md
 * Surtout ne pas hésiter à venir avec des idées de missions supplémentaires, le but ici sera aussi de créer une communauté de dévelopeurs qui créent du contenu indépendant.