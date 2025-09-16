# Plugin WordPress — Horloges mondiales

**Type de projet :** Plugin WordPress personnalisé
**Technologies :** WordPress, PHP, JavaScript (Date API / moment.js ou day.js), HTML/CSS
**Date de réalisation :** 2024
**Client / Organisation :** Usage interne (Richard et Levesque — Portail interne)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Mettre en avant la diversité des nationalités et régions représentées au sein des employés de R&L.
- Créer un affichage visuel d’**horloges mondiales** directement sur le portail interne.
- Apporter un clin d’œil convivial et culturel, tout en facilitant la prise en compte des fuseaux horaires lors des échanges.

## Description

Ce plugin WordPress affiche une série d’**horloges mondiales** correspondant aux pays/régions où travaillent ou vivent les employés de l’entreprise.  
L’affichage est dynamique (mise à jour automatique de l’heure), présenté de manière élégante sous forme de **widgets horloges** alignés ou en carrousel.

## Fonctionnalités principales

- Affichage de plusieurs horloges configurables (par fuseau horaire).
- Format 12h ou 24h selon préférence.
- Actualisation automatique en temps réel via JavaScript.
- Possibilité d’afficher le nom de la ville/pays associé sous chaque horloge.
- Intégration via un **shortcode** ou **widget** personnalisable.

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Gestion des fuseaux horaires et de l’heure d’été/hiver.  
    **Solution :** Utilisation d’une librairie fiable comme **moment-timezone** ou **day.js** avec base de données IANA pour une précision maximale.
- **Problème :** Affichage responsive sur différents écrans.  
    **Solution :** CSS flexible (grid/flex) permettant un rendu propre en ligne ou en colonne.

## Résultats / Impact

- Mise en valeur de la diversité culturelle et géographique de l’équipe.
- Outil utile pour mieux gérer les échanges entre collègues de différentes régions.
- Animation conviviale renforçant le sentiment d’appartenance à une entreprise internationale.

## Notes techniques / apprentissages

- Shortcode `[horloges_mondiales]` pour afficher le bloc où souhaité.
- Données configurables dans les options du plugin (liste des villes/fuseaux horaires).
- JavaScript gère l’actualisation en temps réel sans rechargement de page.
- Possibilité future : affichage analogique (style horloge classique) ou digital au choix.

## Tags

#Plugin #WordPress #PHP #JavaScript #Horloges #Diversité #portfolio #réalisations