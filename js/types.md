Всего 8 типов:
- примитивы - number, BigInt, string, symbol, boolean, null, undefined
- non-primitive - object и его дочерние (function, array, ...)

Примитивы сравниваются по значению, обьекты - по ссылке. Поэтому если сравнить два одинаковых объекта при помощи ==, будет false.
Поэтому нужно сравнивать с помощью json.stringify, lodash, util.isDeepStrictEqual

Всегда нужно использовать имена типов с маленькой буквы, тк которые с  большой - это не типы, это встроенные классы с методами.