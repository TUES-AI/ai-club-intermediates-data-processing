# TUES AI Club · Data Processing (9.–12. клас / Intermediates)

Практически материали за обработка на данни за ученици от 9.–12. клас. Това е **първата от две лекции**: разбиране на данните и първоначални проверки, без обучение на модел.

## Лекция 1: NumPy, pandas и първи поглед върху Heart Disease Dataset

📓 [Отвори notebook-а в Google Colab](https://colab.research.google.com/github/TUES-AI/ai-club-intermediates-data-processing/blob/main/01-heart-disease/TUES_AI_Club_Heart_Disease_Intro.ipynb) · [Изтегли notebook-а](01-heart-disease/TUES_AI_Club_Heart_Disease_Intro.ipynb)

**Какво ще правим:** малки масиви в NumPy → четене на оригиналния processed Cleveland набор с pandas → DataFrame, Series и филтри → липси, дубликати и категории → target, класове и графики. Следват упражнения; решенията са в края на notebook-а. Нужни са само основите на Python. Материалът не е медицински съвет.

### Стартиране в Colab

Отвори връзката по-горе и избери **Runtime → Run all**. При първото изпълнение е необходим интернет за данните от UCI. Ако Colab вече разполага с `processed.cleveland.data` в `/content`, notebook-ът ползва локалния файл. Средата на Colab е временна: за следваща **офлайн** сесия качи и [CSV файла](01-heart-disease/processed.cleveland.data) в `/content`.

### Стартиране локално

Клонирай репото, инсталирай зависимостите и отвори notebook-а в Jupyter:

```bash
git clone https://github.com/TUES-AI/ai-club-intermediates-data-processing.git
cd ai-club-intermediates-data-processing
python -m pip install -r requirements.txt
jupyter notebook
```

Отвори `01-heart-disease/TUES_AI_Club_Heart_Disease_Intro.ipynb` и избери **Run All Cells**. Notebook-ът и `processed.cleveland.data` са в една папка: локално работят **и без интернет**. Ако CSV файлът липсва, notebook-ът ще се опита да го изтегли от UCI и да запази копие след проверка. Не променяй оригиналния файл за упражненията.

## Следваща лекция

Предстоят попълване на липси, encoding и scaling. Когато се работи с тренировъчни и тестови данни, параметрите на трансформациите се научават **само от тренировъчните данни**, за да няма data leakage. В това репо засега е публикувана само лекция 1.

## Данни и признание

Използваме **оригиналния** [UCI Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease), по-конкретно [processed.cleveland.data](https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/processed.cleveland.data). Обясненията за колоните са сверени и с [heart-disease.names](https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/heart-disease.names). Няма смесване с преработени Kaggle версии.

**Цитиране:** Janosi, A., Steinbrunn, W., Pfisterer, M., & Detrano, R. (1989). *Heart Disease* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C52P4X

Наборът е предоставен от UCI под [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Копието на CSV файла тук е непроменено; посочваме авторите и източника. Notebook-ът е учебен материал, не инструмент за диагностика.
