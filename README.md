## React Hooks: JWT Authentication (without Redux) example

## Note:

Open `src/services/auth-header.js` and modify `return` statement for appropriate back-end (found in the tutorial).

```js
export default function authHeader() {
  const user = JSON.parse(localStorage.getItem("user"));

  if (user && user.accessToken) {
    // return { Authorization: 'Bearer ' + user.accessToken }; // for Spring Boot back-end
    return { "x-access-token": user.accessToken }; // for Node.js Express back-end
  } else {
    return {};
  }
}
```
