# odata-v4-server-shim
A shim to share the model classes between frontend and backend.

If you're using [odata-v4-server](https://github.com/jaystack/odata-v4-server), you most probably annotated your model classes and their properties with `@Edm` TypeScript decorators. Unfortunately this will not work if you want to share your model classes between frontend and backend. E.g. if you want to use the model classes in an Angular application, it will not work, as odata-v4-server is developed for server (duh?!?).

If you'll use this shim you will be able to use the model classes in frontend. How to effectively do it?

Just install this shim

```
npm i odata-v4-server-shim
```

or

```
npm i https://github.com/beradrian/odata-v4-server-shim.git
```

and then add the path to your tsconfig

```typescript
{
  ...
  "compilerOptions": {
    ...
    "paths": {
      "odata-v4-sever": ["./node_modules/odata-v4-server-shim"]
    }
  }
}
```
