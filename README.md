# 18-21
# Вместо предисловия
Копал несколько часов в инете по данным вопросам, просмотрел достаточное количество статей, но вынужден признать, что книга параллельное программирование отвечает на данные вопросы наиболее полно. В лекциях Бородина эти вопросы также только упоминаются.
# Пул потоков

Итак если кратко, то простейший пул потоков представляет из себя потокобезопасную очередь потоков, каждый из которых запускается в конструкторе и затем выполняет некоторую функцию. В коде важен порядок объявления: флаг и объект должны быть объявлены до вектора потоков, который должен быть объявлен ранее joinera.
Страница 383 из параллельного программирования

Но данный пул потоков не поддерживает многие функции такие как ожидание задачи или предотвращение конкуренции потоков. Усложненные варианты написаны в следующих пунктах. Их можно посмотреть по диагонали, но чтобы разобраться потребуется несколько часов, поэтому запоминайте, что пул из листинга 9.1 очень не идеален, но реализация всех этих функций займет ОЧЕНЬ МНОГО времени
# Потокобезопасные стуктуры данных с блокировками
Для ответа на данный вопрос рекомендуется прочитать главу 6 (6.1, 6.2 полностью прочитать и понять, 6.3 наискось и на будущее запомнить, что такое тоже бывает)

# Реализация потокобезопасной очереди с блокировкой.
В этих пунктах на мой взгляд все довольно просто
читаем пункт 6.2.1 если на словах "скопируем код из главы 3" вы ипытываете ненависть, то возвращаемся и читаем страницы 81-83, начиная с листинга 3.5
# Реализация потокобезопасного стека с блокировкой.
пункт 6.2.2 нас интересует листинг 6.3 на странице 229 и все комментарии ниже до пункта 6.2.3. Если код в принципе понятен, но непонятны логические решения, то читаем данный пункт сначала(итоговый код это результат усовершенствования листингов 6.1 и 6.2) если вообще код не понятен, то смотри страницу 119 листинг 4.5 и раньше(хотя после разбора стека там особо новых логических ходов нет)
