Lexical scoping


Каждый раз, когда жс создаёь контекст исполнения (из которых состоит стек исполнения), кроме того он создает лексическое окружение - структуру данных, хранящую идентификаторы переменных.

У лексического окружения есть два компонента:
- запись в окружении (environment record) - в нем хранятся объявления переменной?
- ссылка не внешнее лексическое окружение
```
lexicalEnvironment = {  
environmentRecord: {  
    <identifier> : <value>,  
    <identifier> : <value>  
}  
outer: < Reference to the parent lexical environment>  
}
```

Когда функция выполняется, её контекст выполнения удаляется из стека, но её лексическое окружение может или не может быть удалено из памяти, в зависимости от того, ссылается ли на это лексическое окружение другое лексическое окружение. **Так работают замыкания**. Когда в текущем окружении нет такой переменной, язык ищет её во внешней.

Стоит отметить, что доступ имеем только к родительскому окружению. **Если вызываем не в родительском, а в окружении А, то к окружению А доступа не будет, тк при создании мы уже записали другой родительский scope. **
```
var incrementUntil = function(max) { 
    if(num >= max) return num 
    num++
    incrementUntil(max)
}

num = 0
var myFun2 = function() { 
    var num = -1
    incrementUntil(3) // has the outer scope of global
return num 
}

myFun2() //> -1 
num //> 3
```

Замыкание и принцип работы окружений часто используется для создания ф-й с частичным применением:
```
var incrementUntil = function(max) {
    var inc = function(num) { 
        if(num >= max) return num 
        return inc(num+1)
    }
    return (num) => inc(num) // returns another function
}

incrementUntil(4)(1) //> 4
incrementUntil(8)(3) //> 8
```