#### Promise.all
Дожидается успешношо выполнения всех промисов. Если есть
отработавшие с ошибкой, то ошибка в catch будет обработана только первая,
остальные будут пропущены

```js
async function getPageData() {
    try {
        const [user, product] = await Promise.all([
            fetchUser(), fetchProduct()
        ])
    } catch (err) {
        // 🚩 this has a big problem...
    }
}
```

#### Promise.allSettled
возвращает список результатов. Результат - это:
   - статус (fulfilled or rejected)
   - value (only in fulfilled)
   - reason (only in rejected)

#### Promise.race
Из списка возвращает результат первого settled (не важно, fulfilled or rejected)

#### Promise.any
Возвращает результат первого fulfilled, если все упали - тогда rejected