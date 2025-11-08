---
layout: section
class: text-black
---

# Promises

---

# How Promises Work

<div class="grid grid-cols-2 gap-8">

<div>

<v-clicks>

A `Promise<T>` represents a **future value**

- `Promise.resolve(value)` - success
- `Promise.reject(error)` - failure
- `.then()` - chain operations
- `.catch()` - handle errors

</v-clicks>

</div>

<div v-click>

```ts {monaco-run}
function fetchUser(id: string): Promise<{
  name: string;
  email: string;
}> {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (id === "1") {
        resolve({
          name: "Alice",
          email: "alice@example.com",
        });
      } else {
        reject(new Error("User not found"));
      }
    }, 1000);
  });
}

fetchUser("1")
  .then((user) => console.log("User:", user.name))
  .catch((err) => console.error("Error:", err.message));
```

</div>

</div>
