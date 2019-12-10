# ТОП 10 возможностей ускорить работу программиста в VS Code


Visual Studio Code (его ещё называют VS Code и VSCode) — это экономичный но мощный кросс-платформенный редактор кода, выполненный в виде настольного приложения. VS Code поддерживает множество инструментов разработки — вроде TypeScript и отладчика Chrome. Это, а также то, что к нему написано невероятное количество опенсорсных расширений, делает VS Code весьма популярным и любимым многими редактором.

Для меня понятия «работа» и «написание кода» — это одно и то же. И, по большому счёту, неважно, каким именно редактором я буду постоянно пользоваться. Но изменения — это всегда нелегко. После того, как я неделю поработал в VS Code, я обнаружил, что моя продуктивность сильно просела. Я сделал за это время меньше, чем сделал бы, пользуйся я чем-то привычным.

Это было так, отчасти, из-за того, что мне нужно было перестроиться, привыкнуть к новым инструментам. Нужно было выяснить то, какие команды мне пригодятся, нужно было запомнить полезные сочетания клавиш, изучить средства навигации по коду. И, вдобавок, надо было разобраться в том,какие расширения редактора мне понадобится установить для того, чтобы облегчить себе жизнь.

В итоге я снова вышел на высокую производительность. Вряд ли я снова затею переход на новый редактор. VS Code — это надёжный и нетребовательный к ресурсам инструмент. Вокруг него собралось мощное сообщество разработчиков расширений. Пожалуй это — одна из лучших разработок Microsoft.

Вот 10 возможностей VS Code, освоение которых помогло мне ускорить работу. Надеюсь, они пригодятся и вам.


### 1. Сниппеты

Расширение Project Snippets, мой фаворит на все времена, создано на основе встроенного в VS Code инструмента User Snippets. 

Если вы не знакомы с этой стандартной возможностью VS Code, то знайте, что она позволяет пользователю оформлять собственные фрагменты кода в виде так называемых сниппетов. Делается это для того, чтобы многократно использовать их в своих проектах. Что значит «многократно использовать»?

Рассмотрим пример. Предположим, вы обнаруживаете, что вам часто приходится писать один и тот же шаблонный код. Например — такой:

```import { useReducer } from 'react'
const initialState = {
  //
}
const reducer = (state, action) => {
  switch (action.type) {
    default:
      return state
  }
}
const useSomeHook = () => {
  const [state, dispatch] = useReducer(reducer, initialState)
  return {
    ...state,
  }
}
export default useSomeHook```

Подобный код можно оформить в виде сниппета. В результате, вместо того, чтобы вводить всё это с клавиатуры (или копировать откуда-нибудь), вам нужно будет лишь ввести так называемый префикс, после чего в редакторе появится код, соответствующий этому префиксу.

Если вы, в VS Code, перейдёте в меню File > Preferences > User Snippets, то вы, при желании, можете создать новый глобальный файл сниппетов, выбрав команду New Global Snippets File.

Например, для того чтобы создать новый файл сниппетов для React-проектов, в которых используется TypeScript, вы можете выбрать команду New Global Snippets File и задать имя файла как typescriptreact.json. В редакторе будет открыт только что созданный .json-файл, в котором можно будет описывать сниппеты.

Создадим сниппет на основе фрагмента вышеприведённого кода. Для этого файл typescriptreact.json нужно привести к следующему виду:


### 2. IntelliSense

IntelliSense — это система автозавершения кода. Она весьма интеллектуальна, что выгодно отличает её от других подобных систем.

Об IntelliSense говорят, как об одном из основных средств VS Code, обеспечивающих высокую производительность труда. При этом многие, выбирающие VS Code, пользуются этой возможностью далеко не на полную мощность.

Если навести мышь на некий участок кода, IntelliSense покажет дополнительные сведения о типах и даст возможность добраться до сведений об источнике их описания. В то время как эта возможность может оказаться полезной при работе с незнакомыми сущностями, созданными другими людьми, основная ценность IntelliSense заключается в том, что эта система способна предсказывать действия программиста.

Когда программист, например, вводит имя объекта и ставит после него точку, появляется выпадающий список с перечнем методов этого объекта. По мере того, как вводятся всё больше и больше букв имени метода, система фильтрует список. На определённом этапе ввода имени метода можно, клавишами-стрелками, выбрать нужное имя из довольно короткого списка, и нажать Enter для его вставки в код. Если сразу непонятно — какой именно метод нужен в данный момент — тут же можно взглянуть и на документацию.


