### video
\<video> - отображает на странице видео

```html
\<video width="320" height="240" controls autoplay muted>\
   \<source src="movie.mp4" type="video/mp4">\
   \<source src="movie.ogg" type="video/ogg">\
Your browser does not support the video tag.\
\</video>
```

controls - добавляет кнопки управления\
autoplay - начинает проигрывать видео сразу при загрузке страницы\
muted - видео изначально без звука\
source - позволяет браузеру выбрать удобный для него источник

### audio
\<audio>
формат и параметры те же, что и у видео, кроме размера

### object
\<object> - используется для доавления на страницу различных плагинов.
Или для другого html

### embed
как и object

### youtube video
\<iframe> тэг, содержащий ссылку на видос по id ("https://www.youtube.com/embed/tgbNymZ7vqY").
Там нет нужных параметров, поэтому autoplay, controls и mute добавляются как параметры
в конец адресной строки видео
