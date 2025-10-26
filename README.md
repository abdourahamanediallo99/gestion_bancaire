# Gestion Bancaire - API Laravel avec Swagger

Une application Laravel pour la gestion bancaire avec documentation API automatique via Swagger.

## Déploiement sur Render

### Prérequis
- Compte Render
- GitHub repository

### Configuration Render
1. Connectez votre repository GitHub à Render
2. Utilisez le fichier `render.yaml` pour la configuration automatique
3. Configurez les variables d'environnement dans le dashboard Render :
   - `DATABASE_URL` : URL de la base de données PostgreSQL (fournie par Render)
   - `APP_KEY` : Clé d'application Laravel (générez avec `php artisan key:generate`)

### Variables d'environnement
Copiez le contenu de `.env.example` et ajustez les valeurs selon votre environnement Render.

## Développement local

### Avec Docker Compose
```bash
# Construire et démarrer les services
docker-compose up --build

# L'application sera disponible sur http://localhost
# La documentation Swagger sur http://localhost/api/documentation
```

### Installation manuelle
```bash
# Installer les dépendances
composer install

# Copier le fichier d'environnement
cp .env.example .env

# Générer la clé d'application
php artisan key:generate

# Générer la documentation Swagger
php artisan l5-swagger:generate

# Démarrer le serveur
php artisan serve
```

## API Documentation

La documentation Swagger est automatiquement générée et accessible via :
- Interface web : `/api/documentation`
- JSON : `/docs/api-docs.json`

## Technologies utilisées
- Laravel 10
- PHP 8.3
- PostgreSQL
- Nginx
- Docker
- L5-Swagger pour la documentation API
# gestion_bancaire
