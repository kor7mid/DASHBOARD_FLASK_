---

# GESTION DES EMPLOYES AVEC FLASJ

Description brève du projet.

## Installation

### Cloner le Dépôt

1. Clonez le dépôt de votre projet depuis GitHub :
   ```bash
   $ git clone https://github.com/kor7mid/DASHBOARD_FLASK_.git
   ```

2. Accédez au répertoire du projet :
   ```bash
   $ cd votre-projet
   ```

### Configuration de l'Environnement

#### Unix / MacOS
- Installez les modules via `VENV` :
  ```bash
  $ virtualenv env
  $ source env/bin/activate
  $ pip3 install -r requirements.txt
  ```

- Configurez l'environnement Flask :
  ```bash
  $ export FLASK_APP=run.py
  $ export FLASK_ENV=development
  ```

#### Windows
- Installez les modules via `VENV` (Windows) :
  ```bash
  $ virtualenv env
  $ .\env\Scripts\activate
  $ pip3 install -r requirements.txt
  ```

- Configurez l'environnement Flask :
  - **CMD** :
    ```bash
    $ set FLASK_APP=run.py
    $ set FLASK_ENV=development
    ```
  - **Powershell** :
    ```bash
    $ $env:FLASK_APP = ".\run.py"
    $ $env:FLASK_ENV = "development"
    ```

### Démarrer l'Application

1. Lancez l'application Flask :
   ```bash
   $ flask run
   ```

   L'application sera accessible à l'adresse : `http://127.0.0.1:5000/`

   Pour un serveur HTTPS :
   ```bash
   $ flask run --cert=adhoc
   ```

## Recompilez le SCSS

1. Installez les modules :
   ```bash
   $ yarn # installe les modules
   ```

2. Éditez les variables dans `_variables.scss` pour personnaliser les couleurs :
   ```scss
   $default: #344675 !default; // EDIT pour personnalisation
   $primary: #e14eca !default; // EDIT pour personnalisation
   $secondary: #f4f5f7 !default; // EDIT pour personnalisation
   $success: #00f2c3 !default; // EDIT pour personnalisation
   $info: #1d8cf8 !default; // EDIT pour personnalisation
   $warning: #ff8d72 !default; // EDIT pour personnalisation
   $danger: #fd5d93 !default; // EDIT pour personnalisation
   $black: #222a42 !default; // EDIT pour personnalisation
   ```

3. Compilez SCSS en CSS :
   ```bash
   $ gulp # Traduction de SCSS en CSS
   ```

## Structure du Projet

Voici un aperçu de la structure de votre projet :
```
< PROJECT ROOT >
   |
   |-- apps/
   |    |
   |    |-- home/                           # App simple pour servir les fichiers HTML
   |    |    |-- routes.py                  # Définit les routes de l'application
   |    |
   |    |-- authentication/                 # Gère les routes d'authentification (login et register)
   |    |    |-- routes.py                  # Définit les routes d'authentification
   |    |    |-- models.py                  # Définit les modèles
   |    |    |-- forms.py                   # Définit les formulaires d'authentification (login et register)
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>          # Fichiers CSS, fichiers Javascript
   |    |
   |    |-- templates/                      # Modèles utilisés pour rendre les pages
   |    |    |-- includes/                  # Chunks et composants HTML
   |    |    |    |-- navigation.html       # Composant de menu supérieur
   |    |    |    |-- sidebar.html          # Composant de barre latérale
   |    |    |    |-- footer.html           # Pied de page de l'application
   |    |    |    |-- scripts.html          # Scripts communs à toutes les pages
   |    |    |
   |    |    |-- layouts/                   # Pages maîtresses
   |    |    |    |-- base-fullscreen.html  # Utilisé par les pages d'authentification
   |    |    |    |-- base.html             # Utilisé par les pages courantes
   |    |    |
   |    |    |-- accounts/                  # Pages d'authentification
   |    |    |    |-- login.html            # Page de connexion
   |    |    |    |-- register.html         # Page d'inscription
   |    |    |
   |    |    |-- home/                      # Pages de l'interface utilisateur
   |    |         |-- index.html            # Page d'accueil
   |    |         |-- 404-page.html         # Page 404
   |    |         |-- *.html                # Toutes les autres pages
   |    |
   |  config.py                             # Configuration de l'application
   |    __init__.py                         # Initialiser l'application
   |
   |-- requirements.txt                     # Dé

pendances de l'application
   |
   |-- .env                                 # Configuration par injection via l'environnement
   |-- run.py                               # Démarrer l'application - passerelle WSGI
   |
   |-- ************************************************************************
```

## Documentation Complète

Pour une documentation plus détaillée sur les routes, les modèles, les formulaires, etc., veuillez consulter les fichiers correspondants dans le répertoire `apps`.

---
