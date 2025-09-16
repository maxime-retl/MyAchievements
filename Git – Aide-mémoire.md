# 🐙 Git – Aide-mémoire

---

## ⚙️ Initialisation & configuration

| Description | Commande |
|-------------|----------|
| Initialiser un nouveau dépôt Git local | `git init` |
| Vérifier l’état des fichiers suivis / modifiés | `git status` |
| Configurer votre nom (une seule fois) | `git config --global user.name "Votre Nom"` |
| Configurer votre email (une seule fois) | `git config --global user.email "votre.email@exemple.com"` |
| Vérifier la configuration actuelle | `git config --list` |

---

## ⬇️ Cloner & récupérer un dépôt

| Description | Commande |
|-------------|----------|
| Cloner un dépôt distant (ex. GitHub) | `git clone https://github.com/organisation/nom-du-repo.git` |
| Récupérer les dernières modifications distantes | `git pull origin branche` |

---

## 🌱 Gestion des branches

| Description | Commande |
|-------------|----------|
| Lister les branches disponibles | `git branch` |
| Créer une nouvelle branche et se déplacer dessus | `git checkout -b nom-de-branche` |
| Changer de branche existante | `git checkout nom-de-branche` |
| Fusionner une branche dans la branche actuelle | `git merge nom-de-branche` |

---

## 💾 Sauvegarder & envoyer vos modifications

| Description | Commande |
|-------------|----------|
| Ajouter tous les fichiers modifiés à l’index | `git add .` |
| Ajouter un fichier précis | `git add chemin/vers/fichier` |
| Enregistrer un commit avec un message | `git commit -m "Message clair décrivant la modification"` |
| Envoyer vos modifications sur le dépôt distant | `git push origin nom-de-branche` |

---

## 📜 Historique & suivi

| Description | Commande |
|-------------|----------|
| Voir l’historique des commits | `git log` |
| Voir l’historique condensé (graphique simplifié) | `git log --oneline --graph --all` |
| Voir les différences entre fichiers modifiés et version suivie | `git diff` |

---

## 🛠️ Commandes utiles

| Description | Commande |
|-------------|----------|
| Supprimer une branche locale | `git branch -d nom-de-branche` |
| Supprimer une branche distante | `git push origin --delete nom-de-branche` |
| Annuler un fichier modifié (retour version suivie) | `git checkout -- chemin/vers/fichier` |
| Mettre de côté des changements sans commit (stash) | `git stash` |
| Restaurer les changements mis en stash | `git stash pop` |

---

## 🔑 Gestion de plusieurs comptes GitHub / alias SSH

### 1️⃣ Générer une clé SSH
```bash
ssh-keygen -t ed25519 -C "votre.email@exemple.com"
# puis donner un nom de fichier, par ex :
# ~/.ssh/id_ed25519_github_pro
# ~/.ssh/id_ed25519_github_perso
```

### 2️⃣ Ajouter les clés à l’agent SSH
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519_github_pro
ssh-add ~/.ssh/id_ed25519_github_perso
```

### 3️⃣ Créer le fichier de configuration SSH
Éditer `~/.ssh/config` et ajouter :
```txt
# Compte pro
Host github-pro
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_github_pro

# Compte perso
Host github-perso
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_github_perso
```

### 4️⃣ Tester la connexion
```bash
ssh -T git@github-pro
ssh -T git@github-perso
```

### 5️⃣ Utiliser les alias dans Git
| Description | Commande |
|-------------|----------|
| Associer un dépôt à l’alias pro | `git remote set-url origin git@github-pro:Organisation/Repo.git` |
| Associer un dépôt à l’alias perso | `git remote set-url origin git@github-perso:plumedours/Repo.git` |
| Pousser sur le dépôt via l’alias choisi | `git push origin main` |

---

📌 **Tips :**
- Chaque clé est associée à un compte GitHub (perso/pro).
- L’alias défini dans `~/.ssh/config` (`github-pro`, `github-perso`) doit être utilisé dans l’URL du dépôt.