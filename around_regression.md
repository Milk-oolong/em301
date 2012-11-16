1. Гипотеза должна быть сформулирована до обработки данных
2. Если H0 не отвергается, то это еще не означает, что она верна.
3. Хорошая практика:
поделить выборку заранее, ДО исследования, на части:
* для построения моделей
 * оценка нескольких моделей
 * отбор моделей
* оценка качества

Типичная ошибка --- решение о применении метода на основании теста.

### Пример 1.
Есть тест на равенство средних, среди предпосылок которого равенство дисперсий.

Ошибка:
1. Проверим, равны ли дисперсии.
2. Если дисперсии равны, то проверим равны ли средние с помощью теста

### Пример 2. 
Борьба с автокорреляцией/гетероскедастичностью по результатам теста.

Ошибка:
1. Протестируем наличие гетероскедастичности
2. Будем бороться с гетероскедастичностью, если тест сказал, что она есть.


### Пример 3.

Использование стратегии: построим регрессию и выкинем незначимые переменные

Эксперимент с кучей независимых регрессоров.

loop i=1..40
 series z$i=normal(0,1)
endloop

ols z1 z2 z3 ... z40

Сколько регрессоров в среднем будет значимо на 5%-ом уровне значимости?

Если H0 верна, то p-value имеет какое распределение?


### Пример 4.

Ошибка:
1. Протестировали нормальность остатков
2. Если гипотеза о нормальности отверглась, то используем бутстраповские стандартные ошибки




Стандартный подход
------------------

Истинна модель y_i=\b_1+\b_2x_i+\b_3z_i+\e_i (1)
Оценки МНК y_i=\b_1+\b_2x_i+\b_3z_i+\e_i обладают хорошими свойствами

1. Несмещенность (если X - константы или независимые случайные величины)
2. Состоятельность (если X - независимые случайные величины)
3. Эффективность (X - константы, ?)

Проблема.
Вряд ли реальность так просто устроена. Скорее всего ведь реальность лишь примерно описывается 
истинной моделью... Это приводит к следующему стилизованному факту:
### Если наблюдений слишком много, любая гипотеза H0 отвергается

В каком-то смысле парадокс: я заранее уверен, что H0 не верна, но я её зачем-то тестирую.


Но: статистическая значимость оценки коэффициента, не означает, что он важен!
Статистически значимым может быть и ОЧЕНЬ маленький коэффициент.


Оценки МНК с лишней переменной обладают довольно хорошими свойствами. 
1. Несмещенность
2. Состоятельность


Оценки МНК y_i=\b_1+\b_2x_i обладают плохими свойствами. Они смещены.


Наличие уравнения (1) не означает причинности!

С некоторыми нюансами подход обобщается на стационарные временные ряды. (...)

Подход "регрессия всегда прекрасна"
------------------------------

Наши наблюдения - независимые векторные случайные величины
Есть "теоретическая регрессия"

Пример. Теоретическая регрессия.


Регрессия всегда является состоятельной оценкой для теоретической регрессии.
На малых выборках состоятельность ничего не дает. Описательный характер регрессии.

Интерпретация t-статистик (?)

Если мы включили "не те" переменные --- ничего страшного!

Если совместное распределение нормальное --- наилучший линейный прогноз является
наилучшим

Байесовский подход
----------------

* Предполагаем некоторое распределение бет.
* Предполагаем истинность некоторой модели.
* Получаем условное распределение бет, при условии наших данных.

Если включили "не те" переменные --- условное распределение некорректное







Устойчивые альтернативы (параметрические)
--------------------

Квантильная регрессия
В частности, медианная регрессия
Модальная регрессия

LASSO
Ridge









