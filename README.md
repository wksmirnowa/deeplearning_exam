# Репозиторий для проекта по глубокому обучению

## О проекте

### Цель

Решить задачу извлечения определенных именованных сущностей (локаций, персон и организаций) с метриками, не сильно уступающими state-of-the-art. 

### Бейзлайн-решение

LSTM

## Данные

### Датасет

Для выполнения проекта я нашла два почти одинаковых датасета: [CoNLL2003](https://github.com/pfliu-nlp/Named-Entity-Recognition-NER-Papers/tree/master/ner_dataset/CoNLL2003) и [CoNLL++](https://github.com/ZihanWangKi/CrossWeigh/tree/master/data). Разница между ними в том, что в CoNLL++ версии 
чуть более точно размечен файл для тестирования модели. Более точная тестовая выборка – причина, по которой я использовала датасет CoNLL++ для обучения
своей модели.

### Формат

Каждая строка данных состоит из слова, частеречного тега, тега для построения синтаксических деревьев и, собственно, NER-тега. Формат разметки – BIO. Пример разметки:

```
CHINA NNP I-NP B-LOC
IN IN I-PP O
SURPRISE DT I-NP O
DEFEAT NN I-NP O
. . O O
```

### Таргет

Предсказываем NER-тег по слову.

### State-of-the-art метрика

F-мера от 90.94 до 94.3 в зависимости от датасета (CoNLL2003 / CoNLL++) и подхода.

## Результаты и итоги

### Метрики

| Метрика      | Значение |
| ----------- | ----------- |
| micro-F1 (on test)     | 0.86      |
| macro-F1 (on test)   | 0.56        |
| accuracy (on test)   | 0.86        |
| train loss   | 0.04        |
| test loss   | 0.05        |

### Проблемы и решение

### Итоги

## Обзор способов решения задачи

