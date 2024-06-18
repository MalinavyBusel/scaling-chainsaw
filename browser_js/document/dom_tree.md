Любой html элемент можно получить при помощи dom-дерева.
Все операции начинаются с объекта document. Самые верхние -
это document.body и document.documentElement (\<html>).

Если обращаться к элементу, который на момент выполнения скрипта ещё не создан
(к примеру, в head к body), то будет ошибка.

element.childNodes - все дочерние узлы данного (то есть прямые дети,
на первом уровне вложенности)\
firstChild - elem.childNodes\[0]
lastChild - elem.childNodes\[childNodes.length-1]
parentNode

childNodes - не массив, а коллекция, поэтому в нём не работают
методы массивов

elem.nextSibling - следующий (нижний) элемент одного уровня
elem.previousSibling - предыдущий (правый) элемент одного уровня

children, firstElementChild, lastElementChild, nextElementSibling, lastElementSibling -
то же самое, что выше, но только для тэгов (без комментов, текста и тд)

Для таблиц:
 - table.rows - коллекция строк \<tr> таблицы
 - table.caption/tHead/tFoot - ссылки на элементы таблицы caption, thead, tfoot
 - table.tBodies
 - tr.cells
 - tr.sectionRowIndex
 - tr.rowIndex
