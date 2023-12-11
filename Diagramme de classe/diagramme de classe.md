Diagramme de classe
======================

Définition
-----------

Un diagramme de classe est une représentation visuelle et schématique d'une structure de données et de la relation entre les entités dans un système logiciel. Il fait partie des outils de modélisation UML (Unified Modeling Language) largement utilisés dans le domaine du développement logiciel pour concevoir, documenter et communiquer des concepts et des structures de manière claire et compréhensible.
Un diagramme de classe est principalement utilisé pour visualiser les classes, les objets, les attributs, les méthodes et les relations entre eux dans un système logiciel.
Les composants principaux d'un diagramme de classe sont : 

- **Les classes** : Un diagramme de classe est principalement utilisé pour visualiser les classes, les objets, les attributs,les méthodes et les relations entre eux dans un système logiciel.Chaque classe représente un concept ou une entité du monde réel, tels que des personnes, des voitures, des factures, etc. Elles servent de moule à partir duquel des objets individuels sont instanciés.

  
- **Les attributs** : Les attributs sont des caractéristiques ou des données associées à une classe. Ils représentent les propriétés de base de la classe et sont généralement définis comme des variables. Par exemple, une classe "Personne" pourrait avoir des attributs tels que "nom", "âge" et "adresse".


- **Les méthodes** : Les méthodes sont les comportements ou les actions que les objets de la classe peuvent effectuer. Elles sont définies comme des fonctions ou des procédures qui manipulent les attributs de la classe. Par exemple, une classe "Voiture" pourrait avoir des méthodes comme "démarrer" et "arrêter".


- **Les relations** : Les relations entre les classes décrivent comment les classes interagissent les unes avec les autres. Les types de relations courantes incluent l'association, l'agrégation, la composition, l'héritage, l'implémentation, etc. Ces relations montrent comment les objets de différentes classes collaborent pour réaliser des fonctionnalités plus complexes.

  
- La visibilité :  Chaque attribut ou méthode dans une classe peut avoir une visibilité spécifiée, telle que publique (+), privée (-) ou protégée (#). Cela indique quelles parties du code peuvent accéder à ces éléments.
  


Notre Diagramme de classe 
--------------------


Voici à quoi correspond chaque classe dans notre diagramme de classe :



![Diagramme sans nom](https://github.com/mariemonchoix/Genie-Logiciel/assets/147620874/d8eea5f6-d7e1-40d5-b06c-399cf64881f8)



Nous avons donc 3 classes : une classe Pacemaker, une classe Données ECG et une classe Mode Turbo. 


Notre classe pacemaker représente le pacemaker lui-même et permet de faire toutes les fonctions liées à notre pacemaker, c'est à dire envoyer les données au médecin grâce à la fonction EnvoieMedecin, récupérer les données du patient avec récupèredonnéepatients et envoyer des impulsions électriques pour stimuler les muscles cardiaques grâce à la fonction EnvoieImpulsions.


Notre classe ECG permet d'avoir toutes les données du coeur (par exemple le rythme cardiaque) essentielles pour le bon fonctionnement du pacemaker. Puis nous avons rajouter  classe Mode Turbo fictive pour montrer que nous avions bien compris le fonctionnement d'un diagramme de classe.
