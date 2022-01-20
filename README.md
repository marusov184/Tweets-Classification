# Проект для «Викишоп»

Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 

Требуется обучить модель классифицировать комментарии на позитивные и негативные. В вашем распоряжении набор данных с разметкой о токсичности правок.




**Описание данных**

Данные находятся в файле `toxic_comments.csv`. Столбец *text* в нём содержит текст комментария, а *toxic* — целевой признак.


## Вывод

Твитты были очищены от лишних символов, каждое слово твитта было приведено к своей начальной форме - лемме. Затем было проверено три модели с различными гипер параметрами: логистическая регрессия, дерево решений и градиентный бустинг. 

Лучшей моделью как по скорости, так и по качеству модели на тестовой выборке стала логистическая регрессия с параметрами max_iter=300 и С = 3.67. F1 на тестовой выборке составил 0.763.