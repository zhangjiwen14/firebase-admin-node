<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [remoteConfig](./firebase-admin.remoteconfig.md) &gt; [RemoteConfig](./firebase-admin.remoteconfig.remoteconfig.md)

## remoteConfig.RemoteConfig interface

The Firebase `RemoteConfig` service interface.

Do not call this constructor directly. Instead, use \[`admin.remoteConfig()`<!-- -->\](admin.remoteConfig\#remoteConfig).

<b>Signature:</b>

```typescript
interface RemoteConfig 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [app](./firebase-admin.remoteconfig.remoteconfig.app.md) | [app.App](./firebase-admin.app.app.md) |  |

## Methods

|  Method | Description |
|  --- | --- |
|  [createTemplateFromJSON(json)](./firebase-admin.remoteconfig.remoteconfig.createtemplatefromjson.md) | Creates and returns a new Remote Config template from a JSON string. |
|  [getTemplate()](./firebase-admin.remoteconfig.remoteconfig.gettemplate.md) | Gets the current active version of the  of the project. A promise that fulfills with a <code>RemoteConfigTemplate</code>. |
|  [getTemplateAtVersion(versionNumber)](./firebase-admin.remoteconfig.remoteconfig.gettemplateatversion.md) | Gets the requested version of the  of the project. |
|  [listVersions(options)](./firebase-admin.remoteconfig.remoteconfig.listversions.md) | Gets a list of Remote Config template versions that have been published, sorted in reverse chronological order. Only the last 300 versions are stored. All versions that correspond to non-active Remote Config templates (that is, all except the template that is being fetched by clients) are also deleted if they are more than 90 days old. |
|  [publishTemplate(template, options)](./firebase-admin.remoteconfig.remoteconfig.publishtemplate.md) | Publishes a Remote Config template. |
|  [rollback(versionNumber)](./firebase-admin.remoteconfig.remoteconfig.rollback.md) | Rolls back a project's published Remote Config template to the specified version. A rollback is equivalent to getting a previously published Remote Config template and re-publishing it using a force update. |
|  [validateTemplate(template)](./firebase-admin.remoteconfig.remoteconfig.validatetemplate.md) | Validates a . |
