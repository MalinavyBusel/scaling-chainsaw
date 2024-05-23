### WeakMap
В отличие от Map, здесь ключи - это только объекты, а не примитивы. В ней нет .values(), .keys(), .entries() и перебора.
Также, в отличие от обычной мапы, если на объект ссылается только эта мапа, а других ссылок на него нет, то он может быть
удалён сборщиком мусора.
Часто используют как хранилище доп данных для объекта, которое живо, пока жив сам объект. Ну или для кеширования
```
weakMap.set(john, "секретные документы");
// если john умрёт (будет удалён сборщиком мусора), "секретные документы" будут автоматически уничтожены
```
После того, как объект john стал недостижим другими способами,
кроме как через WeakMap, он удаляется из памяти вместе с информацией по такому ключу из WeakMap.

### WeakSet
Поддерживает только объекты в качестве ключей. Не перебираема, нет size, keys().
Принцип работы схож с WeakMap.