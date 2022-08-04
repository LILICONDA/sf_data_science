# Проект. Прогнозирование биологического ответа (соревнование на Kaggle: Predicting a Biological Response) 

## Оглавление
[1. Описание проекта](https://github.com/LILICONDA/sf_data_science/tree/main/Predicting a Biological Response/README.md#Описание-проекта)

[2. Какой кейс решаем](https://github.com/LILICONDA/sf_data_science/tree/main/Predicting a Biological Response/README.md#Какой-кейс-решаем)

[3. Краткая информация о данных](https://github.com/LILICONDA/sf_data_science/tree/main/Predicting a Biological Response/README.md#Краткая-информация-о-данных)

[4. Этапы работы над проектом](https://github.com/LILICONDA/sf_data_science/tree/main/Predicting a Biological Response/README.md#Этапы-работы-над-проектом)

[5. Выводы](https://github.com/LILICONDA/sf_data_science/tree/main/Predicting a Biological Response/README.md#Выводы)

### Описание проекта
Необходимо предсказать биологический ответ молекул (столбец 'Activity') по их химическому составу (столбцы D1-D1776). Данные представлены в формате CSV.  Каждая строка представляет молекулу. 
Первый столбец Activity содержит экспериментальные данные, описывающие фактический биологический ответ [0, 1]. Остальные столбцы D1-D1776 представляют собой молекулярные дескрипторы — это вычисляемые свойства, которые могут фиксировать некоторые характеристики молекулы, например размер, форму или состав элементов.


### Какой кейс решаем?
Необходимо обучить две модели: логистическую регрессию и случайный лес. Далее нужно сделать подбор гиперпараметров с помощью базовых и продвинутых методов оптимизации. Важно использовать все четыре метода (GridSeachCV, RandomizedSearchCV, Hyperopt, Optuna) хотя бы по разу, максимальное количество итераций не должно превышать 50.

### Краткая информация о данных
GitHub не поддерживает отображение интерактивной визуализации в Plotly. Графики, построенные с помощью Plotly, могут не отображаться на странице репозитория. Для того, чтобы посмотреть графики предоставляется ссылка на Notebook on nbviewer: https://nbviewer.org/github/LILICONDA/sf_data_science/blob/main/Predicting a Biological Response/Predicting a Biological Response.ipynb


### Этапы работы над проектом
1. Обучение двух моделей: логистичекой регрессии и случайного леса (использование кросс-валидации).
2. Подбор гиперпараметров с помощью метода GridSeachCV и обучение моделей.
3. Подбор гиперпараметров с помощью метода RandomizedSearchCV и обучение модели.
4. Подбор гиперпараметров с помощью метода Hyperopt и обучение модели (использование кросс-валидации).
5. Подбор гиперпараметров с помощью метода Optuna и обучение модели (использование кросс-валидации).


### Выводы:
Наилучшую метрику удалось получить с гиперпараметрами, подобранными с помощью методов Optuna и GridSeachCV. Однако время, затраченное на подбор параметров с помощью метода GridSeachCV значительно больше, чем у метода Optuna.