---
type: "function"
---

# `parseCookies()`

Parses `Cookie` header value and returns a `Map` with the key/value. Cookie names and values are URI-component decoded.

```ts
function parseCookies(cookieHeader: string | null | undefined): Map<string, string>;
```

- `cookieHeader`: `Cookie` HTTP header

## Example

```ts
import { parseCookies } from "oslo/cookie";

const cookies = parseCookies("message=hello");
const message = cookies.get("message");
```

Cookie names and values are URI-component decoded when parsed.

```ts
const cookies = parseCookies("json=%7B%22message%22%3A%22hello%22%7D");
const parsedJSON = JSON.parse(cookies.get("json"));
```