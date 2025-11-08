---
layout: section
class: text-black
---

# The Null Problem

`null` and `undefined`

Tony Hoare, null's creator, regrets its invention:

> “I call it my billion-dollar mistake."

---

```ts {monaco-run}
interface User {
  name: string;
  email: string;
}

function findUser(id: string): User | null {
  // Look up in DB
  if (id === "1") {
    return {
      name: "Alice",
      email: "alice@example.com",
    };
  }
  return null;
}

const user = findUser("999");

console.log("Email:", user.email); // 💥
```
