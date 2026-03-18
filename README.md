# 🚢 Прогнозирование выживаемости на Титанике с помощью машинного обучения

## 🛠 Инструменты и технологии

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.24+-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-11557C?style=for-the-badge&logo=plotly&logoColor=white)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-76B7B2?style=for-the-badge&logo=python&logoColor=white)](https://seaborn.pydata.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-1.7+-189ABD?style=for-the-badge&logo=python&logoColor=white)](https://xgboost.readthedocs.io/)
[![LightGBM](https://img.shields.io/badge/LightGBM-4.0+-2980B9?style=for-the-badge&logo=python&logoColor=white)](https://lightgbm.readthedocs.io/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/c/titanic)

---

## 📦 Подключение библиотек

На этом этапе импортируются необходимые библиотеки, которые играют ключевую роль в обработке и визуализации данных:

- **[pandas](https://pandas.pydata.org/)** — универсальная библиотека для манипуляции и анализа данных, позволяющая эффективно работать с табличными структурами.
- **[numpy](https://numpy.org/)** — фундаментальная библиотека для численных операций и вычислений с массивами.
- **[seaborn](https://seaborn.pydata.org/)** — мощная библиотека для визуализации данных, основанная на matplotlib.
- **[matplotlib.pyplot](https://matplotlib.org/)** — широко используемая библиотека для создания графиков и диаграмм.

---

## 📂 Загрузка данных

Проект начинается с загрузки данных из CSV-файлов с помощью библиотеки **pandas**. Данные разделены на обучающий (`train`) и тестовый (`test`) наборы и содержат ключевую информацию о пассажирах «Титаника».

---

## 🔍 Разведочный анализ данных (EDA)

В ходе EDA проводится глубокое изучение набора данных:

- **Визуализация распределений** ключевых числовых признаков: возраст, `SibSp`, `Parch`, стоимость билета (`Fare`). Это помогает выявить закономерности и обнаружить выбросы.
- **Исследование взаимосвязей** между переменными для обнаружения корреляций, важных для прогнозирования выживаемости.

---

## 🧹 Очистка данных

- **Обработка пропущенных значений** — импутация и другие методы заполнения пробелов в данных.
- **Удаление неинформативных колонок**: `PassengerId`, `Cabin`, `Name`, `Ticket`.
- **Инженерия признаков (Feature Engineering)** — создание новых характеристик и преобразование существующих для повышения качества модели.

---

## 🤖 Тестирование моделей

Оценивались следующие алгоритмы машинного обучения:

| Модель | Библиотека |
|---|---|
| [Decision Tree](https://scikit-learn.org/stable/modules/tree.html) | scikit-learn |
| [Random Forest](https://scikit-learn.org/stable/modules/ensemble.html#forests-of-randomized-trees) | scikit-learn |
| [Extra Trees](https://scikit-learn.org/stable/modules/ensemble.html#extremely-randomized-trees) | scikit-learn |
| [Logistic Regression](https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression) | scikit-learn |
| [XGBoost](https://xgboost.readthedocs.io/) | xgboost |
| [LightGBM](https://lightgbm.readthedocs.io/) | lightgbm |

🏆 Лучшая достигнутая точность: **73.8%**

---

## 📤 Формирование файла с результатами (Submission)

Применив отобранную модель к тестовому набору данных, создаётся файл `submission.csv` с предсказаниями. Этот шаг позволяет оценить, насколько хорошо модель обобщает знания на новых данных.

---

## ✅ Заключение

Достигнутая точность **73.8%** демонстрирует, что модель эффективно предсказывает выживаемость пассажиров «Титаника». Проект показывает практическое применение техник машинного обучения на исторических данных и даёт представление о факторах, определявших шансы на выживание во время катастрофы.
