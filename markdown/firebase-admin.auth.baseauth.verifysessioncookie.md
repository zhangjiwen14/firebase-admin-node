<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [auth](./firebase-admin.auth.md) &gt; [BaseAuth](./firebase-admin.auth.baseauth.md) &gt; [verifySessionCookie](./firebase-admin.auth.baseauth.verifysessioncookie.md)

## auth.BaseAuth.verifySessionCookie() method

Verifies a Firebase session cookie. Returns a Promise with the cookie claims. Rejects the promise if the cookie could not be verified. If `checkRevoked` is set to true, verifies if the session corresponding to the session cookie was revoked. If the corresponding user's session was revoked, an `auth/session-cookie-revoked` error is thrown. If not specified the check is not performed.

See \[Verify Session Cookies\](/docs/auth/admin/manage-cookies\#verify\_session\_cookie\_and\_check\_permissions) for code samples and detailed documentation

<b>Signature:</b>

```typescript
verifySessionCookie(sessionCookie: string, checkForRevocation?: boolean): Promise<DecodedIdToken>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  sessionCookie | string | The session cookie to verify. |
|  checkForRevocation | boolean | Whether to check if the session cookie was revoked. This requires an extra request to the Firebase Auth backend to check the <code>tokensValidAfterTime</code> time for the corresponding user. When not specified, this additional check is not performed. A promise fulfilled with the session cookie's decoded claims if the session cookie is valid; otherwise, a rejected promise. |

<b>Returns:</b>

Promise&lt;[DecodedIdToken](./firebase-admin.auth.decodedidtoken.md)<!-- -->&gt;
