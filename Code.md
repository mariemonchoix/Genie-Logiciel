Code qui pourrait fonctionner pour coder le fonctionnement de notre pacemaker 
----------------------------------------------------------------------------------

**Code en python**



On crée une classe Pacemaker qui collecte et envoie des données de santé simulées à un médecin. 
Pour simuler l'envoi en temps réel des informations, nous utiliserons simplement une fonction envoyer_donnees qui est utilisée pour simuler l'envoi des données au médecin, imprimera les données pour faire une démonstration. Dans un environnement réel, cette fonction serait modifiée pour effectuer une transmission réelle des données à un système de surveillance ou à un médecin, peut-être via des protocoles de communication appropriés comme HTTP, MQTT, ou d'autres méthodes de communication réseau.
On a écrit le code en simulant des données aléatoires.
Dans le code, on utilise une boucle infinie pour simuler la collecte et l'envoi en temps réel des données ECG. 



import time

import random


**classe Pacemaker:**


    def collecter_donnees_ECG(self):  # On simule la collecte de données ECG
        donnees_ECG = self.generer_donnees_ECG()
        return donnees_ECG
    
    def generer_donnees_ECG(self):
        # On simule la génération de données aléatoires d'ECG
        return random.randint(60, 100)  # Simulation du rythme cardiaque

    def envoyer_donnees(self, donnees):
        # On simule l'envoi des données au médecin (pour l'exemple, affichage des données)
        print("Envoi des données au médecin : {donnees}")
        

**Fonction principale de simulation de l'utilisation du pacemaker**



def simulation_pacemaker():
    
    pacemaker = Pacemaker()
  
    while True:
        # Collecte des données ECG
        donnees_ECG = pacemaker.collecter_donnees_ECG()

        # Envoi des données au médecin en temps réel
        pacemaker.envoyer_donnees(donnees_ECG)

        # Attente de quelques secondes avant la prochaine collecte/envoi de données
        time.sleep(5)  # Attente de 5 secondes pour simuler une période de collecte en temps réel

**Lancement de la simulation**


simulation_pacemaker()
