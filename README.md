# Santemis

Projet d'initiation pour la digitalisation du rapport mensuel d'activités intégrées (RMA) des centres de santé du SDSP Ambalavao, DRSP Haute Matsiatra. 

> Module : Centres de santé

## Backend (.NET 8, PostgreSQL)

- API RESTful pour la gestion des centres de santé
- Entity Framework Core + Npgsql
- Migrations appliquées automatiquement au démarrage
- Swagger pour la documentation API

### Lancer le backend

1. Vérifiez que PostgreSQL est lancé et accessible (voir `appsettings.json` pour la connexion)
2. Placez-vous dans le dossier `backend/`
3. Exécutez :

   ```sh
   dotnet run
   ```

   > Les migrations EF Core sont appliquées automatiquement à chaque démarrage.
   >

### Endpoints principaux

- `GET    /api/centressante` : liste des centres
- `POST   /api/centressante` : création
- `PUT    /api/centressante/{id}` : modification
- `DELETE /api/centressante/{id}` : suppression

## Frontend (React + Vite)

- Affichage, création, édition, suppression des centres de santé
- Appels API synchronisés avec le backend

### Lancer le frontend

1. Placez-vous dans le dossier `frontend/`
2. Installez les dépendances :
   ```sh
   npm install
   ```
3. Lancez le serveur de dev :
   ```sh
   npm run dev
   ```

## Configuration

- La connexion PostgreSQL se configure dans `backend/appsettings.json`
- L’URL de l’API backend est dans `frontend/src/lib/api.ts`

## Configuration de la base de données PostgreSQL

La connexion à la base de données se fait dans le fichier `backend/appsettings.json` :

```json
"ConnectionStrings": {
  "DefaultConnection": "Host=localhost;Port=5432;Database=santemis;Username=postgres;Password=postgres"
}
```

- **Host** : nom d’hôte ou IP du serveur PostgreSQL (ex : `localhost`, `127.0.0.1`, ou une IP distante)
- **Port** : port PostgreSQL (par défaut `5432`, à adapter si besoin)
- **Database** : nom de la base de données à utiliser/créer
- **Username**/**Password** : identifiants PostgreSQL

Adaptez ces valeurs selon votre environnement avant de lancer le backend.

## Dépendances principales

- .NET 8, Entity Framework Core, Npgsql
- React, Vite, TailwindCSS

---

Pour toute question, ouvrez une issue ou contactez l’équipe projet.
# dotSantemis
