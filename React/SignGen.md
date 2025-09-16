# SignGen — Générateur de signatures Outlook

**Type de projet :** Application web (React)
**Technologies :** React, TypeScript, TailwindCSS, Formik/Yup (formulaires), HTML/CSS
**Date de réalisation :** 2025
**Client / Organisation :** Richard et Levesque — Outil interne
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Simplifier la création d’une **signature uniforme** pour les employés.
- Éviter les erreurs ou variations manuelles lors de la mise en place des signatures Outlook.
- Offrir un outil simple et rapide, utilisable par tous les employés.

## Description

**SignGen** est une application React qui permet aux employés de saisir leurs informations personnelles (nom, prénom, poste, courriel, téléphone, etc.).  
L’outil génère automatiquement une **signature HTML normalisée** conforme à la charte graphique de l’entreprise.

L’utilisateur n’a plus qu’à **copier/coller** la signature dans Outlook (ou tout autre client de messagerie).

## Fonctionnalités principales

- Formulaire de saisie : prénom, nom, fonction, courriel, téléphone, etc.
- Validation des champs (ex. adresse courriel correcte).
- Génération instantanée d’un bloc HTML mis en forme selon la charte graphique R&L.
- Option de prévisualisation pour voir le rendu final avant copie.

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Compatibilité du rendu HTML entre différents clients mail (Outlook, Gmail, mobile).  
    **Solution :** Simplification du HTML et usage de styles inline pour une compatibilité maximale.
- **Problème :** S’assurer que tous les employés utilisent bien le modèle.  
    **Solution :** Automatisation + standardisation via l’outil (pas de personnalisation libre).

## Résultats / Impact

- Uniformité des signatures dans l’entreprise.
- Gain de temps pour les employés et le support informatique.
- Image plus professionnelle et cohérente auprès des clients/partenaires.

## Notes techniques / apprentissages

- Utilisation de **React** pour l’interface et la logique.
- Génération de HTML inline stylisé pour compatibilité Outlook.

## Tags

#React #TypeScript #TailwindCSS #Outlook #Signature #Automatisation #portfolio #réalisations