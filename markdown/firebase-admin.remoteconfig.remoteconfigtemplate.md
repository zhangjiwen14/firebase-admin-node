<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [firebase-admin](./firebase-admin.md) &gt; [remoteConfig](./firebase-admin.remoteconfig.md) &gt; [RemoteConfigTemplate](./firebase-admin.remoteconfig.remoteconfigtemplate.md)

## remoteConfig.RemoteConfigTemplate interface

Interface representing a Remote Config template.

<b>Signature:</b>

```typescript
interface RemoteConfigTemplate 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [conditions](./firebase-admin.remoteconfig.remoteconfigtemplate.conditions.md) | [RemoteConfigCondition](./firebase-admin.remoteconfig.remoteconfigcondition.md)<!-- -->\[\] | A list of conditions in descending order by priority. |
|  [etag](./firebase-admin.remoteconfig.remoteconfigtemplate.etag.md) | string | ETag of the current Remote Config template (readonly). |
|  [parameterGroups](./firebase-admin.remoteconfig.remoteconfigtemplate.parametergroups.md) | { \[key: string\]: [RemoteConfigParameterGroup](./firebase-admin.remoteconfig.remoteconfigparametergroup.md)<!-- -->; } | Map of parameter group names to their parameter group objects. A group's name is mutable but must be unique among groups in the Remote Config template. The name is limited to 256 characters and intended to be human-readable. Any Unicode characters are allowed. |
|  [parameters](./firebase-admin.remoteconfig.remoteconfigtemplate.parameters.md) | { \[key: string\]: [RemoteConfigParameter](./firebase-admin.remoteconfig.remoteconfigparameter.md)<!-- -->; } | Map of parameter keys to their optional default values and optional conditional values. |
|  [version](./firebase-admin.remoteconfig.remoteconfigtemplate.version.md) | [Version](./firebase-admin.remoteconfig.version.md) | Version information for the current Remote Config template. |
