<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [auth](./firebase-admin.auth.md) &gt; [ActionCodeSettings](./firebase-admin.auth.actioncodesettings.md) &gt; [handleCodeInApp](./firebase-admin.auth.actioncodesettings.handlecodeinapp.md)

## auth.ActionCodeSettings.handleCodeInApp property

Whether to open the link via a mobile app or a browser. The default is false. When set to true, the action code link is sent as a Universal Link or Android App Link and is opened by the app if installed. In the false case, the code is sent to the web widget first and then redirects to the app if installed.

<b>Signature:</b>

```typescript
handleCodeInApp?: boolean;
```