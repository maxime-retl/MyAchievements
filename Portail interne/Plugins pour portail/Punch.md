# Plugin WordPress — Punch in/out (suivi des heures)

**Type de projet :** Plugin WordPress personnalisé
**Technologies :** WordPress, PHP, MySQL, ACF, JavaScript (AJAX), HTML/CSS
**Date de réalisation :** 2024–2025
**Client / Organisation :** Usage interne (Richard et Levesque — Portail interne)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Permettre aux employés de bureau de **puncher leur arrivée et leur départ** directement depuis le portail interne.
- Offrir un suivi transparent et centralisé des heures travaillées.
- Donner aux gestionnaires une interface claire pour consulter, modifier et valider les entrées.

## Description

Ce plugin WordPress constitue une **solution complète de suivi du temps** intégrée au portail interne.  
Il permet aux employés de **puncher** leur entrée/sortie de travail, de voir leur historique et leur total d’heures, tandis que les administrateurs disposent d’un tableau de bord pour gérer et contrôler les données.

Le système s’appuie sur une **table MySQL personnalisée** afin d’assurer un stockage structuré et performant.

## Fonctionnalités principales

- **Côté employé**
    - Punch in/out (arrivée/départ) via un bouton dédié.
    - Vue en tableau de ses punchs (date, in/out, télétravail, pause dîner, jour férié, commentaire).
    - Vue hebdomadaire avec totaux arrondis et réels.
    - Support du multi-punch par jour (plusieurs entrées/sorties cumulées).
- **Côté admin**
    - Tableau complet de tous les employés avec filtres par semaine/employé.
    - Possibilité de modifier ou supprimer chaque entrée (date, heure, type, télétravail, férié, commentaire).
    - Calcul automatique des heures, avec possibilité de forcer un total via `override_total_seconds`.
    - Mise en évidence visuelle des journées corrigées (ex. fond rouge).
    - Totaux semaine arrondis et réels affichés dans le tableau.
- **Techniques de gestion**
    - Totaux calculés côté serveur pour éviter les incohérences JavaScript.
    - Shortcodes pour afficher punch et tableau côté employé.
    - AJAX pour rafraîchissement fluide sans rechargement de page.

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Gestion de plusieurs punchs dans une même journée.  
    **Solution :** Repenser la structure SQL et l’affichage pour gérer des paires multiples punch in/out cumulées.
- **Problème :** Différence entre heures réelles et heures arrondies.  
    **Solution :** Double calcul côté serveur (arrondi et réel) avec affichage comparatif.
- **Problème :** Besoin de corrections manuelles par les admins.  
    **Solution :** Ajout du champ `override_total_seconds` pour remplacer le total automatique d’une journée.

## Résultats / Impact

- Outil simple et intégré permettant aux employés de bureau de gérer leur présence sans matériel dédié.
- Transparence accrue dans le suivi des heures.
- Gain de temps pour les gestionnaires (moins de calculs manuels et de suivis Excel).
- Base solide extensible pour d’autres usages RH (vacances, absences).

## Notes techniques / apprentissages

- Table SQL personnalisée pour stocker les punchs.
- Fonctions `get_user_punches` et `get_admin_punches` optimisées pour retourner directement les totaux serveur.
- Shortcodes pour intégration flexible dans le portail (formulaire + tableau).
- Distinction claire côté code entre heures arrondies et heures réelles.
- Extensible : ajout futur de graphiques, rapports PDF ou export Excel.

## Tags

#Plugin #WordPress #PHP #MySQL #Punch #TempsDeTravail #Automatisation #portfolio #réalisations