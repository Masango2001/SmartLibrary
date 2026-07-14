[14:57, 7/14/2026] ange schl: # 📚 BiblioManager
## Système de Gestion de Bibliothèque

![Django](https://img.shields.io/badge/Django-5.x-darkgreen)
![Python](https://img.shields.io/badge/Python-3.12-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![GitHub Actions](https://img.shields.io/badge/CI-GitHub%20Actions-orange)

---

# Présentation

*BiblioManager* est une application Web développée avec *Django* utilisant le moteur de templates Django pour l'affichage des interfaces utilisateur.

L'objectif principal est de permettre à une bibliothèque de gérer efficacement ses livres, ses membres ainsi que les opérations d'emprunt et de retour.

Ce projet est réalisé dans le cadre du *cours de DevOps* afin de mettre en pratique les bonnes pratiques de développement collaboratif, l'intégration continue (CI), GitHub Flow et GitHub Actions.

---

# Objectifs du projet

L'application doit permettre de :

- gérer les livres ;
- gérer les catégories ;
- gérer les auteurs ;
- gérer les membres ;
- gérer les emprunts ;
- gérer les retours ;
- gérer les utilisateurs ;
- produire quelques statistiques.

Le projet est développé suivant une architecture propre permettant une maintenance simple et un travail collaboratif.

---

# Technologies utilisées

| Technologie | Utilisation |
|-------------|-------------|
| Python 3.12 | Langage principal |
| Django 5 | Framework Web |
| HTML5 | Interfaces |
| CSS3 | Mise en forme |
| Bootstrap 5 | Design |
| SQLite | Base de données |
| Git | Versionnement |
| GitHub | Dépôt centralisé |
| GitHub Actions | Intégration Continue (CI) |

---

# Fonctionnalités

## Gestion des livres

- Ajouter un livre
- Modifier un livre
- Supprimer un livre
- Consulter tous les livres
- Rechercher un livre

Chaque livre possède :

- titre
- ISBN
- auteur
- catégorie
- année de publication
- nombre d'exemplaires
- disponibilité

---

## Gestion des auteurs

- Ajouter un auteur
- Modifier un auteur
- Supprimer un auteur
- Liste des auteurs

---

## Gestion des catégories

- Ajouter une catégorie
- Modifier
- Supprimer
- Liste

Exemple :

- Informatique
- Mathématiques
- Physique
- Roman
- Histoire

---

## Gestion des membres

Chaque membre possède :

- Nom
- Prénom
- Email
- Téléphone
- Adresse
- Date d'inscription

Le système permet :

- l'inscription
- la modification
- la suppression
- la consultation

---

## Gestion des emprunts

Un membre peut emprunter un ou plusieurs livres.

Le système enregistre :

- le membre
- le livre
- la date d'emprunt
- la date de retour prévue
- le statut

---

## Gestion des retours

Le bibliothécaire peut enregistrer :

- le retour d'un livre
- la date réelle du retour

Le stock est automatiquement mis à jour.

---

## Tableau de bord

Le tableau de bord affiche :

- nombre de livres
- nombre de catégories
- nombre d'auteurs
- nombre de membres
- emprunts en cours
- livres disponibles
- livres empruntés

---

# Architecture du projet


BiblioManager/

│
├── bibliomanager/
│
├── library/
│
├── templates/
│
├── static/
│
├── media/
│
├── tests/
│
├── requirements.txt
│
├── manage.py
│
└── README.md


---

# Installation

## Cloner le projet

bash
git clone https://github.com/Organisation/BiblioManager.git


---

Créer un environnement virtuel

bash
python -m venv venv


---

Activer l'environnement

Windows

bash
venv\Scripts\activate


Linux

bash
source venv/bin/activate


---

Installer les dépendances

bash
pip install -r requirements.txt


---

Effectuer les migrations

bash
python manage.py migrate


---

Créer un administrateur

bash
python manage.py createsuperuser


---

Lancer le serveur

bash
python manage.py runserver


Puis ouvrir :


http://127.0.0.1:8000


---

# Tests

Les tests peuvent être exécutés avec :

bash
python manage.py test


---

# Intégration Continue

À chaque :

- Push
- Pull Request

GitHub Actions exécute automatiquement :

- Vérification du code (Lint)
- Exécution des tests unitaires

Aucune Pull Request ne peut être fusionnée si les tests échouent.

---

# Organisation du travail

Le projet est développé suivant *GitHub Flow*.

Chaque fonctionnalité est développée dans une branche indépendante puis intégrée via une Pull Request.

La branche *main* est protégée.

Les Push directs sont interdits.

---

# Répartition des tâches

| Membre | Responsabilités |
|---------|-----------------|
| *IRISHURA Darlene* | Gestion des catégories, documentation utilisateur |
| *ITERITEKA Ange Chanciella* | Chef de projet, configuration Django, GitHub, GitHub Actions, Dashboard |
| *MASANGO Alain Blaise* | Gestion des livres |
| *EZAKO Juste Ariel* | Gestion des membres |
| *AKIMANA Nelly Franck* | Gestion des emprunts, retours et tests unitaires |

---

# Workflow Git

Chaque membre suit les étapes suivantes :

1. Créer une branche


feature/nom-fonctionnalite


Exemple :


feature/books
feature/members
feature/dashboard


2. Développer la fonctionnalité.

3. Commit.

4. Push.

5. Créer une Pull Request.

6. Validation par un autre membre.

7. Fusion dans la branche *main*.

---

# Licence

Ce projet est distribué sous la licence *MIT*.

---

# Équipe

Projet réalisé dans le cadre du cours de *DevOps*.

### Membres

- IRISHURA Darlene
- ITERITEKA Ange Chanciella
- MASANGO Alain Blaise
- EZAKO Juste Ariel
- AKIMANA Nelly Franck

---

# Remerciements

Nous remercions notre enseignant du cours de *DevOps* pour son accompagnement dans la réalisation de ce projet ainsi que l'ensemble des membres de l'équipe pour leur collaboration.
[15:40, 7/14/2026] ange schl: | Nom | Responsabilité |
|------|----------------|
| Masango Alain Blaise | Tests, GitHub Actions, Documentation |
| Iteriteka Ange Chanciella | Authentification |
| Irishura Darlene | Gestion des livres |
| Akimana Nelly Franck | Gestion des emprunts |
| Ezako Juste Ariel | Gestion des catégories |
