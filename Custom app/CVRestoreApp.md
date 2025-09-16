# CVRestoreApp — Automatisation du processus de restauration Cabinet Vision

**Type de projet :** Application desktop (outil interne)
**Technologies :** C#, WinForms, Process API, Registry, FileSystem
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Simplifier le processus de restauration des paramètres Cabinet Vision pour les utilisateurs non techniques.
- Éviter les erreurs manuelles dans la manipulation des fichiers de sauvegarde.
- Automatiser les actions répétitives afin de gagner du temps.

## Description

CVRestoreApp est une application WinForms développée en C# pour automatiser l’ensemble du processus de restauration de Cabinet Vision.  
Sans l’application, un utilisateur devait :

1. Copier manuellement le dossier **backup** depuis le serveur.
2. Le coller dans le dossier **Automatic Backups** en local.
3. Lancer **CVRestore**.
4. Valider la mise à jour de la base de données.

L’application prend en charge ces étapes de manière automatique et transparente.

## Fonctionnalités principales

- **Copie automatique** du dossier de sauvegarde le plus récent depuis le serveur vers le dossier local.
- **Copie automatique** du fichier `.reg` le plus récent contenant les paramètres.
- **Importation automatique** du fichier `.reg` dans le registre Windows.
- **Lancement automatique** de CVRestore pour mettre à jour la base de données.
- **Nettoyage automatique** des anciens backups pour libérer de l’espace disque (ne conserve que les 5 plus récents).

## Screenshots / Visuels

_(Remplacer les chemins par les captures d’écran réelles)_

## Difficultés rencontrées et solutions

- **Problème :** Identifier le bon backup et le bon fichier `.reg` les plus récents.  
    **Solution :** Utilisation des métadonnées de fichiers (dates de création/modification) pour sélectionner automatiquement le plus récent.
- **Problème :** Risque de surcharge disque par accumulation de backups.  
    **Solution :** Routine de nettoyage intégrée conservant uniquement les 5 derniers dossiers de sauvegarde et le dernier `.reg`.
- **Problème :** Automatisation de l’importation du registre pouvant demander des privilèges.  
    **Solution :** Utilisation de `reg import` avec élévation de privilèges si nécessaire et messages clairs à l’utilisateur.

## Résultats / Impact

- Temps de restauration réduit de plusieurs minutes à quelques secondes.
- Réduction des erreurs humaines (fichiers oubliés, mauvaise version de backup).
- Permet aux utilisateurs disposant d’une licence **Cabinet Vision Designer** d’avoir toujours les paramètres les plus récents.
- Amélioration de la fluidité et de la fiabilité dans les processus internes.

## Notes techniques / apprentissages

- Automatisation via **Process.Start** pour lancer CVRestore et importer le fichier `.reg`.
- Gestion de fichiers : recherche, copie, suppression sécurisée via `System.IO`.
- Utilisation de `try/catch` robustes pour informer l’utilisateur en cas d’échec.
- Interface simple et conviviale avec logs de progression et messages d’état.

## Tags

#Application #WinForms #C# #CabinetVision #Automatisation #portfolio #réalisations