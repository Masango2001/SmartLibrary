# Smart Library API

## 1. Présentation du projet

**Smart Library API** est une API REST de gestion d'une bibliothèque développée avec **Django REST Framework** et une base de données **SQLite**.

Ce projet a été réalisé dans le cadre d'un travail pratique sur la collaboration avec **Git et GitHub**. L'objectif principal est de mettre en place une organisation professionnelle de développement avec :

* Gestion de versions avec Git.
* Dépôt centralisé GitHub.
* Travail collaboratif avec des branches.
* Pull Requests et revue de code.
* Protection de la branche principale.
* Intégration Continue (CI) avec GitHub Actions.

---

# 2. Objectifs du projet

Les objectifs sont :

* Concevoir une API REST backend avec Django REST Framework.
* Appliquer une stratégie de gestion de branches.
* Utiliser GitHub comme plateforme collaborative.
* Automatiser la vérification du code avec GitHub Actions.
* Exécuter automatiquement les tests unitaires.
* Apprendre la résolution des conflits Git.
* Mettre en place un processus professionnel de validation du code.

---

# 3. Technologies utilisées

## Backend

* Python
* Django
* Django REST Framework

## Base de données

* SQLite

## Gestion de versions

* Git
* GitHub

## Qualité et automatisation

* GitHub Actions
* Ruff (analyse statique du code)
* Django Unit Tests

---

# 4. Fonctionnalités principales

## Gestion des utilisateurs

Fonctionnalités :

* Création de compte.
* Authentification.
* Gestion des utilisateurs.
* Gestion des permissions.

Application Django :

```
accounts
```

---

## Gestion des livres

Fonctionnalités :

* Ajouter un livre.
* Modifier un livre.
* Supprimer un livre.
* Consulter la liste des livres.

Application Django :

```
books
```

---

## Gestion des catégories

Fonctionnalités :

* Ajouter une catégorie.
* Modifier une catégorie.
* Supprimer une catégorie.
* Associer un livre à une catégorie.

Application Django :

```
categories
```

---

## Gestion des emprunts

Fonctionnalités :

* Emprunter un livre.
* Retourner un livre.
* Consulter l'historique des emprunts.

Application Django :

```
borrows
```

---

# 5. Architecture du projet

```
smart_library_api/

│
├── accounts/
│
├── books/
│
├── categories/
│
├── borrows/
│
├── config/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── manage.py
│
├── requirements.txt
│
├── README.md
│
├── LICENSE
│
└── .gitignore
```

---

# 6. Organisation Git et GitHub

Le projet utilise une organisation basée sur une branche principale protégée et une branche d'intégration.

Structure :

```
main 🔒
 |
develop
 |
 ├── feature/tests-ci
 ├── feature/accounts
 ├── feature/books
 ├── feature/borrows
 └── feature/categories
```

---

# 7. Rôle des branches

## main

La branche `main` représente la version stable du projet.

Règles :

* Aucun push direct autorisé.
* Fusion uniquement par Pull Request.
* Validation obligatoire avant fusion.

---

## develop

La branche `develop` est utilisée pour intégrer les différentes fonctionnalités développées par les membres.

Toutes les branches `feature/*` sont fusionnées vers `develop` après validation.

---

## Branches fonctionnalités

### feature/accounts

Responsable :

**Iteriteka Ange Chanciella**

Travail :

* Authentification.
* Gestion des comptes utilisateurs.

---

### feature/books

Responsable :

**Irishura Darlene**

Travail :

* CRUD des livres.
* Gestion des informations des livres.

---

### feature/borrows

Responsable :

**Akimana Nelly Franck**

Travail :

* Gestion des emprunts.
* Retour des livres.
* Historique.

---

### feature/categories

Responsable :

**Ezako Juste Ariel**

Travail :

* Gestion des catégories.
* Association avec les livres.

---

### feature/tests-ci

Responsable :

**Masango Alain Blaise**

Travail :

* Tests unitaires.
* Configuration GitHub Actions.
* Analyse qualité avec Ruff.
* Documentation du projet.

---

# 8. Workflow de collaboration

Chaque développeur suit le processus suivant :

## 1. Récupérer les dernières modifications

```bash
git checkout develop

git pull origin develop
```

---

## 2. Créer une branche fonctionnalité

Exemple :

```bash
git checkout -b feature/books
```

---

## 3. Développer la fonctionnalité

Ajouter les modifications :

```bash
git add .
```

Créer un commit :

```bash
git commit -m "Add book management feature"
```

---

## 4. Envoyer la branche

```bash
git push origin feature/books
```

---

## 5. Créer une Pull Request

La Pull Request suit le processus :

```
feature branch
        |
        ↓
Code Review
        |
        ↓
GitHub Actions CI
        |
        ↓
Merge vers develop
```

---

# 9. Protection de la branche main

La branche `main` est protégée avec les règles suivantes :

* Interdiction des push directs.
* Pull Request obligatoire.
* Validation par au moins un membre.
* Vérification automatique du pipeline CI avant fusion.

---

# 10. Pipeline CI avec GitHub Actions

Le fichier utilisé :

```
.github/workflows/ci.yml
```

Le pipeline se déclenche automatiquement lors de :

* Push.
* Pull Request.

Les étapes sont :

## Étape 1 : Installation

Installation des dépendances Python :

```bash
pip install -r requirements.txt
```

---

## Étape 2 : Analyse du code

Utilisation de Ruff :

```bash
ruff check .
```

Cette étape vérifie :

* erreurs de syntaxe.
* problèmes de qualité.
* mauvaises pratiques.

---

## Étape 3 : Tests unitaires

Exécution des tests Django :

```bash
python manage.py test
```

Si les tests échouent :

```
CI Failed
```

La Pull Request est bloquée.

Si les tests réussissent :

```
CI Passed
```

La fusion devient possible.

---

# 11. Installation du projet

## Cloner le dépôt

```bash
git clone URL_DU_DEPOT
```

---

## Créer l'environnement virtuel

```bash
python -m venv venv
```

---

## Activer l'environnement virtuel

Windows :

```bash
venv\Scripts\activate
```

Linux/Mac :

```bash
source venv/bin/activate
```

---

## Installer les dépendances

```bash
pip install -r requirements.txt
```

---

## Appliquer les migrations

```bash
python manage.py migrate
```

---

## Lancer le serveur

```bash
python manage.py runserver
```

---

# 12. Tests

Lancer les tests :

```bash
python manage.py test
```

Les tests permettent de vérifier :

* Authentification.
* Création des livres.
* Gestion des catégories.
* Gestion des emprunts.

---

# 13. Démonstration attendue

La démonstration finale montre :

1. Une Pull Request créée.
2. Une erreur volontaire dans le code.
3. L'échec du pipeline CI.
4. Le blocage automatique de la fusion.
5. La correction du problème.
6. Le succès du pipeline CI.
7. La validation par un membre.
8. La fusion finale.

---

# 14. Membres de l'équipe

| Nom                       | Responsabilité              |
| ------------------------- | --------------------------- |
| Masango Alain Blaise      | Tests, CI/CD, documentation |
| Iteriteka Ange Chanciella | Authentification            |
| Irishura Darlene          | Gestion des livres          |
| Akimana Nelly Franck      | Gestion des emprunts        |
| Ezako Juste Ariel         | Gestion des catégories      |

---

# 15. Licence

Ce projet utilise la licence Open Source MIT.
