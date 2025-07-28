  GNU nano 8.3                                              README.md                                                        
# Jenkins CI para n8n 🚀

Este proyecto muestra cómo usar Jenkins para construir una imagen Docker de n8n usando un pipeline simple.

## Estructura del proyecto

- `Dockerfile`: usa la imagen oficial de n8n
- `Jenkinsfile`: define el pipeline CI en Jenkins
- `README.md`: esta documentación

## Pasos del Pipeline

1. Clonar este repositorio
2. Construir imagen Docker `n8n-ci:build-[número]`
3. Verificar que la imagen fue construida exitosamente

## Próximos pasos

- Publicar en Docker Hub o GCP Artifact Registry
- Agregar etapa de despliegue en Kubernetes (GKE)
- Integrar pruebas automatizadas

## Autor

Diego Arras - [darrasca](https://github.com/darrasca)
