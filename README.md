# Классификация степени ожирения

![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-notebook-F37626?logo=jupyter&logoColor=white)

Учебный проект по машинному обучению (МГТУ им. Н.Э. Баумана, 2023): по возрасту, полу, росту, весу и ИМТ предсказать категорию веса — `Label` (например, *Normal Weight*).

## Что сделано в [Project.ipynb](Project.ipynb)

1. Загрузка датасета [`Data.csv`](Data.csv) (108 записей) и разведочный анализ: основные характеристики, графики распределений.
2. Подготовка признаков: `LabelEncoder` для `Gender` и `Label`, Min-Max масштабирование.
3. Корреляционный анализ.
4. Выбор метрик: precision и F1.
5. Три модели: логистическая регрессия, k ближайших соседей, случайный лес.
6. Baseline без подбора гиперпараметров, затем подбор через `GridSearchCV` и сравнение.

## Результат

| Модель | precision | F1 |
|---|---|---|
| Логистическая регрессия | 0.58 | 0.58 |
| k ближайших соседей (k = 5) | 0.86 | 0.84 |
| Случайный лес | 1.00 | 1.00 |

Лучшей оказалась модель случайного леса. На таком маленьком датасете идеальный результат, скорее всего, связан с тем, что `BMI` почти однозначно определяет категорию.

## Как запустить

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook Project.ipynb
```

## Автор

Салженикин Даниил, МГТУ им. Н.Э. Баумана.
