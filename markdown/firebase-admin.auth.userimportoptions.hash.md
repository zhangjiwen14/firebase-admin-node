<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [auth](./firebase-admin.auth.md) &gt; [UserImportOptions](./firebase-admin.auth.userimportoptions.md) &gt; [hash](./firebase-admin.auth.userimportoptions.hash.md)

## auth.UserImportOptions.hash property

The password hashing information.

<b>Signature:</b>

```typescript
hash: {
            algorithm: HashAlgorithmType;
            key?: Buffer;
            saltSeparator?: Buffer;
            rounds?: number;
            memoryCost?: number;
            parallelization?: number;
            blockSize?: number;
            derivedKeyLength?: number;
        };
```