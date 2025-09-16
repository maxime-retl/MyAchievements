# Plugin WordPress — Gestion des activités du Club Social

**Type de projet :** Plugin WordPress personnalisé
**Technologies :** WordPress, PHP, ACF, MySQL, HTML/CSS, JavaScript
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque — Club Social)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Offrir un espace interne pour la gestion et la participation aux activités du Club Social.
- Permettre aux administrateurs d’ajouter, modifier et supprimer facilement des activités.
- Permettre aux employés de consulter la liste des activités, de filtrer selon leurs préférences et de voter/participer.

## Description

Ce plugin WordPress développé sur mesure permet la gestion complète des **activités du Club Social** de l’entreprise.  
Il comprend une interface côté **administration** pour gérer les contenus et une interface côté **utilisateurs** pour l’affichage et l’interaction.

## Fonctionnalités principales

- **Côté Admin**
    - Création, modification et suppression d’activités.
    - Gestion des détails via des champs personnalisés (titre, description, date, lieu, type d’activité, image, etc.).
    - Suivi des votes/participations.
- **Côté Client (employés)**
    - Liste des activités disponibles avec mise en page en cartes.
    - Filtres dynamiques par type ou catégorie.
    - Fonction de **vote/participation** pour exprimer son intérêt.

## Screenshots / Visuels

_(Remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Créer un système de vote sans plugin tiers.  
    **Solution :** Mise en place d’une table SQL personnalisée reliée aux utilisateurs pour stocker les votes et assurer un suivi unique par utilisateur.
- **Problème :** Affichage flexible et filtrable côté client.  
    **Solution :** Utilisation de requêtes WP_Query personnalisées et filtres dynamiques (AJAX) pour un rendu fluide.

## Résultats / Impact

- Amélioration de l’engagement des employés envers le Club Social.
- Simplification de la gestion pour les administrateurs.
- Outil centralisé, intégré directement au portail interne WordPress.

## Notes techniques / apprentissages

- Création d’un **Custom Post Type** `activites`.
- Utilisation de **champs personnalisés ACF** pour stocker les informations des activités.
- Shortcodes pour afficher les activités côté client.
- Table personnalisée pour gérer les votes.
- Extensible vers d’autres usages (ex. événements RH, sondages).

## Tags

#Plugin #WordPress #PHP #ACF #ClubSocial #portfolio #réalisations