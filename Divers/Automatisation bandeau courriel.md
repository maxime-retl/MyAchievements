# Automatisation Exchange — Bandeau festif dans les e-mails

**Type de projet :** Administration système (Exchange Online / Microsoft 365)
**Technologies :** Exchange Online, Microsoft 365 Admin Center, Transport Rules
**Date de réalisation :** 2024
**Client / Organisation :** Usage interne (Richard et Levesque)
**Lien Git / Démo :** _(N/A — administration Exchange)_

---

## Objectifs

- Ajouter automatiquement un **bandeau festif** dans les e-mails sortants durant la période des fêtes.
- Éviter les interventions manuelles de chaque utilisateur.
- Centraliser et automatiser la personnalisation des courriels via Exchange 365.

## Description

À l’occasion des fêtes, une règle a été configurée dans **Exchange Online (Office 365 Admin)** pour insérer automatiquement un bandeau dans les e-mails sortants.  
L’ajout s’effectue **au niveau serveur** par une **transport rule (règle de flux de messagerie)**, appliquée à l’ensemble des messages envoyés par le domaine.

Cela permet à toute l’organisation d’avoir une communication uniforme et professionnelle, sans nécessiter de configuration locale dans Outlook ou autre client de messagerie.

## Fonctionnalités principales

- Ajout automatique d’un bandeau graphique (image / HTML) dans tous les e-mails envoyés.
- Gestion centralisée via l’interface Exchange Admin Center (EAC).
- Application conditionnelle (période des fêtes uniquement).
- Uniformité et cohérence pour tous les utilisateurs, quelle que soit leur plateforme (Outlook, mobile, webmail).

## Screenshots / Visuels

_(À remplacer par de vraies captures d’écran si disponibles)_

## Difficultés rencontrées et solutions

- **Problème :** Compatibilité de l’image avec différents clients e-mail (Outlook, Gmail, mobiles).  
    **Solution :** Utilisation d’un code HTML simplifié et hébergement du bandeau sur un serveur accessible (HTTPS).
- **Problème :** Risque de perturber la signature e-mail existante des utilisateurs.  
    **Solution :** Positionnement du bandeau en haut du message, avant la signature personnelle.

## Résultats / Impact

- Communication festive homogène dans toute l’organisation.
- Réduction du temps de configuration par utilisateur (zéro action côté employés).
- Image professionnelle et cohérente de l’entreprise auprès des clients/partenaires.

## Notes techniques / apprentissages

- Mise en place via **Exchange Admin Center** → **Rules** → **Mail flow**.
- Utilisation des options _Apply disclaimer_ avec insertion d’un HTML contenant l’image.
- Possibilité de planifier la règle (activation/désactivation selon dates).
- Alternative : PowerShell (`New-TransportRule`) pour automatiser ou répliquer la règle.

## Tags

#Administration #Exchange365 #Office365 #Automatisation #Email #portfolio #réalisations