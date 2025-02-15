---
type: "method"
---

# `Scrypt.verify()`

Verifies the password with the hash using scrypt.

## Definition

```ts
function verify(hash: string, password: string): Promise<boolean>;
```

### Parameters

- `hash`
- `password`

## Example

```ts
//$ scrypt=/reference/password/Scrypt
const validPassword = await $$scrypt.verify(hash, password);
```
