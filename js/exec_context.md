Контекст исполнения - окружение, сделанное движком для выполнения кода. Есть два вида - глобальный (один на программу) и контекст функции (их может быть много). Все контексты помещаются в стек (глобальный контекст тоже)

Состоит из двух фаз - создание и исполнение. На первой выделяется память и настраиваются цепочки областей видимости. На второй исполняется сам код.

Каждый контекст состоит из двух частей - памяти и кода.

При создании контекста жс проходит по всему коду и выделяет память под переменные. Для let и const создается LexicalEnvironment, а для var VariableEnvironment.
В это время и происходит всплытие - на этапе создания все переменные создаются как undefined (или uninitialized в let и const), а на фазе кода уже получают свои значения. Также в это время задается this.