# Plugin WordPress — Anniversaires & ancienneté des employés

**Type de projet :** Plugin WordPress personnalisé
**Technologies :** WordPress, PHP, ACF, MySQL, HTML/CSS, JavaScript
**Date de réalisation :** 2024
**Client / Organisation :** Usage interne (Richard et Levesque — Portail interne)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Afficher automatiquement les **anniversaires** et **anniversaires d’ancienneté** des employés sur le portail interne.
- Centraliser ces informations pour améliorer la communication et la reconnaissance en entreprise.
- Offrir une présentation claire et agréable aux employés.

## Description

Ce plugin WordPress développé sur mesure permet de lister et de mettre en avant :

- Les **anniversaires** des employés.
- Les **anniversaires d’ancienneté** (nombre d’années dans l’entreprise).

Les informations sont récupérées depuis la base de données RH intégrée au portail (via champs ACF ou table dédiée).  
Les événements à venir sont affichés sous forme de **widget** ou **bloc**, directement sur la page d’accueil du portail interne.

## Fonctionnalités principales

- Récupération des données de chaque employé (date de naissance, date d’embauche).
- Calcul automatique des anniversaires et anciennetés.
- Affichage dans un bloc moderne, trié par date à venir.
- Mise en avant des événements du jour ou de la semaine.
- Option de filtrage (ex. anniversaires uniquement, ancienneté uniquement).

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Gestion des dates récurrentes (anniversaire chaque année).  
    **Solution :** Utilisation des fonctions PHP `DateTime` pour comparer mois/jour indépendamment de l’année.
- **Problème :** Calcul des années d’ancienneté de manière dynamique.  
    **Solution :** Soustraction des années à partir de la date d’embauche et affichage du nombre d’années exact.

## Résultats / Impact

- Amélioration du climat social et de la reconnaissance entre collègues.
- Meilleure communication interne grâce à une visibilité centralisée.

## Notes techniques / apprentissages

- Création d’un **shortcode** `[anniversaires]` pour insérer la liste n’importe où sur le portail.
- Utilisation de champs ACF personnalisés (`date_naissance`, `date_embauche`).
- Tri et affichage dynamique avec `WP_Query` + fonctions PHP de manipulation des dates.
- Extension possible : notifications automatiques par e-mail / Teams le jour de l’événement.

## Tags

#Plugin #WordPress #PHP #ACF #Anniversaires #RH #portfolio #réalisations