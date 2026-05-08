# U12 Post 2 - CI/CD con GitHub Actions y Docker Hub

![CI/CD Status](https://github.com/<usuario>/<repo>/actions/workflows/ci.yml/badge.svg)

## Requisitos
- Java 17
- Maven 3.9+
- Docker Hub (Access Token)

## Secrets requeridos
- DOCKERHUB_USERNAME
- DOCKERHUB_TOKEN

## Pipeline
1. Compilar y ejecutar pruebas con JaCoCo
2. Publicar reporte JaCoCo como artefacto
3. Construir imagen Docker multi-stage
4. Publicar imagen en Docker Hub con tags latest y sha-<commit>

## Imagen Docker
```bash
docker pull <usuario>/mi-spring-app:latest
```

## Evidencias (colocar en img/)
- img/checkpoint1.png (historial Actions con checks verdes)
- img/checkpoint2.png (artefacto JaCoCo descargado)
- img/checkpoint3.png (Docker Hub con tags latest y sha)
