Code qui pourrait fonctionner pour coder le fonctionnement de notre pacemaker 
----------------------------------------------------------------------------------

**Code en python**



On crée une classe Pacemaker qui collecte et envoie des données de santé simulées à un médecin. 
Pour simuler l'envoi en temps réel des informations, nous utiliserons simplement une fonction envoyer_donnees qui imprimera les données pour faire une démonstration. En situation réelle, cela nécessiterait une communication en ligne avec un système de transmission approprié.
On va écrire le code en simulant des données.





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
