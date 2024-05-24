Контекст приложения - то, какой способ общ с пользователем мы используем (graphql, http, rpc, ...)

#### ArgumentsHost
ArgumentsHost - класс, предоставляющий методы для получения переданных в хэндлер аргументов. Он позволяет определить механизм для доставания
этих аргументов (http, sockets, graphql, microservices, ...)

Для того, чтобы определить контекст нашего приложения, можно использовать метод ArgumentsHost.getType()

Чтобы получить аргументы, есть ArgumentsHost.getArgs()
Можно сделать более надёжно и переключить объект контекста на конкретный интерфейс:
```
const ctx = host.switchToHttp();
const request = ctx.getRequest<Request>();
```

#### ExecutionContext
ExecutionContext расширяет класс ArgumentsHost, добавляя в него новую функциональность.

В нём, помимо методов ArgsHost, есть ещё следующие:
- getClass - Возвращает тип класса, к которому принадлежит текущий контроллер
- getHandler - возвращает ссылку на хэндлер, который будет вызван при вызове next() реквеста

#### Reflector - может быть использован, чтобы добавить метаданные к хэндлеру (или контроллеру) или получить их.
```
@SetMetadata() // setMetadata works, but its better to create own decorators with Reflector
// .......
const roles = this.reflector.get(Roles, context.getHandler());
```
