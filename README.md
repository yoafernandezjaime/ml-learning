## ml-learning
# Proyecto SageMaker  Proyecto de práctica con AWS SageMaker y MLflow. 
# Tecnologías - Python - SageMaker - MLflow - S3 
# Cómo ejecutar 
1. Crear un entorno virtual
2. Instalar requirements.txt
3.  Ejecutar train.py


ml-learning/
│
├── README.md                      # Documentación y descripción del proyecto
├── .gitignore                     # Archivos que Git no debe versionar
├── requirements.txt               # Librerías necesarias para ejecutar el proyecto
├── config.yaml                    # Configuración del proyecto (AWS, modelo, parámetros, etc.)
│
├── development/                   # Espacio de desarrollo y experimentación
│   └── model_name/                # Nombre del modelo/proyecto (ej. fraud_detection)
│       └── v1/                    # Versión del modelo
│           ├── pipeline.py        # Define, crea y/o ejecuta el pipeline de SageMaker
│           │
│           ├── 01_data/           # Preparación y exploración de datos
│           │   ├── raw/           # Datos originales
│           │   ├── processed/     # Datos procesados
│           │   └── exploratory/   # Análisis exploratorio (EDA)
│           │
│           ├── 02_model/          # Desarrollo y entrenamiento del modelo
│           │   ├── experiments/   # Experimentos y pruebas
│           │   └── artifacts/     # Artefactos generados (gráficos, resultados, etc.)
│           │
│           └── 03_model_testing/  # Evaluación y validación del modelo
│               ├── metrics/       # Métricas de desempeño
│               ├── predictions/   # Predicciones de prueba
│               └── reports/       # Reportes y análisis de resultados
│
└── src/                           # Código reutilizable del proyecto
    ├── __init__.py                # Indica que 'src' es un paquete de Python
    ├── preprocess.py              # Limpieza, transformación y feature engineering
    ├── train.py                   # Entrenamiento del modelo y registro en MLflow
    └── inference.py               # Carga el modelo entrenado y realiza predicciones
