Чтобы использовать:
```
{  "compilerOptions": {    "experimentalDecorators": false,  }
```

Пример:
```
function debugMethod(
    originalMethod: any,
    context: ClassMethodDecoratorContext
) {
    const methodName = String(context.name);
    function replacementMethod(this: any, ...args: any[]) {
        console.log(`'${methodName}' Execution Starts.`);
        const result = originalMethod.call(this, ...args);
        console.log(`'${methodName}' Execution Ends.`);
        return result;
    }
    return replacementMethod;

}
```