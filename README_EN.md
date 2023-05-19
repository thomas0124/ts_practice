# Practice Procedure
# Preparation
- Install node.js
- Install npm (able to execute npm command)
## Set up the Execution Environment
### Create a Directory
- Execute `$mkdir practice`
- Execute `$cd practice`
### Create Files
- Execute `$npm init --yes` (Use the `--yes` option to answer all questions with "yes" and use default values)
- package.json will be created
- Make changes to package.json
- Add "type" to package.json

```
"main": "index.js",
```
↓  ↓  ↓

```
"main": "index.js",
"type": "module",
```

### Install TypeScript
- Execute `$npm install --save-dev typescript @types/node`
- node_modules directory and package-lock.json will be created
- Create tsconfig.json
- Execute `$npx tsc --init`
- Make changes to tsconfig.json as needed
- Change "target" in tsconfig.json

```
"target": "es2016"
```
↓  ↓  ↓

```
"target": "ES2020"
```

- Change "module" in tsconfig.json

```
"module": "commonjs",
```
↓  ↓  ↓

```
"module": "ESNEXT"
```

- Change moduleResolution compiler option to "node"

```
//"moduleResolution": "node",
```
↓  ↓  ↓

```
"moduleResolution": "node",
```

- Change "outDir" in tsconfig.json

```
//"outDir": "./",
```
↓  ↓  ↓

```
"outDir": "./dist",
```

- Finally, set the include option
```
{
 "compilerOptions": {
    // many other compiler options
 },
// ↓ Add here
 "include": ["./src/**/*.ts"]
}
```

### First TypeScript Program
- Create a src directory
- Create index.ts inside the src directory
- Write your code in index.ts
- Go to the project root and execute `$npx tsc`
- dist directory will be created
- index.js will be created inside the dist directory
- Execute `$node dist/index.js` (Pay attention to the path)
- The output of the program will be displayed