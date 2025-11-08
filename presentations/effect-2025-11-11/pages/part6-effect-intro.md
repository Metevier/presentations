---
layout: section
class: text-black
---

# Enter Effect

---

# Promise vs Effect

### Promises

```ts
function fetchUser(id: string): Promise<User> {
  // What errors can this throw? 🤷
  // NetworkError? ParseError?
  // ValidationError?
}

// Catch everything as 'unknown'
fetchUser("1")
  .then((user) => process(user))
  .catch((err) => {
    // What type is err?
    console.error(err);
  });
```

---

```ts {monaco-run}
import { Data, Effect, pipe } from "effect";

class NotFoundError extends Data.TaggedError("NotFoundError")<{
  message: string;
  id: string;
}> {}

function fetchUser(id: string): Effect.Effect<{ name: string }, NotFoundError> {
  if (id === "1") {
    return Effect.succeed({ name: "Alice" });
  }
  return Effect.fail(new NotFoundError({ id, message: "User not found!" }));
}

pipe(
  fetchUser("1"),
  Effect.map((user) => `Hello, ${user.name}!`),
  Effect.catchTag("NotFoundError", (err) =>
    Effect.succeed(`User ${err.id} not found`),
  ),
  Effect.runPromise,
).then(console.log);
```

---

### Async Await

```ts
async function fetchUser(id: string): Promise<User> {
  const user = await db.getById(id);
  return user;
}

try {
  const user = await fetchUser("1");
} catch {}
```

---

### Javascript Generators

```ts {monaco-run}
import { Data, Effect, pipe } from "effect";

class NotFoundError extends Data.TaggedError("NotFoundError")<{
  message: string;
  id: string;
}> {}

const fetchUser = Effect.fn(function* (id: string) {
  if (id === "1") {
    return { name: "Alice" };
  }
  return yield* new NotFoundError({ id, message: "User not found!" });
});

pipe(
  fetchUser("1"),
  Effect.map((user) => `Hello, ${user.name}!`),
  Effect.catchTag("NotFoundError", (err) =>
    Effect.succeed(`User ${err.id} not found`),
  ),
  Effect.runPromise,
).then(console.log);
```

---

# Effect Superpowers

<div>

### 1. Retry & Timeout

```ts
pipe(
  fetchUser("1"),
  Effect.retry(Schedule.exponential("100 millis")),
  Effect.timeout("5 seconds"),
);
```

</div>

<div v-click>

### 2. Resource Management

```ts
const sendFile = Effect.fn(function* (fileName: string, email: string) {
  const file = Effect.acquireRelease(openFile(fileName), (file) =>
    closeFile(file),
  );
  yield* sendEmail(email, file.text);
}, Effect.scoped);
```

</div>
