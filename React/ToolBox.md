# ToolBox — Suite d’outils de conversion et calculs techniques

**Type de projet :** Application web (React)
**Technologies :** React, TailwindCSS, React Router
**Date de réalisation :** 2025
**Client / Organisation :** Richard et Levesque — Outil interne
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Centraliser plusieurs **outils techniques** utiles aux employés dans une seule interface.
- Offrir une solution rapide et fiable pour réaliser des conversions et calculs spécifiques liés aux métiers de R&L.
- Simplifier le quotidien des utilisateurs en réduisant le besoin de multiples fichiers Excel ou calculatrices externes.

## Description

**ToolBox** est une application React moderne regroupant plusieurs utilitaires :

- **Conversions de mesures et poids** (pouces ↔ mm, kg ↔ lbs, etc.).
- **Calculateur de poids de porte** : selon les dimensions et matériaux.
- **Calculateur de poids de verre** : surface × épaisseur × densité.
- **Calculateur de dimensions de verre pour porte** : à partir des dimensions de la porte et des marges définies.

L’application est responsive et conçue pour une utilisation rapide, que ce soit en atelier, au bureau ou sur chantier.

## Fonctionnalités principales

- Interface simple en **onglets** ou **cartes** pour sélectionner un outil.
- Conversions instantanées avec validation des entrées.
- Formules intégrées pour le calcul du poids des portes et vitrages.
- Résultats présentés de manière claire, avec arrondis adaptés.

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Assurer la précision des conversions et formules métier.  
    **Solution :** Utilisation de bibliothèques fiables (**math.js**) et validation par rapport aux méthodes de calcul internes déjà utilisées (Excel, manuels).
- **Problème :** Interface intuitive malgré plusieurs outils différents.  
    **Solution :** Organisation par modules/onglets et design épuré basé sur **TailwindCSS**.

## Résultats / Impact

- Gain de temps pour les employés (calculs rapides, accessibles partout).
- Réduction des erreurs liées à des conversions manuelles ou approximatives.
- Outil polyvalent, adaptable à plusieurs départements (production, design, estimation).

## Notes techniques / apprentissages

- Projet basé sur **React** pour robustesse et maintenabilité.
- Styling avec **TailwindCSS** pour rapidité de design.
- Architecture modulaire (chaque outil = un composant React dédié).
- Extensible facilement pour ajouter d’autres outils (ex. calcul de prix, optimisation de coupe).

## Tags

#React #TypeScript #TailwindCSS #Calculateur #Conversion #OutilsTechniques #portfolio #réalisations