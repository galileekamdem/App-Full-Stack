# App-Full-Stack

#  Projet Full Stack - Flask + PostgreSQL + Kubernetes

Ce projet est une application web full stack construite avec :
-  Frontend : HTML, CSS, JavaScript (Vanilla)
-  Backend : Python Flask
-  Base de données : PostgreSQL
-  Orchestration : Kubernetes (minikube)
-  CI/CD : Jenkins

##  Objectif

Mettre en œuvre un pipeline DevOps complet :
- Déploiement d’une app full stack sur Kubernetes
- Automatisation du build, test, conteneurisation et déploiement avec Jenkins

##  Technologies utilisées

| Composant       | Technologie              |
|------------------|---------------------------|
| Frontend         | HTML, CSS, JavaScript     |
| Backend          | Python Flask              |
| Base de données  | PostgreSQL                |
| Conteneurisation | Docker                    |
| Orchestration    | Kubernetes (Minikube)     |
| CI/CD            | Jenkins                   |

---

##  Prérequis

### Sur votre machine de développement :
- [Python 3.10+](https://www.python.org/)
- [Docker](https://www.docker.com/)
- [Minikube](https://minikube.sigs.k8s.io/)
- [Kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Jenkins](https://www.jenkins.io/)
- Git

##  Étapes de développement

### 1. Lancer Minikube

minikube start

2. Construire les images Docker
Dans chaque dossier :

cd backend
docker build -t flask-backend:1.0 .

4. Appliquer les fichiers Kubernetes

kubectl apply -f k8s/

5. Accéder à l’application
Utilise Minikube pour récupérer l’URL :

minikube service backend-service
- Pipeline CI/CD avec Jenkins
Étapes du Jenkinsfile :
- Cloner le dépôt

- Installer les dépendances Python

- Exécuter les tests unitaires

- Builder l'image Docker

☸️ Déployer automatiquement sur Kubernetes

 Variables d’environnement recommandées
    Variable	Valeur exemple
    DB_HOST	postgres-service
    DB_PORT	5432
    DB_NAME	myapp_db
    DB_USER	user
    DB_PASSWORD	password

Auteurs
Kévin Marius Kamdem

