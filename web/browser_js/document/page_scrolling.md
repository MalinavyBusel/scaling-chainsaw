### Ширина и высота окна
можно взять св-ва clientWidth & clientHeight для document.documentElement

### Ширина и высота всего документа
берём максимум из всех:
```
let scrollHeight = Math.max(
  document.body.scrollHeight, document.documentElement.scrollHeight,
  document.body.offsetHeight, document.documentElement.offsetHeight,
  document.body.clientHeight, document.documentElement.clientHeight
);
```

### Положение прокрутки
window.pageXOffset/YOffset - показывают текущее положение полосы прокрутки

window.scrollBy(x, y) - изменяет прокрутку относительно текущей\
window.scrollTo(x, y) - изменяет прокрутку на абсолютные координаты\
elem.scrollIntoView() - прокручивает, чтобы элемент был вверху\
также туда можно передавать опции, в которых можно указать стиль прокрутки (smooth, instant, auto)

### запрет прокрутки
document.body.style.overflow = "hidden"
