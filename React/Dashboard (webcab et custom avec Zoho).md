# Dashboard React — WebCab & RL Flow Track (Zoho)

**Type de projet :** Application web (React)
**Technologies :** React, TailwindCSS, React Router
**Date de réalisation :** 2025
**Client / Organisation :** Richard et Levesque — Portail interne
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Fournir un **point d’entrée unique** pour consulter différents dashboards internes.
- Permettre aux utilisateurs de **switcher facilement** entre deux environnements :
    - Dashboard **WebCab**
    - Dashboard [[App FlowTrack (pour l'usine)]] (Zoho)
- Centraliser la visualisation des données sans avoir à se connecter à plusieurs outils.

## Description

Ce projet React met en place carrousel des dashboards internes de R&L.  
L’application switch entre :

- **Dashboard WebCab** : indicateurs et rapports liés aux opérations.
- **Dashboard RL Flow Track (Zoho)** : suivi rendement de l'usine.

La navigation est fluide et l’UI est harmonisée grâce à un design moderne basé sur **TailwindCSS**.  
👉 Une note spécifique sur **RL Flow Track** détaille le fonctionnement de ce dashboard.

## Fonctionnalités principales

- Interface React moderne avec design responsive.
- Navigation entre plusieurs dashboards via React Router.
- Intégration du dashboard WebCab via API ou iframe selon les besoins.

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran)_

## Difficultés rencontrées et solutions

- **Problème :** Uniformiser deux dashboards issus de sources différentes (WebCab & Zoho).  
    **Solution :** Création d’une couche d’abstraction et d’une interface commune pour garder la même expérience utilisateur.
- **Problème :** Navigation fluide entre modules sans rechargement.  
    **Solution :** Utilisation de **React Router** avec lazy loading.

## Résultats / Impact

- Simplification de l’accès aux informations clés pour les employés.
- Gain de temps : un seul point d’entrée au lieu de deux applications séparées.
- Amélioration de l’adoption des outils internes grâce à une UI moderne et cohérente.

## Notes techniques / apprentissages

- Utilisation de **React** pour la robustesse et la maintenabilité.
- Styling avec **TailwindCSS** pour rapidité et uniformité.
- Extensible pour accueillir de futurs dashboards internes.

## Tags

#React #TypeScript #TailwindCSS #ZohoCRM #WebCab #Dashboard #portfolio #réalisations