<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [auth](./firebase-admin.auth.md) &gt; [BaseAuth](./firebase-admin.auth.baseauth.md)

## auth.BaseAuth interface

<b>Signature:</b>

```typescript
interface BaseAuth 
```

## Methods

|  Method | Description |
|  --- | --- |
|  [createCustomToken(uid, developerClaims)](./firebase-admin.auth.baseauth.createcustomtoken.md) | Creates a new Firebase custom token (JWT) that can be sent back to a client device to use to sign in with the client SDKs' <code>signInWithCustomToken()</code> methods. (Tenant-aware instances will also embed the tenant ID in the token.)<!-- -->See \[Create Custom Tokens\](/docs/auth/admin/create-custom-tokens) for code samples and detailed documentation. |
|  [createProviderConfig(config)](./firebase-admin.auth.baseauth.createproviderconfig.md) | Returns a promise that resolves with the newly created <code>AuthProviderConfig</code> when the new provider configuration is created.<!-- -->SAML and OIDC provider support requires Google Cloud's Identity Platform (GCIP). To learn more about GCIP, including pricing and features, see the \[GCIP documentation\](https://cloud.google.com/identity-platform). |
|  [createSessionCookie(idToken, sessionCookieOptions)](./firebase-admin.auth.baseauth.createsessioncookie.md) | Creates a new Firebase session cookie with the specified options. The created JWT string can be set as a server-side session cookie with a custom cookie policy, and be used for session management. The session cookie JWT will have the same payload claims as the provided ID token.<!-- -->See \[Manage Session Cookies\](/docs/auth/admin/manage-cookies) for code samples and detailed documentation. |
|  [createUser(properties)](./firebase-admin.auth.baseauth.createuser.md) | Creates a new user.<!-- -->See \[Create a user\](/docs/auth/admin/manage-users\#create\_a\_user) for code samples and detailed documentation. |
|  [deleteProviderConfig(providerId)](./firebase-admin.auth.baseauth.deleteproviderconfig.md) | Deletes the provider configuration corresponding to the provider ID passed. If the specified ID does not exist, an <code>auth/configuration-not-found</code> error is thrown.<!-- -->SAML and OIDC provider support requires Google Cloud's Identity Platform (GCIP). To learn more about GCIP, including pricing and features, see the \[GCIP documentation\](https://cloud.google.com/identity-platform). |
|  [deleteUser(uid)](./firebase-admin.auth.baseauth.deleteuser.md) | Deletes an existing user.<!-- -->See \[Delete a user\](/docs/auth/admin/manage-users\#delete\_a\_user) for code samples and detailed documentation. |
|  [deleteUsers(uids)](./firebase-admin.auth.baseauth.deleteusers.md) | Deletes the users specified by the given uids.<!-- -->Deleting a non-existing user won't generate an error (i.e. this method is idempotent.) Non-existing users are considered to be successfully deleted, and are therefore counted in the <code>DeleteUsersResult.successCount</code> value.<!-- -->Only a maximum of 1000 identifiers may be supplied. If more than 1000 identifiers are supplied, this method throws a FirebaseAuthError.<!-- -->This API is currently rate limited at the server to 1 QPS. If you exceed this, you may get a quota exceeded error. Therefore, if you want to delete more than 1000 users, you may need to add a delay to ensure you don't go over this limit. |
|  [generateEmailVerificationLink(email, actionCodeSettings)](./firebase-admin.auth.baseauth.generateemailverificationlink.md) | Generates the out of band email action link to verify the user's ownership of the specified email. The  object provided as an argument to this method defines whether the link is to be handled by a mobile app or browser along with additional state information to be passed in the deep link, etc. |
|  [generatePasswordResetLink(email, actionCodeSettings)](./firebase-admin.auth.baseauth.generatepasswordresetlink.md) | Generates the out of band email action link to reset a user's password. The link is generated for the user with the specified email address. The optional  object defines whether the link is to be handled by a mobile app or browser and the additional state information to be passed in the deep link, etc. |
|  [generateSignInWithEmailLink(email, actionCodeSettings)](./firebase-admin.auth.baseauth.generatesigninwithemaillink.md) | Generates the out of band email action link to sign in or sign up the owner of the specified email. The  object provided as an argument to this method defines whether the link is to be handled by a mobile app or browser along with additional state information to be passed in the deep link, etc. |
|  [getProviderConfig(providerId)](./firebase-admin.auth.baseauth.getproviderconfig.md) | Looks up an Auth provider configuration by the provided ID. Returns a promise that resolves with the provider configuration corresponding to the provider ID specified. If the specified ID does not exist, an <code>auth/configuration-not-found</code> error is thrown.<!-- -->SAML and OIDC provider support requires Google Cloud's Identity Platform (GCIP). To learn more about GCIP, including pricing and features, see the \[GCIP documentation\](https://cloud.google.com/identity-platform). |
|  [getUser(uid)](./firebase-admin.auth.baseauth.getuser.md) | Gets the user data for the user corresponding to a given <code>uid</code>.<!-- -->See \[Retrieve user data\](/docs/auth/admin/manage-users\#retrieve\_user\_data) for code samples and detailed documentation. |
|  [getUserByEmail(email)](./firebase-admin.auth.baseauth.getuserbyemail.md) | Gets the user data for the user corresponding to a given email.<!-- -->See \[Retrieve user data\](/docs/auth/admin/manage-users\#retrieve\_user\_data) for code samples and detailed documentation. |
|  [getUserByPhoneNumber(phoneNumber)](./firebase-admin.auth.baseauth.getuserbyphonenumber.md) | Gets the user data for the user corresponding to a given phone number. The phone number has to conform to the E.164 specification.<!-- -->See \[Retrieve user data\](/docs/auth/admin/manage-users\#retrieve\_user\_data) for code samples and detailed documentation. |
|  [getUsers(identifiers)](./firebase-admin.auth.baseauth.getusers.md) | Gets the user data corresponding to the specified identifiers.<!-- -->There are no ordering guarantees; in particular, the nth entry in the result list is not guaranteed to correspond to the nth entry in the input parameters list.<!-- -->Only a maximum of 100 identifiers may be supplied. If more than 100 identifiers are supplied, this method throws a FirebaseAuthError. |
|  [importUsers(users, options)](./firebase-admin.auth.baseauth.importusers.md) | Imports the provided list of users into Firebase Auth. A maximum of 1000 users are allowed to be imported one at a time. When importing users with passwords,  are required to be specified. This operation is optimized for bulk imports and will ignore checks on <code>uid</code>, <code>email</code> and other identifier uniqueness which could result in duplications. |
|  [listProviderConfigs(options)](./firebase-admin.auth.baseauth.listproviderconfigs.md) | Returns the list of existing provider configurations matching the filter provided. At most, 100 provider configs can be listed at a time.<!-- -->SAML and OIDC provider support requires Google Cloud's Identity Platform (GCIP). To learn more about GCIP, including pricing and features, see the \[GCIP documentation\](https://cloud.google.com/identity-platform). |
|  [listUsers(maxResults, pageToken)](./firebase-admin.auth.baseauth.listusers.md) | Retrieves a list of users (single batch only) with a size of <code>maxResults</code> starting from the offset as specified by <code>pageToken</code>. This is used to retrieve all the users of a specified project in batches.<!-- -->See \[List all users\](/docs/auth/admin/manage-users\#list\_all\_users) for code samples and detailed documentation. |
|  [revokeRefreshTokens(uid)](./firebase-admin.auth.baseauth.revokerefreshtokens.md) | Revokes all refresh tokens for an existing user.<!-- -->This API will update the user's  to the current UTC. It is important that the server on which this is called has its clock set correctly and synchronized.<!-- -->While this will revoke all sessions for a specified user and disable any new ID tokens for existing sessions from getting minted, existing ID tokens may remain active until their natural expiration (one hour). To verify that ID tokens are revoked, use  where <code>checkRevoked</code> is set to true. |
|  [setCustomUserClaims(uid, customUserClaims)](./firebase-admin.auth.baseauth.setcustomuserclaims.md) | Sets additional developer claims on an existing user identified by the provided <code>uid</code>, typically used to define user roles and levels of access. These claims should propagate to all devices where the user is already signed in (after token expiration or when token refresh is forced) and the next time the user signs in. If a reserved OIDC claim name is used (sub, iat, iss, etc), an error is thrown. They are set on the authenticated user's ID token JWT.<!-- -->See \[Defining user roles and access levels\](/docs/auth/admin/custom-claims) for code samples and detailed documentation. |
|  [updateProviderConfig(providerId, updatedConfig)](./firebase-admin.auth.baseauth.updateproviderconfig.md) | Returns a promise that resolves with the updated <code>AuthProviderConfig</code> corresponding to the provider ID specified. If the specified ID does not exist, an <code>auth/configuration-not-found</code> error is thrown.<!-- -->SAML and OIDC provider support requires Google Cloud's Identity Platform (GCIP). To learn more about GCIP, including pricing and features, see the \[GCIP documentation\](https://cloud.google.com/identity-platform). |
|  [updateUser(uid, properties)](./firebase-admin.auth.baseauth.updateuser.md) | Updates an existing user.<!-- -->See \[Update a user\](/docs/auth/admin/manage-users\#update\_a\_user) for code samples and detailed documentation. |
|  [verifyIdToken(idToken, checkRevoked)](./firebase-admin.auth.baseauth.verifyidtoken.md) | Verifies a Firebase ID token (JWT). If the token is valid, the promise is fulfilled with the token's decoded claims; otherwise, the promise is rejected. An optional flag can be passed to additionally check whether the ID token was revoked.<!-- -->See \[Verify ID Tokens\](/docs/auth/admin/verify-id-tokens) for code samples and detailed documentation. |
|  [verifySessionCookie(sessionCookie, checkForRevocation)](./firebase-admin.auth.baseauth.verifysessioncookie.md) | Verifies a Firebase session cookie. Returns a Promise with the cookie claims. Rejects the promise if the cookie could not be verified. If <code>checkRevoked</code> is set to true, verifies if the session corresponding to the session cookie was revoked. If the corresponding user's session was revoked, an <code>auth/session-cookie-revoked</code> error is thrown. If not specified the check is not performed.<!-- -->See \[Verify Session Cookies\](/docs/auth/admin/manage-cookies\#verify\_session\_cookie\_and\_check\_permissions) for code samples and detailed documentation |
