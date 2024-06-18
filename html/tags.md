### a
ссылка. главный атрибут - href. Можно выбрать, где открыть,
при помощи атрибута target

### img
изображение. атрибуты - src, alt, width, height. Вместо width & height
лучше использовать style, желательно всегда ставить ширину и длину

### picture
как img, но разные картинки под разные типы девайсов

### pre
как и \<p\>, но сохраняет пробелы и переходы на новую строку

### br
linebreak

### hr
horizontal rule

### h
1 - 6 по приоритету. Желательно использовать только для заголовков, а не для форматирования,
тк поисковик опирается на эти теги. Если нужен шрифт ещё больше, нужно использовать
font-size атрибута style

### p
параграф с текстом

### div
Содержит блок других тэгов

Расположить div-ы горизонтально можно при помощи атрибута стилей float или display,
а также flex и grid (тоже как часть display)

### script
содержит в себе js-код, выполняемый на клиенте

### span
контейнер для текста. Используется для форматирования и пр

### table
состоит из дочерних тэгов и создаёт табличку

### html
главный тэг. желательно добавлять атрибут lang

### meta
Определяет не видимую пользователю мета-информацию, такую как:
 -  charset
 -  ключевые слова
 -  описание
 -  как часто обновлять страницу
 -  viewport

### favicon
\<link rel="icon" type="image/x-icon" href="/images/favicon.ico">

### list
ul - unordered\
ol - ordered\
dl - list with descriptions

### text formatting tags
\<b\> - Bold text\
\<strong\> - Important text\
\<i> - Italic text\
\<em> - Emphasized text - как и italic, но скрин-ридер читает его с выделением\
\<mark> - Marked text - выделен цветом\
\<small> - Smaller text\
\<del> - Deleted text\
\<ins> - Inserted text\
\<sub> - Subscript text - внизу и уменьшен\
\<sup> - Superscript text - вверху и уменьшен\
\<blockquote>\</\> - цитата в отдельном блоке\
\<quote> - строчная цитата

### comment
\<!-- some comment --\>