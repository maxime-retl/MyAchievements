# Suivi heures — Visualisation des temps de punch

**Type de projet :** Application desktop (outil interne)
**Technologies :** C#, WinForms, SQL Server (base Punch), Calendar Control
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Permettre aux employés de consulter facilement leurs heures de travail enregistrées par le système de punch.
- Offrir une interface claire et moderne avec double vue (liste + calendrier).
- Donner un accès sécurisé via l’authentification par identifiant et mot de passe Punch.

## Description

Suivi heures est une application WinForms développée en C# qui se connecte directement à la base de données du système Punch.  
L’utilisateur s’authentifie avec son **ID Punch** et son **mot de passe**, puis accède à ses données de pointage (punch in/out).  
Les informations sont présentées sous deux formes :

- **Vue en liste** : détail des journées avec punch in / out et total quotidien.
- **Vue en calendrier** : visualisation graphique des jours travaillés et heures enregistrées.

## Fonctionnalités principales

- Connexion sécurisée à la base SQL du Punch.
- Authentification par identifiant + mot de passe.
- Liste chronologique des punchs in/out.
- Vue calendrier interactive pour repérer rapidement les jours travaillés.
- Totaux journaliers affichés.
- Export simple des données (CSV / Excel) _(optionnel si déjà présent)_.

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Assurer la sécurité de la connexion et des identifiants.  
    **Solution :** Utilisation de requêtes paramétrées SQL (`SqlParameter`) et chiffrement des identifiants côté application.
- **Problème :** Représentation claire des heures sur un calendrier.  
    **Solution :** Utilisation du `MonthCalendar` / contrôle calendrier WinForms enrichi avec des couleurs et bulles d’infos pour montrer les punchs.
- **Problème :** Performances lors du chargement de grandes périodes.  
    **Solution :** Chargement paginé / filtré (ex. mois par mois) et cache local en mémoire.

## Résultats / Impact

- Mise à disposition des employés d’un outil simple et autonome pour consulter leurs heures.
- Réduction des demandes auprès des RH/gestionnaires pour connaître ses heures.
- Amélioration de la transparence et du suivi individuel.

## Notes techniques / apprentissages

- Connexion SQL avec `SqlConnection` et authentification utilisateur via table `Employees`.
- Utilisation de `ListView` pour la vue détaillée et d’un `Calendar Control` personnalisé pour la vue calendrier.
- Importance d’un design simple et responsive pour une adoption rapide par les employés.
- Extensible vers une version web ou mobile pour accès externe.

## Tags

#Application #WinForms #csharp #SQLServer #Punch #TempsDeTravail #portfolio #réalisations