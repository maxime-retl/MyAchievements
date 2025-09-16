# ZohoApp — Intégration Zoho CRM ↔ Cabinet Vision

**Type de projet :** Application desktop (outil interne)
**Technologies :** C#, WinForms, Zoho CRM API, XML (ordx), FileSystem  
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(à remplir si disponible)_
**Documentation interne :** [KB — Utilisation de ZohoApp pour générer un fichier Cabinet Vision prérempli](https://portail-interne.richardetlevesque.com/kb/utilisation-de-zohoapp-pour-generer-un-fichier-cabinet-vision-prerempli/)

---

## Objectifs

- Automatiser le transfert des informations clients/projets depuis Zoho CRM vers Cabinet Vision.
- Éviter la double saisie manuelle des données entre les systèmes.
- Accélérer la création de projets Cabinet Vision avec un fichier prérempli prêt à l’emploi.

## Description

ZohoApp est une application WinForms développée en C# qui sert de **pont entre Zoho CRM et Cabinet Vision**.  
L’utilisateur sélectionne un projet dans Zoho CRM, et l’application :

1. **Récupère les données client et contact** associées au projet via l’API Zoho CRM.
2. **Génère un fichier `.ordx`** prérempli avec ces informations pour Cabinet Vision.
3. **Crée automatiquement le dossier du projet** sur le serveur, correctement nommé et structuré, prêt à être utilisé.

Cette automatisation réduit fortement les erreurs humaines et standardise la structure des projets.

## Fonctionnalités principales

- Connexion directe à l’API Zoho CRM pour extraire les données clients et projets.
- Génération automatique d’un fichier `.ordx` avec insertion dynamique des informations (nom client, adresse, contact, etc.).
- Création automatique du dossier projet avec la bonne nomenclature.
- Interface conviviale et simple (sélection d’un projet → génération instantanée).

## Screenshots / Visuels

_(Remplacer les chemins par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Intégration avec l’API Zoho CRM nécessitant authentification OAuth et gestion des tokens.  
    **Solution :** Mise en place d’un module de gestion des tokens avec rafraîchissement automatique, et stockage sécurisé des identifiants.
- **Problème :** Génération dynamique du fichier `.ordx` en respectant le schéma XML attendu par Cabinet Vision.  
    **Solution :** Analyse du fichier modèle, parsing XML et injection des données de Zoho CRM dans les bons nœuds.
- **Problème :** Uniformité dans la création des dossiers projets.  
    **Solution :** Standardisation des noms de dossiers (ex. `CODECLIENT-PROJET`) et vérification avant création pour éviter les doublons.

## Résultats / Impact

- Gain de temps significatif dans la création de projets Cabinet Vision.
- Élimination de la double saisie manuelle entre Zoho CRM et Cabinet Vision.
- Réduction des erreurs dans les informations clients/projets.
- Processus plus fluide et standardisé pour tous les utilisateurs.

## Notes techniques / apprentissages

- Connexion API Zoho via requêtes HTTPS + JSON, parsing avec `Newtonsoft.Json`.
- Génération XML via `System.Xml` pour modifier le modèle `.ordx`.
- Utilisation du FileSystem C# pour la création automatique de dossiers et fichiers.
- Importance d’une bonne gestion des erreurs réseau (perte connexion Zoho) et de la validation des données avant insertion.

## Tags

#Application #WinForms #csharp #ZohoCRM #CabinetVision #Automatisation #portfolio #réalisations