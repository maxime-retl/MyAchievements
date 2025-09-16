# SQLUserForge — Générateur d’utilisateurs SQL Server

**Type de projet :** Application desktop (outil interne)
**Technologies :** C#, WinForms, SQL Server (T-SQL, gestion des rôles)
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Simplifier la création d’utilisateurs SQL Server pour les administrateurs et développeurs.
- Éviter les erreurs manuelles liées aux scripts SQL répétés.
- Offrir une interface intuitive pour définir les rôles et permissions.

## Description

SQLUserForge est une petite application WinForms en C# qui permet de créer en quelques clics un nouvel utilisateur dans une base SQL Server.  
L’administrateur définit un nom d’utilisateur, un mot de passe et sélectionne les rôles prédéfinis (ex. lecture, écriture, admin partiel). L’application génère et exécute automatiquement le script SQL correspondant.

## Fonctionnalités principales

- Récupération des instances du poste sur lequel est exécuté l'application.
- Récupération des bases de données de l'instance sélectionnée.
- Création rapide d’un utilisateur SQL Server avec mot de passe.
- Sélection des rôles prédéfinis (lecture seule, lecture/écriture, custom, etc.).
- Génération automatique du script T-SQL et exécution sur la base.
- Affichage du script généré pour validation avant exécution.
- Interface minimaliste, adaptée aux administrateurs non experts SQL.

## Screenshots / Visuels

_(Remplacer les chemins par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Garantir la sécurité lors de la création d’utilisateurs (droits trop larges).  
    **Solution :** Définition de rôles prédéfinis sécurisés et limitation volontaire des choix pour éviter les abus.
- **Problème :** Compatibilité avec différentes versions de SQL Server.  
    **Solution :** Génération conditionnelle des scripts selon la version détectée (ex. `CREATE LOGIN` vs `CREATE USER`).

## Résultats / Impact

- Réduction du temps de création d’un compte SQL de plusieurs minutes à quelques secondes.
- Moins d’erreurs de syntaxe ou de configuration dans les rôles.
- Standardisation des droits utilisateurs à travers l’organisation.

## Notes techniques / apprentissages

- Utilisation de `SqlConnection` et `SqlCommand` pour exécuter les scripts générés.
- Paramétrage possible pour se connecter à différents serveurs / bases.
- Importance de la gestion des erreurs (utilisateur déjà existant, mot de passe non conforme aux règles de complexité).
- Application extensible : possibilité future de gérer la suppression, modification ou audit des utilisateurs.

## Tags

#Application #WinForms #csharp #SQLServer #Sécurité #Automatisation #portfolio #réalisations