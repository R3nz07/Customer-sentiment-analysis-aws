# Sentiment Analysis MLOps on AWS

Este proyecto implementa un **pipeline de análisis de sentimiento** usando el **Free Tier de AWS**.  
Incluye CI/CD con CodePipeline y CodeBuild, y servicios como S3, Glue, Athena, Redshift y SageMaker.  

## Objetivo
Analizar reseñas de clientes y clasificarlas en positivas, negativas o neutras para apoyar decisiones de negocio.

## Servicios AWS usados
- Amazon S3 (almacenamiento de datasets y artefactos)
- AWS Glue (limpieza de datos)
- Amazon Athena (exploración de datos con SQL)
- Amazon Redshift (análisis avanzado)
- Amazon SageMaker (entrenamiento y despliegue del modelo)
- AWS Lambda (inferencia automática)
- CodePipeline + CodeBuild (CI/CD)
- CloudWatch / CloudTrail (monitoreo)

## Flujo de arquitectura
Dataset → S3 → Glue → Athena/Redshift → SageMaker → Lambda → S3/Redshift → QuickSight

## Dataset
Usamos un dataset reducido de reseñas (IMDB small, ~5MB) con etiquetas de sentimiento.  
El archivo se almacena en `s3://sentiment-analysis-ds-project/raw/imdb_small.csv`.
