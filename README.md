# web3D-project

## Sommaire
**[Liens utiles](https://github.com/williamkann/web3D-project#liens-utiles)**

**[Lancer le projet](https://github.com/williamkann/web3D-project#lancer-le-projet)**

**[Notre organisation de projet](https://github.com/williamkann/web3D-project#notre-organisation-de-projet)**

**[La méthode de réalisation employée](https://github.com/williamkann/efrei-m2-otter-worlds#la-methode-de-realisation-employee)**

**[Les fonctionnalités à réaliser](https://github.com/williamkann/efrei-m2-otter-worlds#les-fonctionnalités-à-réaliser)**

**[Les difficultés rencontrées](https://github.com/williamkann/efrei-m2-otter-worlds#les-difficultés-rencontrées)**

**[Résumé technique](https://github.com/williamkann/efrei-m2-otter-worlds#technical-round-up)**

**[Auteurs](https://github.com/williamkann/efrei-m2-otter-worlds#authors)**



### Liens utiles
Voici le lien du dépôt Github :
 ```
https://github.com/williamkann/web3D-project
```

Et voici les liens de démonstration du site :
 ```
partie maison : https://share.vidyard.com/watch/QNXdddVYHVpUFKGriw7ABJ
partie zoo : https://share.vidyard.com/watch/VoqbUAkKLFWtRVES9X56X9
 ```



### Lancer le projet
La programmation est fonctionnelle ; il suffit juste de lancer le site web.
Nous avons développé ce site grâce au serveur Nginx, qui permet de déployer des sites localement.

```
  Téléchargez le projet et placez-le dans le dossier HTML
  Lancez le serveur Nginx
  Allez à l'url suivante : http://localhost/web3D-project/Projet/Sujet.html
```



### Notre organisation de projet
Le projet a été divisé en 2 parties distinctes : 
- Partie 1 : modélisation d’un moyen de consultation de bâtiment. Le bâtiment présenté dans cette partie sera une maison avec diverses pièces.
- Partie 2 : modélisation d’un zoo avec des animaux. Cette partie est libre et plus vaste, nous avons décidé d’assigner cela à 2 personnes. 
	

La première phase du projet consistait d’abord à se familiariser avec les modèles récupérés depuis des sites d’hébergement tels que Sketchfab. Nous avons décidé d’utiliser majoritairement des modèles au format glTF. 

La deuxième phase a été d’obtenir ces modèles au format glTF notamment en passant par Blender si besoin. Donc il a fallu en apprendre davantage sur ce logiciel. 

La troisième phase du projet consiste à tout mettre en place sur le site. Tout d’abord, les primitives du type box sont placées dans la scène afin d’avoir une prévisualisation du lieu de chaque composant. Ensuite, nous avons mis en place chaque modèle voulu. Enfin, nous avions modélisé la map permettant de pouvoir naviguer dans la scène en sélectionnant les pièces voulues.



### La méthode de réalisation employée
Nous avons utilisé Nginx, un serveur web permettant de  déployer localement notre site. Le code est situé dans le dossier HTML du serveur Nginx.

Le polyfill utilisé est X3DOM, et est pointé depuis les pages HTML du projet.



### Les fonctionnalités à réaliser
#### Partie 1 : la maison

Cette partie concerne la consultation d’un bâtiment composé de différentes salles qui reflètent la structure habituelle d’une maison.

Afin de peupler l’intérieur de la scène, nous disposerons différents modèles avec lesquels nous pouvons interagir, à savoir :
  Chambre: armoire
  Salon: manette de jeu, boisson sur la table
  Cuisine: fruits sur la table
  Jardin: chat, barbecue
  Garage: boîte à outils
  Salle de bain: un habitant de la maison


#### Partie 2 : le zoo

Cette partie concerne une petite ferme / un zoo avec des animaux. Si l’on clique sur un animal, on peut consulter des informations supplémentaires le concernant, ainsi qu’afficher les interactions possibles avec lui.



### Nos réalisations
En plus du cahier des charges initial, et afin d’ajouter de l’interactivité, rendant le site d’une consultation passive à une véritable interaction avec l’utilisateur, certains éléments 3D sont cliquables, et affichent des informations qui leurs sont relatives en bas à gauche de l’écran.

Aussi, pour fluidifier la navigation dans les scènes 3D, nous mettons à disposition une carte 2D avec les différentes pièces ou espaces présentés. L’utilisateur pourra naviguer dans la scène avec la sélection de la pièce à visualiser. Ces zones sont distinctes, et l’on a une navigation pièce-par-pièce. Cela dit, la navigation dans la scène peut aussi s’effectuer avec la souris et la molette afin d’avoir des vues personnalisées. Nous avons donc la possibilité de naviguer soit par la carte 2D, soit par une navigation via la souris de l’utilisateur.

Enfin, l’utilisateur peut facilement choisir le mode de navigation pour observer les modèles 3D (examine, fly, look-at…) grâce à un dropdown, en haut à droite, sur la barre de navigation.

Concernant l’interface, le framework Materialize a été utilisé pour sa simplicité de mise en place et d’utilisation, et pour l’UI / l’UX améliorés qu’il apporte au projet.

#### Partie 1 : la maison
Concernant les réalisations obtenues, nous avons pu mettre en place la scène 3D de notre bâtiment. La disposition des modèles dans le décor ont aussi été réalisées. De plus, les interactions sont aussi disponibles sur les modèles mentionnés précédemment. Enfin, la map 2D de navigation a été bien mappée (découpage de chaque zone de la carte) et la visualisation des points spécifiques de chaque pièce est fonctionnelle.

L’IHM permet à l’utilisateur de choisir de naviguer librement dans la scène 2D mais aussi avec le plan 2D.


#### Partie 2 : le zoo
Pour ce qui est du zoo, la scène 3D consiste davantage en une surface d’herbe sur laquelle une plateforme est construite en assemblant différentes primitives ensemble (des escaliers, une plateforme surélevée ainsi que d’une sortie et d’une entrée). Différents modèles 3D parsèment aussi le zoo, que ce soit des animaux comme prévu, ou des visiteurs, afin de rendre le zoo plus dynamique que prévu. Une fois encore, des interactions sont disponibles sur les modèles des animaux et des visiteurs. Pour ce qui est d’un plan 2D, nous estimons que l’architecture proposée ne se prêtait pas à la création d’un plan, puisqu’il s’agit ici d’un sol et d’une surface centrale, et non pas d’un bâtiment composé de différentes pièces clairement définies.



### Les difficultés rencontrées
Ce projet a été l’occasion pour nous de découvrir la 3D avec le web. Nous avions un background en web, notamment grâce à des frameworks JavaScript ; cependant, nous avons rencontré plusieurs difficultés concernant quelques points :
La gestion de nombreux formats disponibles (X3D / Collada / glTF). Au début du projet, il a été difficile pour nous de comprendre les distinctions entre ces formats.
Effectuer des conversions entre chaque format et surtout gérer les textures pour chaque format ; tout cela s’est effectué avec Blender.
Gérer aussi la dispositions des modèles dans la scène avec les balises transform. Il a fallu d’abord visualiser cela avec des primitives pour ensuite pouvoir mettre en place nos modèles.

Avec nos expériences en VueJS, nous avons voulu mettre en place la scène avec  ce framework JavaScript. Cependant, des difficultés de rendu nous ont ralenti, que ce soit en local ou sur une version déployée en ligne ; afin de s’assurer que le site fonctionne correctement pour tout le monde, nous avons préféré revenir à des fichiers HTML natifs  déployé avec le serveur Nginx, comme vu en cours.



## Résumé technique
The whole project was made using :
* **[glTF](https://www.khronos.org/gltf)** - GL Transmission Format - type de modèle 3D préféré pour ce projet
* **[Materialize](https://materializecss.com/)** - Framework front-end pour l’UI / L’UX reprenant les codes de Google
* **[Nginx](https://www.nginx.com)** - Serveur permettant de déployer des sites HTML en local
* **[Sketchfab](https://sketchfab.com)** - Bibliothèque de modèles 3D sous différents formats
* **[Sketchup](https://www.sketchup.com)** - Modélisation d’environnement 3D
* **[X3DOM](https://www.x3dom.org)** -  Polyfill permettant l’affichage de modèles 3D dans une page HTML



## Auteurs
Ce projet a été fait par ces étudiants à l'Efrei Paris :
* **ABDMEZIEM Théo** - [his Git repository](https://github.com/opsilonn)
* **BEGEOT Hugues** - [his Git repository](https://github.com/opsilonn)
* **KANN William** - [his Git repository](https://github.com/patatart)

Voir aussi la liste de [contributeurs](https://github.com/williamkann/web3D-project/-/graphs/main) qui ont participé à ce projet.

Note : Nous sommes actuellement dans notre 5ème année (2020-21), dans un cursus de Software Engineering.
