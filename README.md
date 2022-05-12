- `yarn`
- `yarn dev`

=> This works

- Now rename `package.json` to `package.json.bak`
- Rename `package.json.withError` to `package.json`
- Remove comments and comment out relevant lines in `src/App.tsx`
- `yarn`
- `yarn dev`

Results in:

```
[plugin vite:dep-scan] Failed to resolve entry for package "@cognite/3d-web-parser". The package may have incorrect main/module/exports specified in its package.json: Failed to resolve entry for package "@cognite/3d-web-parser". The package may have incorrect main/module/exports specified in its package.json.
```

=> A direct dependency on `@cognite/3d-web-parser` does not result in a Vite error, while a transitive dependency on it **does** result in an error