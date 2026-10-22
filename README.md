# Kwatsur — structure initiale

Kwatsur est un agent conversationnel de recherche et de comparaison de logements à louer, conçu d’abord pour le marché camerounais.

Cette arborescence est un squelette de projet, pas une application terminée.

## Architecture

Architecture en couches inspirée de MVC :
1. `frontend/` : présentation HTML/CSS/JavaScript.
2. `app/api/routes/` : contrôleurs HTTP FastAPI.
3. `app/services/` : logique métier et cas d’utilisation.
4. `app/repositories/` : accès aux données persistées.
5. `app/models/` et `app/schemas/` : persistance SQLAlchemy et contrats Pydantic.
6. `app/integrations/` : adaptateurs des fournisseurs externes.
7. `app/db/`, `migrations/` et Docker : infrastructure.

Les routes ne contiennent pas la logique métier complexe. Les services ne dépendent pas des détails HTTP. Les adaptateurs isolent les fournisseurs externes.

## Dossiers

Chaque dossier contient un fichier `<nom_du_dossier>_readme.md` qui explique sa responsabilité et les règles de contribution.

- `app/` : backend Python.
- `frontend/` : interface web.
- `tests/` : tests unitaires, d’intégration et E2E.
- `migrations/` : migrations de schéma.
- `scripts/` : scripts répétables.
- `docs/` : documentation technique.

## Règles

- Utiliser Service Layer, Repository, Dependency Injection et Adapter quand ils apportent une vraie valeur.
- Ne pas inventer de données, d’endpoints ou d’intégrations.
- Marquer les données de démonstration comme fictives.
- Garder les secrets dans `.env`, jamais dans Git ni dans le frontend.
- Ne déclarer un test réussi qu’après l’avoir exécuté.

## État actuel

Le script crée la structure et des fichiers de départ ; il ne constitue pas une application complète. Les dépendances, routes, modèles, migrations, intégrations et fichiers Docker restent à implémenter.
