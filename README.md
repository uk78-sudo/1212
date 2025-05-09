# Проект по анализу данных

Этот проект создан для анализа, обработки и визуализации структурированных данных с использованием Python.

## Структура проекта

```
data-analysis-project/
├── data/                  # Директория для наборов данных
│   └── README.md          # Описание форматов данных
├── src/                   # Исходный код
│   ├── __init__.py
│   ├── data_loader.py     # Загрузка данных
│   ├── data_cleaner.py    # Очистка данных
│   ├── data_analyzer.py   # Количественный анализ
│   └── data_visualizer.py # Визуализация данных
├── notebooks/             # Jupyter notebooks для интерактивного анализа
│   └── example_analysis.ipynb  
├── results/               # Результаты анализа и визуализации
├── requirements.txt       # Зависимости проекта
├── setup.py               # Установка проекта
└── README.md              # Описание проекта
```

## Установка

```bash
# Клонирование репозитория
git clone https://github.com/username/data-analysis-project.git
cd data-analysis-project

# Установка зависимостей
pip install -r requirements.txt

# Установка проекта в режиме разработки
pip install -e .
```

## Использование

### Загрузка и очистка данных

```python
from src.data_loader import load_data
from src.data_cleaner import clean_data

# Загрузка данных из CSV-файла
data = load_data('data/dataset.csv')

# Очистка данных
cleaned_data = clean_data(data)
```

### Анализ данных

```python
from src.data_analyzer import calculate_statistics, analyze_by_category

# Получение основных статистик
stats = calculate_statistics(cleaned_data, 'value')
print(stats)

# Анализ по категориям
category_analysis = analyze_by_category(cleaned_data, 'category', 'value')
print(category_analysis)
```

### Визуализация

```python
from src.data_visualizer import plot_histogram, plot_boxplot, plot_heatmap

# Построение гистограммы
plot_histogram(cleaned_data, 'value')

# Построение box plot по категориям
plot_boxplot(cleaned_data, 'category', 'value')

# Построение тепловой карты корреляций
plot_heatmap(cleaned_data)
```

## Требования

- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn

## Лицензия

MIT
