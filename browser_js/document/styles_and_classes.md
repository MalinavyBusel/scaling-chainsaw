Желательно всегда изменять вид элемента через изменение класса, а не через атрибут style

### Изменение класса
Чтобы изменить класс элемента, есть св-ва className & classList. Первое соответствует
атрибуту класс, и при его изменении заменяется вся строка с классами. Чтобы добавить или удалить отдельный
класс, следует использовать второе свойство. У него есть свои методы (add/remove, toggle, contains)

Если всё таки нужно использовать style, то все его значения в js записаны camelCase

### Сброс стиля
Чтобы вернуться к первоначальному состоянию св-ва, можно задать его пустой строкой

### Получение всего стиля
Св-во style показывает только стили, заданные в нём. Чтобы получить все стили элемента (с каскадом),
нужно использовать метод getComputedStyle (тем не менее, он возвращает не вычисленные значения, а окончательные, то есть применимо к данному устройству, в пикселях а не процентах и тд)
