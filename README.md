# summarizationRussianNews

# Автоматическая суммаризация новостей на русском языке

Набор данных доступен по ссылке: https://www.kaggle.com/datasets/yutkin/corpus-of-russian-news-articles-from-lenta

В данной работе была проведена предобработка набора данных, получены базовые версии заголовков с помощью алгоритма
LexRank, дообучена модель mBart для генерации новостных заголовков на русском языке. Было показано, что при
небольшой обработке входных данных, модель способна выдавать высокое качество на русском языке в задаче 
суммаризации.

## Результаты обучения модели

|       | Rouge-1| Rouge-2 | Rouge-L |
|-------|--------|---------|---------|
|LexRank| 12.9408 | 3.9882 | 11.9508 |
|mBart  | 35.9931 | 18.6076| 34.1661 |

## Примеры оригинальных и сгенерированных заголовков

|Оригинальный заголовок | Сгенерированный заголовок |
|-----------------------|---------------------------|
|бабочку хофштадтера впервые «поймали» вне магнитного поля | бабочку хофштадтера впервые продемонстрировали в магнитном поле |
|youtube занялся гражданской журналистикой | youtube запустил сервис видеохостинга для сми |
|минздрав пообещал заменить импортные лекарства безболезненно для пациентов | минздрав рассказал о внедрении новой методики перевода пациентов с зарубежных лекарств на российские аналоги |
|конгресс дал обаме денег на войны и борьбу с гриппом | американские законодатели одобрили экстренные бюджетные расходы на борьбу с эпидемией гриппа |
