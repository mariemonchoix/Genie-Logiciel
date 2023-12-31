**Tests unitaires**
===================

Ceci est le document qui permet de recenser les tests unitaires pour vérifier l'efficacité de notre dispositif. Pour cela, nous allons effectuer plusieurs tests qui seront décrit ci-dessous. Une validation pratique sera effectué pour garantir de l'efficacité et de la sécurité de notre dispositif.

**Tests liés au pacemaker**
----------------------------

- **Détection des battements cardiaques** : Tester la capacité du pacemaker à détecter les battements cardiaques naturels afin de ne pas envoyer des impulsions électriques en même temps que celles naturelles. 

*Validation* : le capteur de détection cardiaque capte une tension électrique comprise dans une marge définie entre 0 et 450 battements par minute.

- **Stimulation**: Tester la capacité du pacemaker à générer des impulsions électriques pour stimuler le cœur en cas de besoin grâce aux capteurs de détection.

*Validation* : Présence d'une tension en sortie du stimulateur lorsque la fréquence cardiaque est entre 0 et X battements par minute.

- **Batterie** : Tester la durée de vie de la batterie et la gestion de l'énergie du pacemaker.

*Validation* : Dans les conditions limites d'utilisation, on mesure les paramètres de la batterie (voltage ...).

- **Mode de sauvegarde** : Tester le basculement automatique vers un mode de sauvegarde en cas de défaillance du pacemaker principal. 

*Validation* : effectuer une stimulation et vérifier dans les logs qu'il y a bien des données enregistrées.

- **Réaction aux interférences électromagnétiques** : Tester la résistance du pacemaker aux interférences électromagnétiques externes.

*Validation* : induction d'un champ magnétique proche du pacemaker et vérifier son bon fonctionnement (vérification de présence d'impulsions en cas d'arythmie).

- **Tests de robustesse** : Tester la capacité du pacemaker à résister aux conditions environnementales défavorables (humidité, chocs, température, etc.).

*Validation* : Surveiller s'il surchauffe ou s'il s'arrête de fonctionner.

**Tests de simulation** : Tester le pacemaker à l'aide de simulateurs de signaux cardiaques pour valider son fonctionnement en toute sécurité.

*Validation* : Simuler différents rythmes cardiaques (sains ou pathologiques) et surveiller si le DM fonctionne correctement.

**Tests d'interopérabilité** : Tester la capacité du pacemaker à fonctionner avec d'autres dispositifs médicaux et systèmes de santé.

*Validation* : vérification à l’aide d’un moniteur, IRM, et radio et tester le bon fonctionnement (détection arythmie et correction)

**Tests de durée de vie** : Tester la durée de vie du pacemaker dans des conditions d'utilisation normale et extrême. 

*Validation* : induction d’une obsolescence programmée en réalisant plusieurs stimulations programmés (pour égaler la durée de vie maximale du PM), et voir à quel moment le PM ne fonctionne plus pour savoir sa durée de vie.

**Conformité aux normes réglementaires** : S'assurer que le pacemaker est conforme aux normes et réglementations médicales en vigueur.

*Validation* : vérification du PM par les organismes de santé qui délivre l’Autorisation de Mise sur le Marché (ANSM)


**Tests de performances à long terme** : Tester la performance du pacemaker sur une période prolongée pour évaluer sa fiabilité dans le temps.

*Validation* : voir s'il réussit à fonctionner malgré le vieillissement accéléré que nous effectuerons, induction d’une obsolescence programmée en réalisant plusieurs stimulations programmés et vérification de la correction d’arythmie


**Tests liés à la communication à un poste médical**
----------------------------------------------------

**Surveillance des paramètres du patient** : Tester la capacité du pacemaker à surveiller des paramètres tels que la fréquence cardiaque, la température, l'activité physique, etc. 

*Validation* : dès que la tension en sortie de la pile n'est plus constante, envoi d'une alarme au système de télésurveillance du médecin, vérifier que les données peuvent être récupérer dans la base de données du logiciel.

**Communication sans fil** : Tester la capacité du pacemaker à communiquer sans fil avec des dispositifs de contrôle et de suivi. 

*Validation* : émission de ping par le pacemaker et réception de ping via la plateforme de télémédecine

**Sécurité et confidentialité des données** : Tester les mécanismes de sécurité et de confidentialité pour protéger les données du patient. 

*Validation* : spam de ping vers le système du pacemaker, vérification de l'alarme auprès du système de télémédecine. Blocage du dispositif sur les paramètres enregistrés par le médecin et impossible de les modifier avant le prochain RDV en urgence chez le médecin

**Gestion des alarmes** : Tester la génération et la gestion des alarmes en cas de problèmes. 

*Validation* : en cas d'arythmie, vérification de la présence d'une alarme sur le système de télémmédecine.

**Gestion des mises à jour logicielles** : Tester la capacité de mettre à jour le logiciel du pacemaker de manière sécurisée. 

*Validation* : effectuer une mise à jour et surveiller la capacité du pacemaker à réagir à des variations de rythme cardiaque.

**Réponse aux erreurs et aux défaillances** : Tester la réponse du pacemaker aux erreurs et aux défaillances matérielles ou logicielles.

*Validation* : le logiciel demande une stimulation cardiaque alors que le rythme détécter par le pacemaker est dans la norme. Vérifier qu'aucune stimulation est envoyé dans ce cas par exemple.

**Évaluation de la sécurité des communications sans fil** : Tester la sécurité des communications sans fil entre le pacemaker et les dispositifs de contrôle.

*Validation* : savoir si les signaux sont toujours récupérable dans différentes situations (pacemakers sous une certaine profondeur terrestre ou hauteur aérienne).