### 3. Интегрированный терминал

Наличие в VS Code интегрированного терминала может помочь экономить время за счёт того, что программисту не приходится постоянно переключаться между окнами терминала и редактора. Это ещё значит и то, что в ходе автоматического запуска проекта очень легко замечать ошибки, не прерывая при этом своего обычного рабочего процесса.

Для того чтобы открыть терминал, можно воспользоваться сочетанием клавиш CTRL + ` (обратная галочка).

Терминал открывается для корневой директории текущего рабочего пространства.

Для открытия ещё одного окна терминала можно воспользоваться комбинацией клавиш CTRL + SHIFT + ` (всё та же обратная галочка).


### 4. Просмотр мест использования сущностей и их определений, рефакторинг

При работе над большим проектом некий класс, метод или свойство могут быть использованы в огромном количестве мест. VS Code позволяет узнать о том, где именно используются подобные сущности, быстро и эффективно собирая соответствующий список и демонстрируя его пользователю.

Для того чтобы увидеть такой список, достаточно щёлкнуть правой кнопкой мыши по методу, функции, или по чему-нибудь ещё, и выбрать в появившемся меню команду Peek References. Того же эффекта можно добиться, выделив нужный участок, и, на Windows-компьютере, воспользовавшись сочетанием клавиш SHIFT + F12.

Команда Rename Symbol из того же меню позволяет переименовывать сущности. Это особенно полезно при рефакторинге, или тогда, когда оказывается, что имя чего-либо больше не соответствует его предназначению.


### 5. Средства форматирования кода и инструменты для управления техническим долгом

Форматирование кода может превратиться в настоящий кошмар. Тут, конечно, программисту могут помочь линтеры, но запускать их приходится за пределами редактора.

Средства для форматирования кода помогают ускорить процесс разработки и обеспечить определённый уровень единообразия кода. Это оказывается очень кстати для проектов, работой над которыми занимаются команды программистов, когда у каждого разработчика могут быть собственные представления о форматировании.

Средства форматирования кода часто основаны на определённых соглашениях. Они позволяет обеспечить единообразие оформления текстов программ. Например, речь идёт о правилах выравнивания кода, о расстановке скобок, и, в целом, о том, как выглядит код.

В то время как автоматическое форматирование способствует снижению количества споров, касающихся стиля текстов программ, и помогает улучшить внешний вид кода, оно никак не помогает избавляться от технического долга. Именно поэтому я рекомендую обратить внимание на расширение Tech Debt Tracker.



Средство для управления техническим долгом в действии (источник)

Tech Debt Tracker использует набор показателей для определения сложности кода и потенциального технического долга, который может быть связан с этим кодом. Данное расширение нацелено на JavaScript и TypeScript-код. Оно даёт разработчику рекомендации по поводу улучшения текстов программ и может помочь ему выработать у себя привычку писать чистый и читабельный код.


### 6. Клавиатурные сокращения

Каждый раз, когда программисту приходится убирать руки с клавиатуры, он теряет несколько секунд. Это удлиняет сроки работы над проектами. Хотя такие потери времени и могут показаться незначительными, надо отметить, что смены положения рук и переключения с клавиатуры на мышь может быть вполне достаточно для того, чтобы нарушить рабочий процесс и выдернуть человека из состояния потока.

Многие разработчики стремятся к тому, чтобы делать всё, что можно, с помощью клавиатуры. Просто потому, что это позволяет им работать быстрее.

Клавиатурные сокращения позволяют решать большинство задач только с помощью клавиатуры. Это означает, что меньше времени тратится на поиск нужных команд в меню, что помогает программисту быстрее достигать своих целей.

Панель клавиатурных сокращений можно посмотреть, воспользовавшись комбинацией клавиш CTRL + K + S.



Панель клавиатурных сокращений в VS Code

Если кому-то не хочется изучать совершенно новый набор «горячих клавиш», он может создать такой список сам или импортировать клавиатурные сокращения из других популярных редакторов. Возможности гибкой настройки клавиатурных сокращений позволяют тем, кто уже к чему-то привык, быстрее достичь высокой продуктивности работы в VS Code.

Здесь можно найти расширения, которые помогают настраивать клавиатурные сокращения в VS Code.


### 7. Дзен-режим

