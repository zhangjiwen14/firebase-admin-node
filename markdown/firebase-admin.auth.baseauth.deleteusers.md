<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [auth](./firebase-admin.auth.md) &gt; [BaseAuth](./firebase-admin.auth.baseauth.md) &gt; [deleteUsers](./firebase-admin.auth.baseauth.deleteusers.md)

## auth.BaseAuth.deleteUsers() method

Deletes the users specified by the given uids.

Deleting a non-existing user won't generate an error (i.e. this method is idempotent.) Non-existing users are considered to be successfully deleted, and are therefore counted in the `DeleteUsersResult.successCount` value.

Only a maximum of 1000 identifiers may be supplied. If more than 1000 identifiers are supplied, this method throws a FirebaseAuthError.

This API is currently rate limited at the server to 1 QPS. If you exceed this, you may get a quota exceeded error. Therefore, if you want to delete more than 1000 users, you may need to add a delay to ensure you don't go over this limit.

<b>Signature:</b>

```typescript
deleteUsers(uids: string[]): Promise<DeleteUsersResult>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  uids | string\[\] | The <code>uids</code> corresponding to the users to delete. A Promise that resolves to the total number of successful/failed deletions, as well as the array of errors that corresponds to the failed deletions. |

<b>Returns:</b>

Promise&lt;[DeleteUsersResult](./firebase-admin.auth.deleteusersresult.md)<!-- -->&gt;
