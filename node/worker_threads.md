Кроме задач, что блокают eventloop ожиданием, есть также задачи, блокирующие eventloop высокой нагрузкой на
процессор, которые тоже заставляют простаивать. Чтобы этого не было, в ноде есть worker threads - потоки,
которые создаются главным потоком ноды и выполняют эти сложные задачи. Они используют часть памяти родительского
процесса, в связи с чем создать их проще и быстрее, чем новый процесс (не нужно просить память).

При старте главного процесса создается также главный поток, в котором крутится нода, v8 и libuv.
При создании новых рабочих потоков у них есть свой инстанс v8 (поэтому свои память и микрозадачи, недоступные другим),
а также свой libuv с eventloop-ом и инстанс ноды.

Каждый воркер связан с родительским при помощи канала сообщений. Сообщения бывают следующие:
- message - когда воркер отправляет сообщение
- error - когда рабочий выкидывает непойманную ошибку
- exit - когда рабочий завершает работу
- online - когда рабочий инитнулся и начал работать

Кроме сообщений могут также отсылать друг другу данные с помощбю месседжей (в обе стороны)