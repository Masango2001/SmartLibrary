# Smart Library

## 📚 Présentation du projet

**Smart Library** est une application web de gestion d'une bibliothèque développée avec **Django** et le moteur de **Templates Django**. L'application permet de gérer les utilisateurs, les livres, les catégories et les emprunts à travers une interface web conviviale.

Ce projet a été réalisé dans le cadre d'un travail pratique sur la collaboration avec **Git** et **GitHub**. Il met en œuvre les bonnes pratiques de développement collaboratif :

- Gestion de versions avec Git
- Dépôt centralisé sur GitHub
- Travail collaboratif avec des branches
- Pull Requests et revue de code
- Protection des branches
- Intégration Continue (CI) avec GitHub Actions

---

## 🎯 Objectifs

- Développer une application web avec Django.
- Utiliser les Templates Django pour l'interface utilisateur.
- Appliquer une stratégie de gestion de branches.
- Collaborer efficacement avec GitHub.
- Automatiser les vérifications du code avec GitHub Actions.
- Exécuter automatiquement les tests unitaires.
- Mettre en place un workflow professionnel de validation du code.

---

## 🛠️ Technologies utilisées

### Backend

- Python
- Django

### Frontend

- Django Templates
- HTML5
- CSS3
- Bootstrap 5

### Base de données

- SQLite

### Gestion de versions

- Git
- GitHub

### Intégration Continue

- GitHub Actions
- Ruff
- Django Unit Tests

---

## ✨ Fonctionnalités

### 👤 Gestion des utilisateurs (`accounts`)

- Inscription
- Connexion / Déconnexion
- Gestion des profils
- Gestion des permissions

### 📚 Gestion des livres (`books`)

- Ajouter un livre
- Modifier un livre
- Supprimer un livre
- Rechercher un livre
- Consulter la liste des livres

### 🗂 Gestion des catégories (`categories`)

- Ajouter une catégorie
- Modifier une catégorie
- Supprimer une catégorie
- Associer un livre à une catégorie

### 🔄 Gestion des emprunts (`borrows`)

- Emprunter un livre
- Retourner un livre
- Consulter l'historique des emprunts

---

## 📁 Structure du projet

```text
smart_library/

├── accounts/
├── books/
├── borrows/
├── categories/
├── config/
├── templates/
│   ├── accounts/
│   ├── books/
│   ├── borrows/
│   ├── categories/
│   └── base.html
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── .github/
│   └── workflows/
│       └── ci.yml
├── manage.py
├── requirements.txt
├── README.md
├── LICENSE
└── .gitignore
```

---

## 🌿 Stratégie Git

```text
main 🔒
 │
 └── develop
      │
      ├── feature/accounts
      ├── feature/books
      ├── feature/categories
      ├── feature/borrows
      └── feature/tests-ci
```

### Branches

#### `main`

- Version stable
- Aucun push direct
- Pull Request obligatoire
- Pipeline CI obligatoire
- Validation obligatoire

#### `develop`

- Branche d'intégration
- Toutes les branches `feature/*` sont fusionnées ici

#### Branches `feature/*`

Chaque développeur travaille dans sa propre branche avant de créer une Pull Request vers `develop`.

---

## 👥 Répartition des tâches

| Branche | Responsable | Travail |
|----------|-------------|---------|
| feature/accounts | Iteriteka Ange Chanciella | Authentification |
| feature/books | Irishura Darlene | Gestion des livres |
| feature/categories | Ezako Juste Ariel | Gestion des catégories |
| feature/borrows | Akimana Nelly Franck | Gestion des emprunts |
| feature/tests-ci | Masango Alain Blaise | Tests, CI, Documentation |

---

## 🔄 Workflow Git

### 1. Mettre à jour `develop`

```bash
git checkout develop
git pull origin develop
```

### 2. Créer une branche

```bash
git checkout -b feature/books
```

### 3. Développer

```bash
git add .
git commit -m "Add book management"
```

### 4. Envoyer la branche

```bash
git push origin feature/books
```

### 5. Créer une Pull Request

```text
Feature Branch
      │
      ▼
Code Review
      │
      ▼
GitHub Actions
      │
      ▼
Merge vers develop
```

---

## 🔒 Protection des branches

Les branches `main` et `develop` sont protégées par les règles suivantes :

- Interdiction des push directs
- Pull Request obligatoire
- Validation par un ou plusieurs reviewers
- Pipeline CI obligatoire
- Branche à jour avant la fusion

---

## ⚙️ Pipeline CI

Le pipeline est défini dans :

```text
.github/workflows/ci.yml
```

À chaque **Push** ou **Pull Request**, GitHub Actions exécute automatiquement :

### Installation

```bash
pip install -r requirements.txt
```

### Analyse du code

```bash
ruff check .
```

### Tests

```bash
python manage.py test
```

Si une étape échoue :

```text
❌ CI Failed
```

La Pull Request est bloquée.

Si toutes les étapes réussissent :

```text
✅ CI Passed
```

La Pull Request peut être fusionnée.

---

## 🚀 Installation

### Cloner le dépôt

```bash
git clone <URL_DU_DEPOT>
```

### Se placer dans le projet

```bash
cd smart_library
```

### Créer un environnement virtuel

```bash
python -m venv venv
```

### Activer l'environnement

Windows

```bash
venv\Scripts\activate
```

Linux / macOS

```bash
source venv/bin/activate
```

### Installer les dépendances

```bash
pip install -r requirements.txt
```

### Appliquer les migrations

```bash
python manage.py migrate
```

### Créer un superutilisateur

```bash
python manage.py createsuperuser
```

### Lancer le serveur

```bash
python manage.py runserver
```

Ouvrir :

```text
http://127.0.0.1:8000/
```

Administration Django :

```text
http://127.0.0.1:8000/admin/
```

---

## 🧪 Tests

Lancer tous les tests :

```bash
python manage.py test
```

Les tests couvrent :

- Authentification
- Livres
- Catégories
- Emprunts

---

## 🎓 Démonstration

La démonstration du projet montre :

1. Création d'une Pull Request
2. Exécution automatique du pipeline CI
3. Échec volontaire d'un test
4. Blocage de la Pull Request
5. Correction du problème
6. Nouveau passage du pipeline
7. Validation par un reviewer
8. Fusion vers `develop`
9. Fusion finale vers `main`

---

## 👨‍💻 Membres de l'équipe

| Nom | Responsabilité |
|------|----------------|
| Masango Alain Blaise | Tests, GitHub Actions, Documentation |
| Iteriteka Ange Chanciella | Authentification |
| Irishura Darlene | Gestion des livres |
| Akimana Nelly Franck | Gestion des emprunts |
| Ezako Juste Ariel | Gestion des catégories |

---

## 📄 Licence

Ce projet est distribué sous la licence **MIT**.

---

## 🤝 Contribution

Pour contribuer :

1. Mettre à jour `develop`
2. Créer une branche `feature/*`
3. Développer la fonctionnalité
4. Créer une Pull Request
5. Attendre la revue de code
6. Vérifier le succès du pipeline CI
7. Fusionner après validation