### for ... in
Проходит по перечисляемым ключам **объекта** (св-вам), в том числе унаследованным от прототипа. Не следует использовать для прохода по массиву.
### for ... of
Проходит по итерируемому объекту (список, сет, мапа, но **не object**)
### Object.entries(obj)
Проходит по объекту и перечисляет его ключи и значения. **Не перечисляет унаследованные св-ва**.

### map
применяет ф-ю к каждому элементу и возвращает новый массив, возвращает **shallow copy** предыдущего, но измененную

### forEach
применяет ф-ю к каждому элементу, модифицирует существующий массив

### filter
отбирает элементы, подходящие по условию

### reduce
превращает массив в одно значение, что-то делая с каждым элементом поочередно