# CV Report — Générateur de rapports pour licences Designer Cabinet Vision

**Type de projet :** Application desktop (outil interne)
**Technologies :** C#, WinForms, SQL Server (connexion distante), iTextSharp / PdfSharp (export PDF), API d'impression Windows
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Contourner la limitation de licence « Designer » de Cabinet Vision qui empêche l’accès natif aux rapports.
- Reproduire les rapports essentiels (ex. Sommaire des achats) en se connectant directement à la base SQL et en présentant les données dans une interface simple.
- Permettre l’export en PDF et l’impression directe depuis l’application.

## Description

CV Report est une application WinForms en C# conçue pour récupérer en arrière-plan les données nécessaires depuis le serveur SQL de l’utilisateur et reconstruire les rapports habituellement générés par Cabinet Vision. L’outil offre une interface épurée permettant d’afficher un aperçu du rapport, puis d’exporter en PDF ou d’imprimer directement.

## Fonctionnalités principales

- Connexion sécurisée au serveur SQL distant pour extraire les données sources des rapports.
- Reproduction des rapports standards (ex. Sommaire des achats) avec mise en forme proche de l’original.
- Sommaire par cabinet avec liste des matériaux pour chaque cabinet d'un projet.
- Aperçu intégré du rapport avant export/impression.
- Export au format PDF.
- Impression directe via la file d’impression Windows.

## Screenshots / Visuels

_(Remplacer les chemins par les captures d’écran réelles)_

## Difficultés rencontrées et solutions

- **Problème :** Accès aux données sur un serveur SQL distant avec des contraintes réseau (VPN, pare-feu).  
    **Solution :** Connexions paramétrables (string de connexion), tests de connectivité, et documentation des ports/accès nécessaires ; possibilité d’utiliser un compte dédié avec droits en lecture seule.
- **Problème :** Reproduire fidèlement le format des rapports CV sans utiliser les outils internes.  
    **Solution :** Analyse du schéma de la base et des calculs utilisés par CV, création d’un moteur de rendu HTML → PDF permettant une mise en page flexible (tables, totaux, en-têtes/ pieds de page).
- **Problème :** Gestion des impressions (marges, orientation, imprimantes réseau).  
    **Solution :** Intégration des options d’impression Windows standards et aperçu avant impression pour ajuster les paramètres.

## Résultats / Impact

- Les utilisateurs avec licence Designer peuvent désormais obtenir les rapports nécessaires sans changer de licence.
- Réduction des demandes d’assistance liées à l’impossibilité d’accéder aux rapports.
- Production de rapports exportables et imprimables, facilitant la distribution et l’archivage.

## Notes techniques / apprentissages

- Connexion SQL via `SqlConnection` avec requêtes paramétrées pour éviter les injections.
- Impression : utilisation de `PrintDocument` et des dialogues Windows pour la sélection d’imprimante et les options papier.

## Prochaines améliorations possibles

- Liste des matériaux pour faciliter l'estimation avant soumission (en cours).   

## Tags

#Application #WinForms #csharp #SQLServer #PDF #Impression #CabinetVision #portfolio #réalisations