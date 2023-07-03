# graphql-codegen-windows-repro

## Repro Steps

The issue only occurs on Windows. Tested in Windows 11.

1. `cd app`
1. `yarn install`
1. `yarn graphql-codegen --watch`

It outputs:

```text
[Watcher] Longest common prefix () is not accessible
[Watcher] Watching current working directory (C:\Projects\oss\bugs\graphql-codegen-windows-repro\app) instead
```

So if you make an edit to `schema.gql`, graphql-codegen will not update the generated code.
