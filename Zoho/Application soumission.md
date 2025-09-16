# Application Zoho Creator — Gestion des soumissions

**Type de projet :** Application Zoho Creator (low-code)
**Technologies :** Zoho Creator, Deluge (scripting), Excel import, Zoho CRM intégration
**Date de réalisation :** 2025 (en cours de développement)
**Client / Organisation :** Richard et Levesque — Estimation / Soumission
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Mettre en place un système complet de **gestion des soumissions**.
- Automatiser le processus depuis **Cabinet Vision** jusqu’à la génération du prix final.
- Intégrer la gestion des **escomptes, taxes et particularités régionales** (Québec, Ontario).
- Centraliser toutes les soumissions dans un seul outil relié à Zoho.

## Description

Ce projet ambitieux repose sur une application développée dans **Zoho Creator**.  
Le flux principal :

1. **Export Excel d’un projet Cabinet Vision**.
2. **Importation dans l’app Zoho Creator**.
3. **Extraction et classification** des données (matériaux, dimensions, catégories).
4. **Génération automatique d’un prix estimatif** pour chaque ligne et pour le projet complet.
5. Application des **escomptes, règles de taxes et paramètres régionaux**.
6. Production d’une soumission claire et structurée, prête à être envoyée au client. _(en cours)_

## Fonctionnalités principales

- Importation d’un fichier Excel généré par Cabinet Vision.
- Parsing et stockage des données dans des tables Zoho Creator.
- Classification automatique des matériaux.
- Calcul des coûts et génération du prix final.
- Modules complémentaires :
    - Gestion des **escomptes**.
    - Gestion des **taxes** selon la province (QC / ON).
    - Ajustements manuels possibles par les estimateurs.
- Génération de la soumission finale (PDF / envoi par e-mail).

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Structurer correctement les données exportées de Cabinet Vision (Excel complexe).  
    **Solution :** Développement d’un parseur Deluge pour classer et nettoyer les données dès l’import.
- **Problème :** Gestion des différences de taxes entre provinces.  
    **Solution :** Ajout de règles conditionnelles selon QC/ONT avec champs configurables.
- **Problème :** Garantir la flexibilité des estimateurs (modifications manuelles).  
    **Solution :** Interface permettant de surcharger les prix ou escomptes avant génération de la soumission finale.

## Résultats / Impact attendus

- Réduction considérable du temps de création d’une soumission (de plusieurs heures à quelques minutes).
- Standardisation des calculs et des prix → moins d’erreurs humaines.
- Meilleure traçabilité et historique des soumissions.
- Intégration future possible avec Zoho CRM pour rattacher les soumissions aux projets/clients.

## Notes techniques / apprentissages

- Usage intensif de **Deluge Script** pour l’import, le parsing et les calculs.
- Exploitation des fonctions Zoho Creator pour créer plusieurs **blocs modulaires** (taxes, escomptes, ajustements).
- Test et validation avec des fichiers Excel réels exportés de Cabinet Vision.
- Application encore en **phase de développement** → évolutive vers un module complet d’estimation intégré au CRM.

## Tags

#ZohoCreator #Deluge #CabinetVision #Excel #Soumission #Estimation #portfolio #réalisations