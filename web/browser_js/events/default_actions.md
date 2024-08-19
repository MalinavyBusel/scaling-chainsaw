В браузере есть обработчики событий, существующие по умолчанию. К примеру, переход по ссылке
при нажатии на неё.

Чтобы отменить вызов таких обработчиков, нужно вызвать на объекте event метод
preventDefault

### passive: true
В некоторых ситуациях бывает полезно передать в обработчик опцию passive: true.
Это скажет браузеру, что событие по умолчанию не будет отменено, и в некоторых ситуациях
позволит ему сразу начать обработку, увеличив плавность и начав обработку события параллельно

### defaultPrevented
event.defaultPrevented показывает, было ли предотвращено действие по умолчанию

### default actions
Список самых частых действий по умолчанию:
 - mousedown – начинает выделять текст (если двигать мышкой).
 - click на <input type="checkbox"> – ставит или убирает галочку в input.
 - submit – при нажатии на <input type="submit"> или при нажатии клавиши Enter в форме данные отправляются на сервер.
 - keydown – при нажатии клавиши в поле ввода появляется символ.
 - contextmenu – при правом клике показывается контекстное меню браузера.