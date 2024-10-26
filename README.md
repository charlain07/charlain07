
# Système de Gestion de Parc Automobile pour Entreprise de Location

## Description
Cette application permet de gérer le parc de véhicules d' une entreprise géolocalisée .  Elle offre des fonctionnalités permettant d' ajouter des voitures et des clients, de louer et de restituer des voitures et de visualiser les voitures  disponibles . L' application utilise les principes de la programmation orientée objet et met en œuvre des idées importantes telles que l'héritage, le polymorphisme, l'encapsulation et la gestion des exceptions .



## Fonctionnalités

1. **Ajouter un véhicule**
   l'utilisateur peut choisir parmi les types suivants pour ajouter un nouveau véhicule au parc :
   - Voiture : Indiquer le nombre d' emplacements et type de carburant .

   Camion : précise le nombre d' essieux et la capacité de charge .

2. **Employez un client**  
   L' l'utilisateur peut ajouter un client en fournissant son nom, son prénom , son numéro de permis de conduire et son numéro de téléphone .son numéro de permis et son numéro de téléphone .

3. **Louer une voiture**  
   Permettre à un client de louer une voiture qui est disponible.. Pour commander pour l' application calcule le prix total en fonction de la durée, l' utilisateur doit préciser les dates de début et de fin de l' application location .pour calculer le prix total en fonction de la durée, l' utilisateur doit préciser les dates de début et de fin de la location.

La possibilité de modifier le statut d' un véhicule loué afin de le rendre à nouveau disponible est connue sous le nom de « restitution de véhicule ».Le fait de rendre un véhicule à nouveau disponible est connu sous le nom de « retour d’un véhicule ».

5. ** Une liste des véhicules disponibles ** Affichant une liste complete des vehicules encore en liste pour un renouvellement de location**​
6. **Quitter l'application**  
   Permet de sortir de l'application en toute sécurité.

---

## Structure du Projet

Le projet est organisé en plusieurs classes pour assurer une architecture modulaire et claire.

### Classes Principales

**Véhicule de Classe Abstraite "  
  Une fondationclasse classepour tous types de véhicules.pour tous types de véhicules. Il comprend des informations communesdes informations tel quetelles que le numéro d'immatriculation du véhicule , la marque, le modèle, l'année d' entretien, le kilométrage et le statut (prêté ou disponible).le numéro d'immatriculation du véhicule , la marque, le modèle, l'année de service, le kilométrage et le statut (prêté ou disponible). Une méthode abstraiteméthode appeléappelée « calculerPrixLocation » est définie pour les sous-classes à utiliser.« calculerPrixLocation » est défini pour les sous-classes à utiliser.


SOUS-classe de Véhicule (Voiture)  
  représente une voiture d' un certain type, avec des caractéristiques particulières telles que le nombredes caractéristiques detelles que le nombre de sièges et le type de carburant .sièges et type de carburant . Mettez en pratique l' interface « Louable » .

(Sous-classe de Véhicule) Camion  
  Ce véhiculetype taperreprésente un camion avec certaines caractéristiques comme la capacité de charge et le nombre d'essieux .représente un camion avec certaines caractéristiques comme la capacité de charge et le numéro d'essieu . Mettez en pratique l' interface « Louable » .

**Client**  
  les informations familiales du client (nom, prénom , numéro de permis , numéro de téléphone ), et conserve une trace de tous les lieux visités.

- **ParcAutomobile**  
  Gère la liste de tous les véhicules et clients. Fournit des méthodes pour ajouter des véhicules et des clients, louer et retourner des véhicules, et afficher les véhicules disponibles.

- **Location**  
  Représente un contrat de location avec un client et un véhicule spécifique, ainsi que les dates de début et de fin de la location. Calcule automatiquement le prix total de la location en fonction de la durée.

### Interfaces

- **Louable**  
  Interface qui impose la définition des méthodes `louer` et `retourner`, permettant de gérer le changement de statut des véhicules (disponible ou loué).

### Exceptions Personnalisées

- **VehiculeIndisponibleException**  
  Exception levée lorsqu'un véhicule déjà loué est demandé pour une nouvelle location.

- **ClientNonAutoriseException**  
  Exception levée lorsqu'un client tente de louer un véhicule (comme un camion) sans autorisation adéquate (cette logique peut être étendue selon les besoins).

---

## Instructions pour l'Utilisation

1. **Lancer l'Application**  
   Exécutez le fichier principal qui contient le `main` dans la classe `ParcAutomobile`.

2. **Suivre le Menu Interactif**  
   À l'exécution, un menu interactif s'affiche avec les options :
   - `1` pour ajouter un véhicule
   - `2` pour ajouter un client
   - `3` pour louer un véhicule
   - `4` pour retourner un véhicule
   - `5` pour lister les véhicules disponibles
   - `0` pour quitter l'application

3. **Navigation dans le Menu**  
   Saisissez le numéro correspondant à l'action souhaitée et suivez les instructions affichées.

---

## Exemple de Flux d'Utilisation

1. **Ajouter une Voiture** : Choisissez l'option 1, entrez les informations de la voiture, puis ajoutez-la au parc.
2. **Ajouter un Client** : Choisissez l'option 2, saisissez les informations du client, puis enregistrez-le.
3. **Louer un Véhicule** : Choisissez l'option 3, entrez le nom du client, sélectionnez le véhicule, et spécifiez les dates de location.
4. **Retourner un Véhicule** : Choisissez l'option 4 et entrez l'immatriculation du véhicule pour le rendre disponible.

---

## Remarques

- La classe `ParcAutomobile` utilise des collections `ArrayList` pour stocker les clients et les véhicules.
- L'application est conçue pour être extensible et pourrait être améliorée avec une interface graphique (GUI) ou en ajoutant des fonctionnalités supplémentaires, telles que des vérifications d’autorisation plus avancées pour les locations de véhicules spécifiques.

---

