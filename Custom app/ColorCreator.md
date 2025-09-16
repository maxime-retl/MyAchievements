# ColorCreator — Automatisation de création de couleurs dans Cabinet Vision

**Type de projet :** Application desktop (outil interne)
**Technologies :** C#, WinForms, SQL Server (Cabinet Vision DB)
**Date de réalisation :** 2024
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Faciliter et automatiser la création de nouvelles couleurs dans Cabinet Vision.
- Réduire les manipulations manuelles répétitives dans la base de données.
- Permettre la modification rapide des finitions existantes.

## Description

ColorCreator est une application WinForms développée en C# qui interagit directement avec la base SQL de Cabinet Vision.  
Son rôle est de créer une nouvelle **finition** et d’automatiser toutes les étapes nécessaires dans la base :

1. Création d’une **finition**.
2. Création d’un **matériau** portant le même nom que la finition.
3. Mise à jour du script **UCS** (User Created Standards) pour inclure cette nouvelle création.

En plus de l’ajout, l’application permet également de **modifier des finitions existantes** de manière simple et rapide.

## Fonctionnalités principales

- Création automatique d’une finition dans Cabinet Vision.
- Génération d’un matériau associé portant le même nom.
- Mise à jour automatique de l’UCS pour intégrer la nouvelle donnée.
- Édition et modification des finitions existantes.
- Interface simple et intuitive, adaptée aux utilisateurs non techniques.

## Screenshots / Visuels

_(Remplacer les chemins par les captures d’écran réelles)_

## Difficultés rencontrées et solutions

- **Problème :** Manipuler directement les tables SQL de Cabinet Vision sans documentation officielle pouvait provoquer des erreurs d’intégrité.  
    **Solution :** Analyse des schémas de base, test sur base de développement, mise en place d’une transaction SQL sécurisée regroupant toutes les étapes (finition, matériau, UCS) pour éviter tout état incohérent.
- **Problème :** Assurer la cohérence entre le nom de la finition et celui du matériau.  
    **Solution :** Synchronisation automatique du champ lors de l’insertion et contrôle de doublons avant validation.

## Résultats / Impact

- Gain de temps considérable pour l’équipe de production lors de l’ajout de nouvelles couleurs.
- Réduction des erreurs humaines liées à des oublis ou incohérences dans les données.
- Amélioration de la flexibilité et de la rapidité pour répondre aux demandes clients de personnalisation.

## Notes techniques / apprentissages

- Connexion SQL via `SqlConnection` et exécution des requêtes paramétrées.
- Usage de transactions (`BEGIN TRANSACTION`, `COMMIT`, `ROLLBACK`) pour garantir la cohérence des données.
- Possibilité d’intégrer des validations supplémentaires (par ex. champ couleur hexadécimal).

## Tags

#Application #WinForms #csharp #SQLServer #CabinetVision #portfolio #réalisations