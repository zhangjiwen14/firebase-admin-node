<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [auth](./firebase-admin.auth.md) &gt; [MultiFactorConfig](./firebase-admin.auth.multifactorconfig.md)

## auth.MultiFactorConfig interface

Interface representing a multi-factor configuration. This can be used to define whether multi-factor authentication is enabled or disabled and the list of second factor challenges that are supported.

<b>Signature:</b>

```typescript
interface MultiFactorConfig 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [factorIds](./firebase-admin.auth.multifactorconfig.factorids.md) | [AuthFactorType](./firebase-admin.auth.authfactortype.md)<!-- -->\[\] | The list of identifiers for enabled second factors. Currently only ‘phone’ is supported. |
|  [state](./firebase-admin.auth.multifactorconfig.state.md) | [MultiFactorConfigState](./firebase-admin.auth.multifactorconfigstate.md) | The multi-factor config state. |
