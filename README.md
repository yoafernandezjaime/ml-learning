# ml-learning

## Proyecto SageMaker

Proyecto de práctica con AWS SageMaker y MLflow para entrenamiento y despliegue de modelos de Machine Learning.

---

## Tecnologías

- Python
- AWS SageMaker
- MLflow
- S3
- scikit-learn / CatBoost / XGBoost

---

## Estructura del proyecto

```text
ml-learning/
│
├── config.yaml                    # Configuración del proyecto (AWS, modelo, parámetros)
├── requirements.txt              # Librerías necesarias para ejecutar el proyecto
├── README.md                     # Documentación del proyecto
├── .gitignore                    # Archivos que Git NO debe versionar
│
├── development/                  # Zona de experimentación y desarrollo de modelos
│   └── model_name/              # Nombre del caso de uso (ej: fraud_detection)
│       └── v1/                  # Versión del pipeline/modelo
│           │
│           ├── pipeline.py      # Orquesta el pipeline (preprocess + train + eval)
│           │
│           ├── 01_data/         # Datos del proyecto
│           │   ├── raw/         # Datos sin procesar
│           │   ├── processed/   # Datos limpios listos para modelar
│           │   └── exploratory/# Análisis exploratorio (EDA)
│           │
│           ├── 02_model/        # Desarrollo del modelo
│           │   ├── experiments/ # Pruebas de modelos e hiperparámetros
│           │   └── artifacts/   # Outputs del modelo (gráficos, features, etc.)
│           │
│           └── 03_model_testing/# Evaluación del modelo
│               ├── metrics/     # Métricas (AUC, accuracy, etc.)
│               ├── predictions/ # Predicciones generadas
│               └── reports/     # Reportes finales de performance
│
└── src/                          # Código reutilizable (core del sistema)
    ├── __init__.py              # Marca src como paquete Python
    ├── preprocess.py            # Limpieza y transformación de datos
    ├── train.py                 # Entrenamiento del modelo + MLflow
    └── inference.py             # Predicción con modelo ya entrenado
