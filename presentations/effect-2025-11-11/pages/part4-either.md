---
layout: section
class: text-black
---

# Enter Either

Errors as Values

---

# Either: Errors in the Type System

<div>

<v-clicks>

`Either<Right, Left>` = computation that **can fail**

- `Either.left(error)` - failure
- `Either.right(value)` - success

```ts
type Either<R, L> = { _tag: "Left"; left: L } | { _tag: "Right"; right: R };
```

**Compiler forces you to handle errors!**

</v-clicks>

</div>

---

```ts {monaco-run}
import { Data, Either } from "effect";

class DivisionError extends Data.TaggedError("DivisionError")<{
  message: string;
}> {}

function safeDivide(
  a: number,
  b: number,
): Either.Either<number, DivisionError> {
  if (b === 0) {
    return Either.left(new DivisionError({ message: "Cannot divide by 0!" }));
  }
  return Either.right(a / b);
}

const result = safeDivide(10, 2);
console.log(
  Either.match(result, {
    onLeft: (e) => `Error: ${e.message}`,
    onRight: (v) => `Result: ${v}`,
  }),
);
```
