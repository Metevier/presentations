---
layout: section
class: text-black
---

# Keeping it simple

---

# Array.map

<div class="grid grid-cols-2 gap-8">

<div>

```ts
const numbers = [1, 2, 3, 4];

// Transform each number
const doubled = numbers.map((n) => n * 2);

console.log(doubled);
// [2, 4, 6, 8]
```

<v-clicks>

**map applies a function to each element**

- Takes: `Array<A>` and `(A => B)`
- Returns: `Array<B>`

</v-clicks>

</div>

</div>

---

**Challenge**: Extract all items from all orders

```ts {monaco-run}
interface Order {
  id: string;
  items: string[];
}

const orders: Order[] = [
  { id: "1", items: ["apple", "banana"] },
  { id: "2", items: ["orange"] },
  { id: "3", items: ["grape", "melon", "kiwi"] },
];

// TODO:  Expected: ['apple', 'banana', 'orange',
//            'grape', 'melon', 'kiwi']
const allItems = orders;

console.log(allItems);
```

---

```ts {monaco-run}
import { Option } from "effect";
const maybeNumber = Option.some(5);

const doubled = maybeNumber.pipe(Option.map((n) => n * 2));
console.log(doubled);
```

---

```ts {monaco-run}
import { Option } from "effect";

interface User {
  name: string;
  email: string;
}

function findUser(id: string): Option.Option<User> {
  // Lookup in DB
  if (id === "1") {
    return Option.some({
      name: "Alice",
      email: "alice@example.com",
    });
  }
  return Option.none();
}

const maybeId = Option.some("1");
const maybeUser = findUser(maybeId);

declare const maybeEmail: string; // how do I get this??
```