Кто не любит работать, не отвлекаясь ни на что постороннее? В дзен-режиме (zen mode) VS Code переводится в полноэкранный режим, из интерфейса исчезает всё, что может отвлечь от работы с кодом. Для перевода редактора в этот режим нужно выполнить особую последовательность действий. А именно, тут используется не сочетание клавиш, а скорее — последовательность сочетаний клавиш. Для того чтобы выяснить, как именно дзен-режим включается у вас — загляните в панель клавиатурных сокращений и поищите по слову zen.

В моём случае для включения дзен-режима используется следующая последовательность сочетания клавиш: сначала — CTRL + Z, и сразу после этого — K. То есть — для перехода в этот режим я сначала нажимаю клавиши CTRL + Z, отпускаю их, а потом нажимаю и отпускаю K. У вас это может выглядеть иначе. Например — как CTRL + K и Z.

Дзен-режим помогает поддерживать состояние потока, избавляя программиста от любых потенциальных отвлекающих факторов.


### 8. Git

Прямо из VS Code можно делать коммиты в Git-репозитории. Как оказалось, VS Code очень хорошо поддерживает Git. А именно, тут можно готовить к коммитам изменённые файлы, делать коммиты, откатывать изменения, делать комментарии. В общем — всё, что обычно делается средствами командной строки, можно сделать, не покидая редактора. Тут вам понадобится панель Source Control, открываемая соответствующей кнопкой, расположенной в левой части экрана. Например, для подготовки изменённого файла к коммиту можно воспользоваться кнопкой со знаком +, находящейся в верхней части этой панели. После этого можно вызвать контекстное меню этого файла и найти в нём дополнительные команды.

Хотя всё это можно сделать и в консоли, и воспользовавшись настольным приложением GitHub, возможность работать с Git, не покидая редактора, может помочь в повышении производительности труда программиста.

Тут, опять же, всё дело в сохранении состояния потока. Программист, работая с Git, не покидает привычной рабочей среды. Ему не нужно переключаться между терминалом и редактором, не нужно постоянно думать о том, что где находится. Всё, что нужно для решения различных задач, всегда у него под рукой.

Существуют расширения для VS Code, автоматизирующие разные аспекты работы с системами контроля версий. Например, расширение GitLens позволяет получать подробности о репозиториях. Скажем — о том, кто внёс какое изменение в код, о том, какие изменения подготовлены к коммиту, а какие — нет. Это расширение умеет аннотировать код, давая доступ к сведениям из системы контроля версий. Например — к таким, как время коммита и изменения, внесённые коммитом в проект. GitLens — это инструмент, который особенно полезен при командной работе над проектами.


### 9. Отладчик

В VS Code имеется отладчик, который позволяет запускать код и устанавливать в нём точки останова, указывая те места, в которых выполнение программы должно быть приостановлено. Это позволяет, не покидая редактора, отлаживать программы, анализируя их внутреннее состояние во время их выполнения.

Отладка — это нечто большее, нежели вывод сообщений в консоль инструментов разработчика Chrome. В ходе отладки можно узнавать о том, что происходит внутри программы и, в результате, обнаруживать и устранять источники самых разных проблем. Если у программиста, например, есть подозрения по поводу правильности работы некоей функции, он может, в ходе отладки, выполнить эту функцию в пошаговом режиме, исследуя в ходе этого процесса состояние программы.

Для того чтобы приступить к отладке программы, нужно открыть панель отладки. Для этого можно воспользоваться кнопкой Debug, которая находится в левой части окна программы.



Кнопка Debug и панель отладки

Для запуска отладки надо нажать на кнопку Start Debugging, которая находится в верхней части панели отладки. В ходе отладки можно работать с окном консоли, открываемом в нижней части окна программы.

По умолчанию VS Code использует для запуска отлаживаемого кода среду Node.js, но можно сделать так, чтобы для отладки использовался бы отладчик браузера Google Chrome. В целом, можно отметить, что отладка кода — это режим работы, в котором можно обнаружить источники проблем, которые очень непросто найти при обычном выполнении кода.


### 10. Совместная работа над проектами в режиме реального времени

Вам когда-нибудь доводилось редактировать в Google Docs документ вместе с кем-нибудь другим? Расширение Live Share даёт, в сущности, те же возможности, но в применении к работе над программами. Связь между теми, кто работает в таком режиме, устанавливается через учётные записи GitHub или Azure.

Возможность совместной работы над проектами в режиме реального времени может оказаться крайне полезной в командной разработке. Она позволяет быстрее устранять ошибки, помогает заниматься парным программированием и ускоряет разработку.
