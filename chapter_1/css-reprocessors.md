# CSS-препроцессоры

Если рассматривать препроцессоры вместе с CSS, то получается картина более понятная, нежели чем рассматривать понятие препроцессора отдельно.




## Определение

**CSS препроцессор** (от англ. CSS preprocessor) — это надстройка над CSS, которая добавляет ранее недоступные возможности для CSS, с помощью новых синтаксических конструкций.

Основная задача препроцессора — это предоставление удобных синтаксических конструкций для разработчика, чтобы упростить, и тем самым, ускорить разработку и поддержу стилей в проектах.

CSS препроцессоры преобразуют код, написанный с использованием препроцессорного языка, в чистый и валидный CSS-код.

При помощи препроцессоров вы можете писать код, который нацелен на:

 * Читабельность для человека
 * Структурированность и логичность
 * Производительность

И это лишь малая часть того, что может дать вам препроцессор. Но не стоит забегать вперёд.




## Синтаксический сахар

Перед тем, как перейти к дальнейшему рассмотрению CSS-препроцесоров, давайте обновим наш лексикон новым понятием — «синтаксический сахар».

**Синтаксический сахар** (от англ. syntactic sugar) — это дополнения синтаксиса языка программирования, которые не вносят каких-то существенных изменений или новых возможностей, но делают этот язык более читабельным для человека.

Синтаксический сахар вводит в язык альтернативные варианты записи заложенных в этот язык конструкций. Под альтернативными вариантами записи стоит понимать более короткие или удобные конструкции для человека, которые в конечном итоге будут преобразовываться препроцессором в исходный язык, без синтаксического сахара.

Если попытаться применить это понятие к CSS-препроцессорам, то оно, в общем случае, полностью описывает их суть. Ещё раз напомню, что основной задачей препроцессоров является упрощение и ускорение разработки, а как это ещё можно сделать, если не ввести альтернативные варианты записи?




## Какие бывают CSS-препроцессоры?

Пора перейти к более конкретным примерам, а именно к самим CSS-препроцессорам. На момент написания книги можно выделить три популярных препроцессора:

 * Less
 * Sass (SCSS)
 * Stylus

И несколько незначительных для нас игроков:

 * Closure Stylesheets
 * CSS Crush

О первой тройке мы поговорим отдельно немногим ниже, а вот о двух последних разговора вообще не будет, в виду их непопулярности. При желании, описания этих препроцессоров с лёгкостью можно найти в поисковике.




## Какой смысл использования препроцессоров?

Как я уже отметил выше, основные плюсы — это читабельность кода, структурирование и повышение производительности.

Существуют также и другие причины того, чтобы начать использовать препроцессор уже сегодня. Я хочу заострить на этом внимание, так как разработчики раньше, да многие и сейчас, отнекиваются от использования препроцессоров, находя их сложными, непонятными и ненужными.


#### CSS — это сложно

Стандартный CSS — это сложно. Синтаксис без использования вложенности, которую предлагают CSS-препроцессоры, просто напросто сложен для зрительного восприятия. Кроме того, нужно помнить имя родителя при вложенности. Отсутствие нормальных переменных и «функций» делает CSS-код грязным и узконаправленным.


#### Доступная документация

Прошли те времена, когда документация от препроцессоров была доступна только людям «в теме». Сейчас любой желающий может в кратчайшие сроки освоить любой из препроцессоров, причём с минимальными затратами сил.


#### Простота использования

Использовать препроцессоры стало проще, чем раньше, причём намного проще. Для этого нужно лишь установить программу, которая будет следить за файлами, предназначенными для препроцессора, и при их изменении будет компилировать содержимое этих файлов в чистый CSS-код.

Для более продвинутых пользователей есть специальные сборщики проектов. Не думайте, что если вы используете программу для препроцессоров, а не сборщик проектов, то вы недостаточно круты. На самом деле, такие сборщики предлагают полный контроль и расширенные настройки, а не делают из вас джедая.


#### Структура и логичность кода

Самым популярным предлагаемым функционалом любого CSS-препроцессора является возможность вкладывать селекторы друг в друга. Я не буду сейчас приводить пример, так как о возможностях Less, включая вложенность, будет написана соответствующая часть книги. На этом этапе вам стоит знать лишь то, что при использовании препроцессоров, можно вкладывать один селектор в другой, а другой в третий, получая что-то, похожее на оглавление книги:

