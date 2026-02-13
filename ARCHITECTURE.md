# Architecture (High Level)

## Mobile
- Flutter app stores data locally in SQLite.
- User actions are written locally first.
- Sync pushes pending changes to the server and pulls updates back.

## Backend
- Django REST API with JWT authentication.
- Data is scoped by institute.
- PostgreSQL stores server-side data.

## Data Flow
- App -> API: login, sync push/pull, CRUD modules
- API -> App: tokens, data snapshots/changes
