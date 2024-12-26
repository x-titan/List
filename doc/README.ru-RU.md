# Data Structures Library: List, Queue, and Stack

Эта библиотека предоставляет реализацию основных структур данных: [**связного списка (List)**][list], [**очереди (Queue)**][queue] и [**стека (Stack)**][stack]. Каждый из них экспортируется как функция-класс для удобной работы.

---

## Установка

Сначала установите библиотеку через NPM (если она опубликована) или клонируйте репозиторий:

```bash
npm install your-library-name
```

---

## Использование

### [**List**][list]
`List` реализует почти все методы массивов JavaScript, что делает его простым и удобным для работы.

#### Поддерживаемые методы:
- **`push(element)`**: Добавляет элемент в конец списка.
- **`pop()`**: Удаляет последний элемент и возвращает его.
- **`unshift(element)`**: Добавляет элемент в начало списка.
- **`shift()`**: Удаляет первый элемент и возвращает его.
- **`indexOf(element)`**: Возвращает индекс указанного элемента (или -1, если элемент не найден).
- **`splice(index, count, ...elements)`**: Удаляет или добавляет элементы в список.
- **`at(index)`**: Возвращает элемент по индексу (аналог `array.at()`).
- **`find({ element, callback })`**: Ищет элемент по значению или через функцию обратного вызова.
- **`concat(collection)`**: Объединяет текущий список с другим списком или массивом.

#### Не реализованные методы (в разработке):
- **`sort()`**: Сортировка списка.
- **`reverse()`**: Разворот списка.
- **`filter(callback)`**: Фильтрация элементов списка.

#### Пример:
```javascript
import { List } from 'your-library-name';

const list = new List();
list.push(1);
list.push(2);
list.push(3);

console.log(list.pop()); // 3
console.log(list.indexOf(2)); // 1
```

---

### [**Queue**][queue]
Очередь — это структура данных, которая работает по принципу **FIFO** (First In, First Out).

#### Поддерживаемые методы:
- **`enqueue(element)`** (аналог `push`): Добавляет элемент в конец очереди.
- **`dequeue()`** (аналог `shift`): Удаляет первый элемент и возвращает его.
- **`peek()`**: Возвращает первый элемент без его удаления.

#### Пример:
```javascript
import { Queue } from 'your-library-name';

const queue = new Queue();
queue.enqueue('A');
queue.enqueue('B');

console.log(queue.peek()); // 'A'
console.log(queue.dequeue()); // 'A'
console.log(queue.dequeue()); // 'B'
```

---

### [**Stack**][stack]
Стек — это структура данных, которая работает по принципу **LIFO** (Last In, First Out).

#### Поддерживаемые методы:
- **`push(element)`** (аналог `unshift`): Добавляет элемент в начало стека.
- **`pop()`** (аналог `shift`): Удаляет первый элемент и возвращает его.
- **`peek()`**: Возвращает первый элемент без его удаления.

#### Пример:
```javascript
import { Stack } from 'your-library-name';

const stack = new Stack();
stack.push('X');
stack.push('Y');

console.log(stack.peek()); // 'Y'
console.log(stack.pop()); // 'Y'
console.log(stack.pop()); // 'X'
```

---

## Планы на будущее
- Реализация методов `sort`, `reverse`, и `filter` для `List`.
- Оптимизация производительности и добавление новых функций.

---

## Лицензия

Этот проект распространяется под лицензией MIT. Подробнее читайте в [LICENSE](./LICENSE).

[list]: /src/list.js
[queue]: /src/queue.js
[stack]: /src/stack.js