```
1. Родительский селектор
  1.1. Вложенный селектор
  1.2. Вложенный селектор
    1.2.1. Вложенный селектор
  1.3. Вложенный селектор
```

Конечно, в реальной жизни селекторы не могут начинаться с цифр, однако, для проведения параллели между вложенностью и оглавлением, думаю такое упущение здесь уместно.


#### Примеси

Если говорить совсем кратко, то, используя **примеси** (от англ. Mixins), можно сделать код переиспользуемым. Это помогает избежать вспомогательных классов в разметке или дублирования свойств от селектора к селектору.


#### Модульность

Еще одним бонусом, который прямо сейчас уговорил бы меня начать пользоваться CSS-препроцессором, будет возможность вкладывать файлы в файлы, то есть проще говоря, производить конкатенацию файлов в заданной последовательности. Да, это можно организовать и на чистом CSS, но вкупе с другими возможностями получается очень мощный инструмент.

При этом мы получаем возможность делиться модулями (библиотеками примесей), которые создали для своих нужд и посчитали полезными для других людей. Получается, что любой разработчик может загрузить вашу библиотеку и использовать её в своих целях, вызывая по мере необходимости написанные вами примеси.




## Почему бы не подождать развития CSS?

Развитие CSS идёт очень маленькими и неуверенными шагами, так как W3C придерживается приоритета скорости срабатывания CSS (производительности). С одной стороны это правильно и очень важно, но с другой — это отсутствие удобства для разработчиков.

В пример поставлю одну из спецификаций CSS4, которую ввели под давлением разработчиков — селектор по родителю. Столь долгий путь от идеи до принятия решения был из-за того, что W3C считало такой селектор медленным и дальнейшее его использование на сайтах привело бы к диким тормозам. Конечно же, речь идёт о повсеместном применении этого селектора, а не о единичных случаях.

Так что не стоит ждать в ближайшее время революций и изменений, способных затмить функционал и возможности CSS-препроцесоров.




## Разновидности препроцессоров

Разумеется, как и в любой другой области, всегда есть конкуренция, и на рынке препроцессоров сейчас три главных, враждующих между собой лагеря:

 * Less
 * Sass (SCSS)
 * Stylus

Враждующими я их называю, потому что каждый приверженец одного из препроцессоров считает своим долгом поливать нечистотами представителей других, скажем так, конфессий. Такая неприязнь особенно часто проявляется у любителей препроцессора Sass, который считается старейшим и мощнейшим из всех трёх препроцессоров.

Для полной картины, я хочу привести краткую справку по каждому препроцессору:


#### Less

Собственно, герой этой книги. Самый популярный на момент написания книги препроцессор. Основан в 2009 году Алексис Сельер (Alexis Sellier) и написан на JavaScript (изначально был написан на Ruby, но Алексис вовремя сделал правильный шаг). Имеет все базовые возможности препроцессоров и даже больше, но не имеет условных конструкций и циклов в привычном для нас понимании. Основным плюсом является его простота, практически стандартный для CSS синтаксис и возможность расширения функционала за счёт системы плагинов.


#### Sass (SCSS)

Самый мощный из CSS-препроцессоров. Имеет довольно большое сообщество разработчиков. Основан в 2007 году как модуль для HAML и написан на Ruby (есть порт на C++). Имеет куда больший ассортимент возможностей в сравнении с Less. Возможности самого препроцессора расширяются за счёт многофункциональной библиотеки Compass, которая позволяет выйти за рамки CSS и работать, например, со спрайтами в автоматическом режиме.

Имеет два синтаксиса:

 * Sass (Syntactically Awesome Style Sheets) — упрощённый синтаксис CSS,
который основан на идентации. Считается устаревшим.
 * SCSS (Sassy CSS) — основан на стандартном для CSS синтаксисе.


#### Stylus

Самый молодой, но в тоже время самый перспективный CSS-препроцессор. Основан в 2010 году небезызвестной в наших кругах личностью TJ Holowaychuk. Говорят, это самый удобный и расширяемый препроцессор, а ещё он гибче Sass. Написан на JavaScript. Поддерживает уйму вариантов синтаксиса от подобного CSS до упрощённого (отсутствуют `:`, `;`, `{}` и некоторые скобки).
