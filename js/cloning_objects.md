1. Object.assign
Берет сразу с нескольких источников. КЛОНИТ ТОЛЬКО 1-й УРОВЕНЬ, т.е. shallow copy

2. Spread
КЛОНИТ ТОЛЬКО 1-й УРОВЕНЬ, т.е. shallow copy

3. Json.stringify
Json.stringify & json.parse - жсон парсит не все типы данных, к тому же может портить точность чисел, и переводит
4. даты в строки

4. structuredClone\
Встроенный метод.\
Клонит:
   - бесконечную вложенность
   - циркулярные ссылки
   - большинство типов
   - transferable objects
      
   
Не клонит:
   - ф-и
   - части DOM
   - геттеры и сеттеры
   - прототипы объекта
```
class MyClass { 
   foo = 'bar' 
   myMethod() { /* ... */ }
}
const myClass = new MyClass()

const cloned = structuredClone(myClass)
// Becomes: { foo: 'bar' }

cloned instanceof myClass // false
```
