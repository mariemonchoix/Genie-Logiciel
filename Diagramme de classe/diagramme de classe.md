comment on fait pour que les classes interagissent
main un while, une bouce infini
comment faire en sorte que ca marche eternellment
classe constitue d'objets : switch on off...
le main tant quon a du courant fait le truc
objet qui centralise le tout ? 
interaction d'objet = structure
creer des objets
et main = 10 lignes : créer l'objet et declanche 
héritage

attribut et fonction en dessous


Notre diagramme de classes
======================

Définition
-----------

Un diagramme de classe est une représentation visuelle et schématique d'une structure de données et de la relation entre les entités dans un système logiciel. Il fait partie des outils de modélisation UML (Unified Modeling Language) largement utilisés dans le domaine du développement logiciel pour concevoir, documenter et communiquer des concepts et des structures de manière claire et compréhensible.
Un diagramme de classe est principalement utilisé pour visualiser les classes, les objets, les attributs, les méthodes et les relations entre eux dans un système logiciel.
Les composants principaux d'un diagramme de classe sont : 

- Les classes : Un diagramme de classe est principalement utilisé pour visualiser les classes, les objets, les attributs,les méthodes et les relations entre eux dans un système logiciel.Chaque classe représente un concept ou une entité du monde réel, tels que des personnes, des voitures, des factures, etc. Elles servent de moule à partir duquel des objets individuels sont instanciés.

  
- Les attributs : Les attributs sont des caractéristiques ou des données associées à une classe. Ils représentent les propriétés de base de la classe et sont généralement définis comme des variables. Par exemple, une classe "Personne" pourrait avoir des attributs tels que "nom", "âge" et "adresse".


- Les méthodes : Les méthodes sont les comportements ou les actions que les objets de la classe peuvent effectuer. Elles sont définies comme des fonctions ou des procédures qui manipulent les attributs de la classe. Par exemple, une classe "Voiture" pourrait avoir des méthodes comme "démarrer" et "arrêter".


- Les relations : Les relations entre les classes décrivent comment les classes interagissent les unes avec les autres. Les types de relations courantes incluent l'association, l'agrégation, la composition, l'héritage, l'implémentation, etc. Ces relations montrent comment les objets de différentes classes collaborent pour réaliser des fonctionnalités plus complexes.

  
- La visibilité :  Chaque attribut ou méthode dans une classe peut avoir une visibilité spécifiée, telle que publique (+), privée (-) ou protégée (#). Cela indique quelles parties du code peuvent accéder à ces éléments.
  


Diagramme de classe 
--------------------




|           Pacemaker                |
------------------------------------


-------------------------------------

- id: int                         
- patient: Patient                
- telemetry: TelemetryModule      



 + getPacemakerID(): int           
 + getPatient(): Patient           
 + setPatient(patient: Patient):   
 + getTelemetry(): TelemetryModule 
 + setTelemetry(telemetry:        
 TelemetryModule):                
 + sendTelemetryData(): void      



|           TelemetryModule          |
-------------------------------------
--------------------------------------


 - telemetryData: TelemetryData[]   
-------------------------------------

+ collectData(): void
+ transmitData(): void            
+ storeData(): void               



|           TelemetryData            |
-------------------------------------


 - dataID: int                     
 - heartRate: int                  
 - ECG: ECGData                    
 - activityLevel: int              
-------------------------------------
| + getDataID(): int                |
| + getHeartRate(): int             |
| + getECGData(): ECGData           |
| + getActivityLevel(): int         |
-------------------------------------

-------------------------------------
|            ECGData                 |
-------------------------------------
| - ecgID: int                      |
| - dataPoints: int[]               |
-------------------------------------
| + getECGID(): int                 |
| + getDataPoints(): int[]          |
-------------------------------------

-------------------------------------
|            Patient                 |
-------------------------------------
| - patientID: int                  |
| - name: string                    |
| - dateOfBirth: Date               |
| - medicalHistory: string[]        |
-------------------------------------
| + getPatientID(): int             |
| + getName(): string               |
| + getDateOfBirth(): Date          |
| + getMedicalHistory(): string[]   |
| + addMedicalRecord(record: string)|
-------------------------------------

Pacemaker : Représente le pacemaker lui-même avec des attributs tels que l'identifiant, le patient associé et un module de télémétrie. Il possède des méthodes pour accéder à ces attributs et pour envoyer des données de télémétrie.

TelemetryModule : Représente le module de télémétrie qui collecte, transmet et stocke les données de télémétrie. Il a des méthodes pour effectuer ces opérations.

TelemetryData : Représente les données de télémétrie collectées, y compris le rythme cardiaque, les données ECG et le niveau d'activité. Il a des méthodes pour accéder à ces données.

ECGData : Représente les données ECG spécifiques, y compris un identifiant et les points de données ECG.

Patient : Représente le patient associé au pacemaker, avec des attributs tels que l'identifiant, le nom, la date de naissance et l'historique médical. Il possède des méthodes pour accéder à ces informations et pour ajouter des enregistrements médicaux.
