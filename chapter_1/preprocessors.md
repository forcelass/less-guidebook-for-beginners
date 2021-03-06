# Препроцессоры

Пожалуй, начнём с определения:

**Препроцессор** (от англ. Preprocessor) — это инструмент, преобразующий код из одного синтаксиса в другой. Обычно, на вход препроцессора поступает код, написанный с использованием синтаксических конструкций, понятных этому препроцессору.

Стоит сказать, что препроцессор может полностью замещать синтаксические конструкции языка или частично расширять их, то есть добавлять новые конструкции. Так как препроцессор преобразует код, то помимо входа у него должен быть и выход. Иначе какой смысл в его работе, ведь другие программы не смогут воспользоваться его трудами.

Как правило, на выходе ожидается код с более низким уровнем. То есть код, лишённый синтаксических конструкций, вносимых препроцессором. Сейчас нам не важно, что происходит с такими конструкциями, допустим, что препроцессор их раскрывает или удаляет в соответствии с заложенными в него правилами. Иначе говоря, на выходе мы получаем код, понятный программе, которая будет использовать его после препроцессора.



### Пример

Рассмотрим работу препроцессора на простейшем примере. Условия задачи у нас будут такими:

> Пусть на вход препроцессора поступает строка, включающая в себя последовательность слов, разделённых пробелами, запятыми и точками. Основная функция препроцессора — замена ключевого слова «.CSS.» на его полную форму записи «Cascading Style Sheets». На выходе препроцессора имеем преобразованную строку.

Итак, исходя из условий мы понимаем, что «.CSS.» — это синтаксическая конструкция, которую должен обработать препроцессор.

Допустим, что на вход была подана следующая строка:

```
Developers use CSS preprocessors to build .CSS. faster.
```

Как мы видим, в этой строке два раза встречается слово «CSS». В первом случае это будет обычным словом как, например, «use» или «build», а во втором — синтаксической конструкцией препроцессора.

Далее препроцессор преобразует строку в соответствии с заложенным в него функционалом, и, в зависимости от настроек, на выходе имеется преобразованная строка.


```
Developers use CSS preprocessors to build Cascading Style Sheets faster.
```

Так работают препроцессоры в самом примитивном случае. В больших проектах все куда сложнее.



### Некоторые понятия

Кстати, для того, чтобы понимать некоторые статьи и книги, нужно запомнить, что вместо слова «преобразует», могут использоваться слова «компилирует» и «транслирует».

Если вы ничего не поняли из этой части главы, не расстраивайтесь — это нормально. Понимание придёт к вам на следующей странице. Конечно, при желании.
