# JavaScript

<details>
<summary>Содержание</summary>
 
 - [Регулярные выражения](#регулярные-выражения)
 - [Promises](#promises)
 - [Set, Map](#set-map)

 </details>

## Регулярные выражения

* Что такое регулярные выражения? Когда они могут быть полезны?
* Какие есть способы создания инстанса регулярного выражения?
* Что такое флаги? Зачем нужны? Какие бывают?
* Какие методы есть у инстансов регулярных выражений?
* Какие методы есть у строк, которые позволяют работать с регулярными выражениями?
* Что такое квантификаторы? Как работают квантификаторы `{}`, `?`, `*`, `+`?
  * Что такое жадные и ленивые квантификаторы?
* Что такое набор `[abc]` и диапазон `[a-c]` символов? Когда они могут быть полезны?
  * Что такое исключающий набор и диапазон?
* Для чего нужны спецсимволы `^`, `$`, `.`, `|`?
* Когда использовать экранирующий символ `\`?
* Что такое символьные классы? Как работают символьные классы `\w`, `\W`, `\d`, `\D`, `\s`, `\S`, `\b` `\B`?
  * Почему регулярное выражение `\babc\b` сработает для строки `abc`, но регулярное выражение `\b\.\.\b` не сработает для строки `..`?
* Группы
  * Что такое?
  * Как создать?
  * Когда могут быть полезны?
  * Можно ли создавать вложенные группы?
  * Как сделать незапоминающуюся группу (группу, вхождение которой не будет возвращено при матчинге строки на регулярное выражение)?
  * Как использовать значение группы в шаблоне регулярного выражения?
  * Можно ли дать группе имя? Когда это может быть полезно?
  * Как использовать значение группы в новой подстроке в методе replace?
* Как работают опережающие и ретроспективные проверки?
* Решить задачи:
  * Написать регулярное выражение по переводу Function Expression в Function Declaration.
  * Написать регулярное выражение по переводу Function Declaration в Function Expression.
  * Написать регулярное выражение для поиска всех команд Телеграма в сообщении (примеры: `/help`, `/start`, `/active_orders`, `/order123`). Учесть, что команд в подстроке может быть несколько.

## Promises

* Что такое Promise? Для чего он нужен?
* Как создать Promise?
  * Когда выполняется коллбэк, передаваемый аргументом в конструктор промиса?
* Методы `then`, `catch`, `finally`
  * Для чего используются?
  * Что такое цепочка промисов?
  * Что могут возвращать их коллбеки?
    * Как возвращаемое значение влияет на состояние промиса, возвращаемого данным методом?
* В чем отличие между `then(resolveHandler).catch(rejectHandler)` и `then(resolveHandler, rejectHandler)`?
* Можно ли отменить выполнение промиса?
* Для чего нужны и как использовать следующие методы:
  * `Promise.resolve`
  * `Promise.reject`
  * `Promise.all`
  * `Promise.allSettled`
  * `Promise.race`
  * `Promise.any`
* В чем преимущества и недостатки коллбэков и промисов?
* Какое состояние и результат будут у следующего промиса и почему:
  ```javascript
    const promise = new Promise((resolve, reject) => {
      resolve(0);
      reject(1);
      resolve(2);
    });
  ```

## Set, Map

* Set
  * Что такое?
  * Как создать инстанс?
  * Какие методы существуют у инстанса?
  * Как можно перебрать?
  * Может ли содержать одинаковые элементы?
  * Где может быть полезен?
* Map
  * Что такое?
  * Как создать инстанс?
  * Какие методы существуют у инстанса?
  * Как можно перебрать?
  * В чем отличие от обычного объекта?
  * Где может быть полезен?
* WeakSet/WeakMap
  * Что такое?
  * В чем отличия от Set/Map?
  * Где могут быть полезны?

#### Ресурсы

* [JavaScript — from callbacks to async/await](https://medium.freecodecamp.org/javascript-from-callbacks-to-async-await-1cc090ddad99)
* [Promise (learn.javascript.ru)](https://learn.javascript.ru/promise)
* [We have a problem with promises](https://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html)
* [You're Missing the Point of Promises](https://blog.domenic.me/youre-missing-the-point-of-promises/#toc_1)
* [You Don't Know JS: Async & Performance](https://github.com/leonardomso/You-Dont-Know-JS/tree/master/async%20%26%20performance) [(рус.)](https://github.com/devSchacht/You-Dont-Know-JS/tree/master/async%20%26%20performance) - можно прочесть первые три главы
* [Map и Set](https://learn.javascript.ru/map-set)
* [Map (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
* [WeakMap и WeakSet (learn.javascript.ru)](https://learn.javascript.ru/weakmap-weakset)
