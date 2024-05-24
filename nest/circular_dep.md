Циркулярная зависимость - когда два класса зависят друг от друга.

В несте можно зарезолвить её двумя способами

#### forward reference
Можно зависеть от класса, который ещё не создан, при помощи
```
constructor(
    @Inject(forwardRef(() => CatsService))
    private catsService: CatsService,
) {}
```
Просто ставим такой inject в обоих классах.

#### ModuleRef
Использовать ModuleRef