# U12 Post 2 - CI/CD con GitHub Actions y Docker Hub

![CI/CD Status](https://github.com/ericktj21/pro-web-toloza-post2-u12/actions/workflows/ci.yml/badge.svg)

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
docker pull ericktj21/mi-spring-app:latest
```

## Evidencias
Historial de GitHub Actions con ejecuciones verdes
![Historial Actions](img/actions.png)

Artefacto JaCoCo descargado
![JaCoCo report](img/jacoco-report.png)

Docker Hub con tags latest y sha
![Docker Hub tags](img/dockerhub.png)
