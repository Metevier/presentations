---
layout: section
class: text-black
---

# The Error Problem

When Try/Catch Fails Us

---

# Errors Are Invisible

<div class="grid grid-cols-2 gap-8">

<div>

### The Problem with Try/Catch

<v-clicks>

**Errors not in type system**

- What errors can a function throw? Does a function throw?
- TypeScript can't tell you!
- Must read implementation
- `catch (error)` is `unknown`

</v-clicks>

</div>

</div>

---

```ts {monaco-run}
function calculatePrice(quantity: number, pricePerUnit: string): number {
  const price = parseFloat(pricePerUnit);

  if (Number.isNaN(price)) throw new Error("Price must be a number!");

  const total = quantity * price;

  if (total > 1000) {
    throw new Error("Too expensive!");
  }

  return total;
}

try {
  console.log(calculatePrice(5, "50"));
} catch (error) {
  console.error(error);
}
```
