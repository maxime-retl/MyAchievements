# ExportParamCV — Export automatisé des paramètres Cabinet Vision

**Type de projet :** Application desktop (outil interne)
**Technologies :** C#, WinForms, Registry API, FileSystem
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Faciliter l’exportation de la clé de registre contenant les paramètres critiques de Cabinet Vision.
- Standardiser le nommage des fichiers exportés pour les rendre facilement identifiables.
- Centraliser la configuration en utilisant la base de référence de Simon.

## Description

ExportParamCV est une application WinForms développée en C# qui automatise l’export de la clé de registre Windows contenant les **paramètres importants de Cabinet Vision**.  
Le fichier généré est automatiquement renommé afin d’être clair et immédiatement reconnaissable (par exemple incluant la date, l’utilisateur ou un label spécifique).

La clé de registre exportée provient principalement de la base maintenue par Simon, considéré comme le **"master"** au niveau des paramètres. L’outil assure ainsi une cohérence des configurations entre les postes.

## Fonctionnalités principales

- Export automatique de la clé de registre Cabinet Vision.
- Nommage normalisé des fichiers `.reg` pour faciliter leur identification.
- Utilisation de la base de référence (Simon) comme source principale.
- Interface simple et exécutable en un clic.

## Screenshots / Visuels

_(Remplacer les chemins par les captures d’écran réelles)_

## Difficultés rencontrées et solutions

- **Problème :** Risque d’exporter une mauvaise clé ou de générer des fichiers non standardisés.  
    **Solution :** Définition claire du chemin de la clé de registre à exporter et génération automatique du nom de fichier.
- **Problème :** Gestion des droits nécessaires pour accéder et exporter la clé de registre.  
    **Solution :** Exécution avec élévation de privilèges (UAC) si requis, et messages clairs en cas d’échec.

## Résultats / Impact

- Processus d’export rendu plus rapide, fiable et reproductible.
- Suppression des erreurs humaines liées à des exports manuels mal réalisés ou mal nommés.
- Mise en place d’une **méthode standardisée** pour partager les paramètres Cabinet Vision entre les postes.

## Notes techniques / apprentissages

- Utilisation de `reg export` via **Process.Start** pour générer le fichier `.reg`.
- Génération dynamique du nom de fichier (date + identifiant) pour éviter les doublons.
- Application conçue pour être complémentaire avec **CVRestoreApp** et **ColorCreator** dans la gestion des paramètres Cabinet Vision.

## Tags

#Application #WinForms #C# #CabinetVision #Automatisation #Registry #portfolio #réalisations