# CheckRDP

**Type de projet :** Application desktop (outil interne)  
**Technologies :** C#, WinForms, APIs Windows (WTS / WMI), threading asynchrone  
**Date de réalisation :** 2025  
**Client / Organisation :** Usage interne (Richard et Levesque)  
**Lien Git / Démo :** _(à remplir si disponible)_

---

## Objectifs

- Permettre aux collaborateurs de savoir rapidement si un poste distant est déjà utilisé avant d’établir une connexion RDP.
- Éviter les déconnexions inopinées d'un utilisateur lorsqu'une autre personne tente de se connecter.
- Offrir un outil simple, portable et rapide à lancer depuis un poste de travail.

## Description

CheckRDP est une petite application WinForms développée en C# qui « scanne » un poste Windows distant et retourne l’état de session(s) utilisateur (libre / utilisé). L’interface est volontairement minimale : on saisit le nom ou l’IP du poste, on clique sur **Scanner**, et l’application affiche si quelqu’un est connecté, qui est connecté (nom d’utilisateur / session) et d’éventuelles informations complémentaires (type de session, heure de connexion).

## Fonctionnalités principales

- Scan d’un poste distant par nom d’hôte ou adresse IP.
- Détection des sessions actives (utilisateur connecté, type de session — console / RDP —, heure de connexion).
- Affichage clair (OK / Occupé) + nom d’utilisateur quand disponible.
- Historique/log local des dernières vérifications.
- Option de rafraîchissement automatique / scan périodique (configurable).
- Copier les résultats dans le presse-papier / export CSV simple.
- Gestion des erreurs réseau et messages d’explication (pare-feu, permissions).

## Screenshots / Visuels

_(Remplacer les chemins par les images du projet)_

## Difficultés rencontrées et solutions

- **Problème :** Obtenir l’état de session d’un poste distant de façon fiable et sans provoquer d’actions sur la session (ne pas déconnecter).  
    **Solution :** Utilisation des API Terminal Services (WTS) et de requêtes WMI en lecture seule pour interroger les sessions existantes (WTSEnumerateSessions / WTSQuerySessionInformation). Ces appels permettent de récupérer l’utilisateur connecté et le type de session sans affecter la session elle-même.
- **Problème :** Restrictions côté cible (pare-feu, RPC/WMI désactivé, droits insuffisants).  
    **Solution :** Ajout d’un message d’erreur explicite et de diagnostics : test de connectivité (ping / port 3389), tentative WMI en fallback, et documentation indiquant les ports/services à autoriser. L’outil peut être exécuté avec un compte de service disposant des droits nécessaires si requis.
- **Problème :** Interface bloquante lors de scans réseau lents.  
    **Solution :** Exécution des scans en tâche asynchrone (Task / BackgroundWorker) avec indicateur de progression et possibilité d’annuler.

## Résultats / Impact

- Réduction des déconnexions inattendues et du nombre d’appels au support pour causes de sessions RDP conflictuelles.
- Gain de temps pour les équipes en évitant d’ouvrir plusieurs sessions en même temps sur la même machine.
- Amélioration de la coordination entre les utilisateurs partageant des postes distants.

## Notes techniques / apprentissages

- Implémentation UI : WinForms simple, boutons clairs, couleur verte/rouge pour l’état, logs visibles dans un panel inférieur.

## Prochaines améliorations possibles

- Création des IP à contrôler : fichier local de liste des IP (CSV ou json ou autre) pour gérer facilement la liste plutôt qu'en dur dans le code.
- Internationalisation possible (FR/EN) si l’outil est partagé hors équipe.

## Tags

#Application #WinForms #csharp #RDP #OutilInterne #portfolio #réalisations