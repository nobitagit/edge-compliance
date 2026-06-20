# Skill: update-cards

Parse `data.csv` from the project root and replace the `CARDS` array in `index.html` with the converted data.

## Column mapping

| CSV column | JSON key | Type |
|---|---|---|
| _(fill in: column containing the card question text)_ | `title` | `string` |
| _(fill in: column containing the correct answer)_ | `correct` | `boolean` — `true` for Yes, `false` for No |
| _(fill in: column containing the category)_ | `category` | `string` |
| _(fill in: column containing the explanation)_ | `reason` | `string` |

Each object also gets an `id` key equal to its zero-based index in the array.

## Steps

1. Read `data.csv` from the project root.
2. Parse the CSV — respect quoted fields and handle any trailing whitespace.
3. Convert each row to an object using the column mapping above.
4. Add `id` as the zero-based row index.
5. In `index.html`, replace the entire `const CARDS = [ ... ];` block with the new array.
6. Commit the change with the message: `Update CARDS from data.csv`.

## Expected output shape

```js
const CARDS = [
  {
    id:       0,
    title:    "...",
    correct:  true,   // or false
    category: "...",
    reason:   "...",
  },
  // ...
];
```

## Notes

- Do not modify any other part of `index.html`.
- Do not add or remove fields beyond those listed above.
- The `correct` field must always be a boolean, never a string.
