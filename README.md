Matching.

Matching - одна из базовых задач машинного обучения, которая встречается в информационном поиске, компьютерном зрении, рекомендательных системах и др.

Задача.

- разработать алгоритм, который для всех товаров из validation.csv предложит несколько вариантов наиболее похожих товаров из base;
- оценить качество алгоритма по метрике accuracy@5.

Данные: источник

base.csv - анонимизированный набор товаров. Каждый товар представлен как уникальный id (0-base, 1-base, 2-base) и вектор признаков размерностью 72.

train.csv - обучающий датасет. Каждая строчка - один товар, для которого известен уникальный id (0-query, 1-query, …) , вектор признаков И id товара из base.csv, который максимально похож на него (по мнению экспертов).

validation.csv - датасет с товарами (уникальный id и вектор признаков), для которых надо найти наиболее близкие товары из base.csv

validation_answer.csv - правильные ответы к предыдущему файлу

Вывод.

Исходные данные имеют хорошее качество. Тип данных - соответствует. Пропуски, дубликаты- отсутствуют. 8 признаков содержат выбросы, на основании теста Шапиро–Уилка данные признаки были удалены. Метрика улучшилась после удаления. 

Поскольку значения признаков сильно отличаются друг от друга все признаки подверглись маштабированию с помощью StandardScaler().

Поиск подходящего количества кластеров выдал: 100 кластеров, поиск по 50 соседним. На таких данных метрика себя показала лучшим образом 71% .

Итоговое значение метрики на валидационной выборке показало 70.9%


Matching.

Matching is one of the basic machine learning tasks found in information retrieval, computer vision, recommender systems, and more.

Task.

    To develop an algorithm that for all products from validation.csv will suggest several variants of the most similar products from base;
    Evaluate the quality of the algorithm by the accuracy@5 metric.

Data: source

base.csv is an anonymized set of goods. Each product is represented as a unique id (0-base, 1-base, 2-base) and a feature vector of dimensionality 72.

train.csv - training dataset. Each line - one product for which the unique id (0-query, 1-query, ...), vector of features AND the id of the product from base.csv, which is maximally similar to it (according to experts) is known.

validation.csv - dataset with goods (unique id and vector of attributes), for which it is necessary to find the closest goods from base.csv.

validation_answer.csv - correct answers to the previous file.

Conclusion.

The source data is of good quality. The data type is consistent. There are no omissions, duplicates. 8 features contain outliers, based on Shapiro-Wilk test these features were removed. The metric improved after removal.

Since the feature values are very different from each other all features were mashable using StandardScaler().

A search for the appropriate number of clusters yielded: 100 clusters, searching through 50 neighboring clusters. On such data the metric showed the best 71%.

The final value of the metric on the validation sample showed 70.9%
