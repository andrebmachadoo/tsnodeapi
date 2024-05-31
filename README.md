# tsnodeapi
---

> tsnodeapi is a start code for projetcs of rest api. The initial objective was study ts, but this project turn something util to use in other projects.


### Starting a project 

1. Install dependencies 
```bash
$ npm install typescript @types/node -D
$ npx tsc --init
```

2. Changing tsconfig.json 

> Search on google 'node target mapping github' or accept [this url](https://github.com/microsoft/TypeScript/wiki/node-target-mapping) and change tsconfig.json with the same node version

```JSON
// node 20 
{
  "compilerOptions": {
    "lib": ["ES2023"],
    "module": "node16",
    "target": "ES2022"
  }
}

// node 18
{
  "compilerOptions": {
    "lib": ["ES2023"],
    "module": "node16",
    "target": "ES2022"
  }
}

//node 16
{
  "compilerOptions": {
    "lib": ["ES2021"],
    "module": "node16",
    "target": "ES2021"
  }
}
...
```
3. install tsx for to build/execute app in devel time and changing script package.json

```shell
$ npm install tsx -D
```

```JSON
"scripts": {
    "dev": "tsx watch src/http/server.ts",
}

//or 

"scripts": {
    "dev": "tsx watch src/http/server.ts --onSuccess \"node dist/index.js\"",
},

```

3. install tsup for to build app for deploy in prodution, and changing script package.json


```shell
$ npm install tsx -D
```

```JSON
"scripts": {
    "dev": "tsup src",
}
```

4. Install vitest for tests 


```shell
$ npm vitest -D
```

