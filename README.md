# Проект NLP: Классификация сообщений на спам/неспам

### Выполнил: Палысаев Вадим, студент первого курса ФКН ПМИ

## Описание проекта

В этом проекте, посвященном введению в обработку естественного языка (NLP), я исследую задачу классификации текстовых сообщений на спам и неспам. Целью было создать нейросеть, способную определять, является ли сообщение спамом, используя известные алгоритмы классификации и библиотеки Python.

### Основные цели проекта

1. Провести предварительный анализ датасета.
2. Освоить методы первичной обработки текста.
3. Привести текстовые данные к векторному виду.
4. Написать и обучить нейронную сеть на основе популярных алгоритмов для классификации спама.
5. Проанализировать и оценить качество модели с помощью метрик accuracy и ROC-AUC.

### Используемые библиотеки и технологии

Для выполнения проекта я изучил и применил следующие библиотеки:
- **pandas** — для чтения и работы с датасетами.
- **nltk** — для предобработки текста (удаление стоп-слов и знаков препинания).
- **seaborn** и **sklearn** — для визуализации и векторизации текстов, а также для обучения модели.

Я также изучил подход "мешок слов" (bag-of-words) и алгоритмы классификации, такие как Наивный Байесовский Классификатор и Логистическая регрессия, которые были применены для построения классификатора спама.

### Первичный анализ данных

- Загружен датасет с помощью `pandas`, удалены пустые значения и назначены названия столбцов.
- Произведен анализ данных для спам и неспам-сообщений, определена частота встречаемости различных слов и длина сообщений.

### Токенизация и векторизация

Для преобразования текстов в вектора были выполнены следующие шаги:

- Удалены знаки препинания и стоп-слова.
- Выполнена векторизация с использованием модели "мешок слов".

### Построение и обучение модели

#### Наивный Байесовский Классификатор

Для классификации я использовал **Наивный Байесовский Классификатор** (MultinomialNB), который показал точность более 98%. Модель имеет высокий уровень правильных предсказаний, но не откалибрована, что выявлено при оценке вероятностей предсказаний.

#### Логистическая регрессия

Логистическая регрессия также достигла точности выше 98%, и показала лучший уровень калибровки, что делает её более надежной для использования на реальных данных.

### Оценка моделей

Для оценки моделей я использовал:

- **Accuracy** — точность классификации, которая для обеих моделей превышает 98%.
- **ROC-AUC** — площадь под кривой ошибок, которая также показывает высокий уровень качества обеих моделей.

### Выводы

В результате работы были достигнуты следующие цели:

- Я изучил и провел предобработку данных, создал векторы признаков и исследовал методы улучшения качества векторизации.
- Были построены и обучены две модели классификации спама: Наивный Байесовский Классификатор и Логистическая регрессия.
- Оценка показала, что обе модели хорошо справляются с классификацией спама, но логистическая регрессия обладает лучшим уровнем калибровки и точности на реальных данных.