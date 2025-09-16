# Plugin WordPress — Suivi de projet client (via API Zoho CRM)

**Type de projet :** Plugin WordPress personnalisé
**Technologies :** WordPress, PHP, JavaScript (AJAX), API Zoho CRM (REST), HTML/CSS
**Date de réalisation :** 2024
**Client / Organisation :** Richard et Levesque — site web officiel
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Permettre aux entrepreneurs/clients de **consulter l’avancement de leur projet** directement depuis le site web de l’entreprise.
- Rendre l’information claire et transparente en synchronisant l’état du projet avec Zoho CRM.
- Réduire les demandes de suivi manuel adressées à l’équipe.

## Description

Ce plugin WordPress fournit une interface sur le site web permettant aux clients d’entrer une **référence de projet** (numéro ou code).  
Le plugin interroge l’**API Zoho CRM** pour récupérer les données associées au projet, puis affiche le **statut** de manière visuelle et conviviale.

Le statut est basé sur le champ **Stage** du projet dans Zoho CRM, avec un mapping défini (par exemple :

- Prospect → “Projet en soumission”
- En cours → “Projet en production”
- Terminé → “Projet complété”).

## Fonctionnalités principales

- Champ de saisie client (numéro de projet / code).
- Connexion à l’API Zoho CRM pour récupérer les infos en temps réel.
- Conversion du champ _Stage_ en statut lisible pour le client.
- Affichage sous forme de **barre de progression** ou de **timeline visuelle**.
- Gestion des erreurs (projet introuvable, problème API).

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Authentification et gestion des tokens Zoho CRM.  
    **Solution :** Mise en place du système OAuth avec rafraîchissement automatique et stockage sécurisé.
- **Problème :** Traduction du champ _Stage_ CRM en statuts parlants pour le client.  
    **Solution :** Création d’un mapping personnalisé entre les valeurs CRM et des libellés simplifiés + design graphique.
- **Problème :** Expérience utilisateur fluide sans rechargement de page.  
    **Solution :** Implémentation d’AJAX pour la requête Zoho et mise à jour dynamique de l’interface.

## Résultats / Impact

- Amélioration de la transparence et de la communication avec les clients.
- Réduction du nombre de demandes manuelles de suivi de projet.
- Image plus moderne et professionnelle de l’entreprise grâce à un outil interactif sur le site web.

## Notes techniques / apprentissages

- Utilisation de l’API REST de **Zoho CRM** avec authentification OAuth.
- Shortcode pour intégrer le formulaire de suivi sur n’importe quelle page.
- Mapping `Stage` Zoho → statut client défini dans une fonction PHP configurable.
- Extensible : ajout possible de notifications par e-mail lorsque le projet change de statut.

## Tags

#Plugin #WordPress #PHP #ZohoCRM #API #Clients #portfolio #réalisations