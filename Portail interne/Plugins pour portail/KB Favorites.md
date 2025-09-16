# Plugin WordPress — Favoris sur la base de connaissance

**Type de projet :** Plugin WordPress personnalisé
**Technologies :** WordPress, PHP, MySQL, JavaScript (AJAX), HTML/CSS
**Date de réalisation :** 2024
**Client / Organisation :** Usage interne (Richard et Levesque — Portail interne)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Permettre aux utilisateurs d’ajouter facilement en **favoris** les articles de la base de connaissance.
- Offrir un accès rapide aux articles les plus utiles pour chaque employé.
- Améliorer l’expérience utilisateur et la rétention des connaissances.

## Description

Ce plugin WordPress ajoute un système de **favoris** dans la base de connaissance interne.  
Chaque article dispose d’un bouton (ex. icône étoile ou cœur) que l’utilisateur peut activer/désactiver.  
Les favoris sont stockés dans la base, liés à l’utilisateur connecté, et accessibles dans une **page dédiée “Mes Favoris”**.

## Fonctionnalités principales

- Bouton **Ajouter/Retirer des favoris** directement sur les articles.
- Sauvegarde des favoris par utilisateur (lié au compte WordPress).
- Liste personnalisée des favoris accessible via un shortcode ou une page dédiée.
- Gestion en AJAX pour éviter le rechargement de la page.
- Icône visuelle dynamique (remplie si déjà en favoris, vide sinon).

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Associer les favoris à chaque utilisateur connecté.  
    **Solution :** Utilisation d’une table personnalisée ou de la table `usermeta` pour stocker les IDs des articles favoris.
- **Problème :** Rendre l’expérience fluide (sans rechargement).  
    **Solution :** Implémentation d’un appel AJAX en PHP pour ajouter/retirer les favoris instantanément.

## Résultats / Impact

- Amélioration de l’ergonomie et de la personnalisation de la base de connaissance.
- Les employés retrouvent plus vite les articles utiles, réduisant le temps de recherche.
- Adoption renforcée du portail interne comme ressource de référence.

## Notes techniques / apprentissages

- Shortcode pour afficher la liste des articles favoris de l’utilisateur.
- Vérification des droits (seulement pour utilisateurs connectés).
- Icône dynamique changée via JavaScript lors du clic.
- Extensible : possibilité d’ajouter un système de classement (ex. top 10 des articles les plus ajoutés en favoris).

## Tags

#Plugin #WordPress #PHP #AJAX #Favoris #BaseDeConnaissance #portfolio #réalisations