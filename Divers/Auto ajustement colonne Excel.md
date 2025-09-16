# Script Excel — Automatisation de mise en page pour rapports Zoho

**Type de projet :** Script VBA intégré à Excel
**Technologies :** VBA, Microsoft Excel
**Date de réalisation :** 2025
**Client / Organisation :** Usage interne (Richard et Levesque — demande de Ian & Jennyfer)
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Rendre lisibles et exploitables les rapports exportés depuis Zoho au format Excel.
- Réduire le temps passé à manipuler manuellement les colonnes et la mise en page.
- Permettre une impression rapide et standardisée des rapports.

## Description

Un rapport exporté depuis Zoho au format Excel nécessitait de nombreuses manipulations manuelles pour être utilisable :  
redimensionnement des colonnes, alignements, en-têtes, marges, etc.

Pour répondre à cette problématique, un script **VBA** a été intégré directement dans le fichier Excel.  
Un simple **bouton dans le ruban** permet :

1. D’automatiser la mise en page (taille des colonnes, alignement, entêtes, orientation).
2. De lancer immédiatement l’**aperçu avant impression**.

L’outil est donc utilisable par tous sans connaissances techniques.

## Fonctionnalités principales

- Redimensionnement automatique des colonnes selon le contenu.
- Alignement des cellules pour une meilleure lisibilité.
- Mise en page adaptée pour l’impression (orientation paysage, marges, zones d’impression).
- Ajout d’en-têtes / pieds de page si nécessaire.
- Bouton intégré dans Excel pour lancer la macro en un clic.
- Ouverture automatique de l’aperçu avant impression.

## Screenshots / Visuels

_(À remplacer par des captures d’écran réelles)_

## Difficultés rencontrées et solutions

- **Problème :** Rapports exportés depuis Zoho peu standardisés selon les colonnes et longueurs de texte.  
    **Solution :** Utilisation de `AutoFit` pour les colonnes et adaptation conditionnelle pour les colonnes critiques.
- **Problème :** Variabilité du nombre de colonnes entre les rapports.  
    **Solution :** Script générique qui détecte automatiquement la dernière colonne/ligne utilisées (`UsedRange`).

## Résultats / Impact

- Gain de temps significatif pour Ian et Jennyfer (et autres utilisateurs).
- Standardisation de la mise en page des rapports imprimés.
- Réduction des erreurs ou oublis liés à une préparation manuelle répétitive.

## Notes techniques / apprentissages

- Script écrit en **VBA**, stocké dans le module du classeur.
- Appelé via un **bouton personnalisé** dans la barre d’outils Excel.
- Exploitation de `UsedRange`, `AutoFit`, `PageSetup` et `PrintPreview`.
## Tags

#Script #Excel #VBA #Automatisation #Zoho #portfolio #réalisations