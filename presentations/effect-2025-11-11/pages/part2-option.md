---
layout: section
class: text-black
---

# Enter Option

A Better Way to Handle "Nothing"

---

# Option: Making Missing Values Explicit

<v-clicks>

`Option<A>` = value that **may or may not exist**

- `Option.some(value)` - has value
- `Option.none()` - no value

```ts
type Option<A> = { _tag: "None" } | { _tag: "Some"; value: A };
```

</v-clicks>

---

<div v-click>

```ts {monaco-run}
import { Option, pipe } from "effect";

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

const result = pipe(
  findUser("1"),
  Option.map((user) => user.email.toUpperCase()),
  Option.getOrElse(() => "Not found"),
);

console.log(result);
```

</div>
