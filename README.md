# TiltWords API

Backend API développé avec Django pour une application mobile de jeu de mots à deviner.

L’application mobile (iOS / React Native ou équivalent) consomme cette API afin de :
- récupérer des mots aléatoires par catégorie,
- gérer les comptes utilisateurs,
- enregistrer les actions de jeu (mot trouvé / passé).

Le backend est volontairement découplé de la logique d’interface et des capteurs mobiles
(inclinaison du téléphone), qui sont entièrement gérés côté client.

---

## Concept de l’application

L’utilisateur ouvre l’application mobile, choisit une catégorie (culture, sport, science, histoire),
puis reçoit des mots à faire deviner à une autre personne.

- Si le mot est trouvé : l’utilisateur incline le téléphone vers l’avant
- Si le mot est passé : l’utilisateur incline le téléphone vers l’arrière

Dans les deux cas, un nouveau mot est fourni par l’API.

---

## Objectifs du projet

- Concevoir une API REST claire et évolutive
- Découpler totalement frontend mobile et backend
- Implémenter une gestion simple des utilisateurs
- Gérer une randomisation contrôlée des mots
- Poser une base saine pour des évolutions futures (scores, statistiques, API publique)

Projet réalisé dans un objectif d’apprentissage de Django après une expérience préalable en développement web et infrastructure.

---

## Fonctionnalités (Backend)

### Version actuelle (MVP)

- Authentification utilisateur (JWT)
- Liste des catégories de mots
- Récupération d’un mot aléatoire par catégorie
- Enregistrement des événements de jeu :
  - mot trouvé
  - mot passé

### Fonctionnalités prévues

- Anti-répétition des mots
- Difficulté des mots
- Historique utilisateur
- Statistiques simples
- API publique en lecture seule

---

## Stack technique

- Python 3
- Django
- Django REST Framework
- JWT (SimpleJWT)
- Base de données : SQLite (dev) / PostgreSQL (prod)

---

## Architecture du projet

