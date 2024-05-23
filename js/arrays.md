Могут изменять длину и хранить смесь различных типов данных

В массивах могут храниться так называемые пустые значения - не проинициализированные значения, которые не являются undefined.\
К примеру:\
```
const a = Array(5); // [ <5 empty items> ]
// Consecutive commas in array literal:
const b = [1, 2, , , 5]; // [ 1, 2, <2 empty items>, 5 ]
```
Иногда они ведут себя как undefined, иногда просто скипаются


### Методы
Все методы, которые возвращают новый массив, используют неглубокую копию, то есть если есть вложенность, то копируется только первый слой.
Те методы, которые возвращают новый массив, это map, filter, slice, те, которые начинаются на to и ?другие.

##### .concat()
соединяет два массива

#####  .every()
возвращает true, если все элементы подходят под условие

##### .some()
возвращает true, если хоть один элемент подходит под условие

##### .fill()
делает все элементы от x до y равными z

##### find() findLast()
возвращает первый (последний) элемент, подходящий под условие, или undefined

##### findIndex() findLastIndex()
возвращает индекс первого элемента под условие, или же -1

##### includes()

##### indexOf() lastIndexOf

##### join(separator)
соединяет всё в строку

##### pop()
убирает последний элемент и возвращает его

##### push()

##### shift()
убирает первый элемент и возвращает его

##### slice()
возвращает неглубокую копию массива начиная с элемента а и заканчивая элементом b

##### splice & toSpliced
убирает, добавляет или заменяет элементы в произвольном месте массива. splice меняет текущий, toSpliced возвращает новый

##### with
возвращает новый массив с замененным значением указанного индекса. может принимать негативные индексы.