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
├── config.yaml
├── requirements.txt
├── README.md
├── .gitignore
│
├── development/
│   └── model_name/
│       └── v1/
│           ├── pipeline.py
│           ├── 01_data/
│           ├── 02_model/
│           └── 03_model_testing/
│
└── src/
    ├── __init__.py
    ├── preprocess.py
    ├── train.py
    └── inference.py
