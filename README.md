# fastapi-school

API REST pour la gestion d'une école : gestion des classes, élèves, matières, notes avec FastAPI et SQLAlchemy.

## Fonctionnalités

- Gestion des classes (création, modification, suppression)
- Gestion des élèves avec relations vers les classes
- Gestion des matières et des notes associées aux élèves
- Suppression en cascade (ex : suppression d'une classe supprime ses élèves)
- API documentée automatiquement avec Swagger (OpenAPI)

## Prérequis

- Python 3.10 ou plus récent
- MySQL, MariaDB ou autre base compatible avec SQLAlchemy
- pip (gestionnaire de paquets Python)
- Git

## Installation

1. Cloner le dépôt :
    ```bash
    git clone https://github.com/nellywalker/fastapi-enseignement.git
    cd fastapi-enseignement
    ```

2. Créer et activer un environnement virtuel :
    - Sur Linux/macOS :
    ```bash
    python -m venv .venv
    source .venv/bin/activate
    ```
    - Sur Windows :
    ```powershell
    python -m venv .venv
    .venv\Scripts\activate
    ```

3. Installer les dépendances :
    ```bash
    pip install -r requirements.txt
    ```

4. Configurer la connexion à la base de données (dans `app/config.py` ou via variables d'environnement).

5. (Optionnel) Appliquer les migrations si vous utilisez Alembic ou un outil similaire.

6. Lancer l'application :
    ```bash
    python run.py
    ```

## Utilisation

- Ouvrir dans un navigateur l’URL : [http://localhost:8000/docs](http://localhost:8000/docs)  
  pour accéder à la documentation interactive Swagger et tester les endpoints API.

## Tests

Pour lancer les tests unitaires, exécutez :

```bash
pytest tests/
