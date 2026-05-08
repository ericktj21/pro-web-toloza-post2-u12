# U12 Post 1 - Docker y despliegue en Railway

## Requisitos
- Java 17
- Maven 3.9+
- Docker Desktop

## Build de imagen
```bash
docker build -t mi-app:local .
```

## Docker Compose
```bash
docker compose up -d --build
```
Verificar: http://localhost:8080/actuator/health

## Railway
- Crear proyecto desde GitHub
- Agregar PostgreSQL
- Variables:
	- SPRING_PROFILES_ACTIVE=prod
	- DATABASE_URL=${{Postgres.DATABASE_URL}}
	- DB_USER=${{Postgres.PGUSER}}
	- DB_PASS=${{Postgres.PGPASSWORD}}
- Generar dominio publico y probar /actuator/health

## Evidencias (colocar en img/)
- img/checkpoint1.png (Docker build sin errores)
- img/checkpoint2.png (docker compose up y health OK)
- img/checkpoint3.png (Railway con endpoints funcionando)
