# Simple Node TypeScript Project

This is a basic Node.js project using TypeScript to demonstrate a simple setup and to test installation via `npm`.

## Features

- Basic TypeScript setup
- Simple project structure
- Test installation via `npm install <repository>`

## Requirements

- Node.js (>= 14)
- npm (>= 6)

## Installation

Install this project locally by running:

```
$ npm install https://github.com/sutigit/node-typescript-template.git
```

## Usage
Then you should be able to use the module via 
```
import Main from 'node_typescript';

const app = new Main('lol')

console.log(app.getWord()) -> lol
```

## How to achieve this
1. Create project folder: `mkdir project-name`
2. Install typescript: `npm i typescript -g`
3. Create typescript config file: `tsc --init`
4. Make sure in package.json the `main` is set to the entry file. Example:
```
{
  "name": "node_typescript",
  "version": "1.0.0",
  "main": "src/main.ts",
  "scripts": { ...
```
5. For building, adjust settings in `tsconfig.json`
    1. Set source path. Look for entry `rootDir` and change to: `"rootDir": "./src"`
    2. Set build path. Look for entry `outDir` and change to: `"outDir": "./build"`
6. Make typescript ignore everything except the src folder when building. Add to the bottom of `tsconfig.json`:
```
    "skipLibCheck": true                                 
  },
  "include": [
    "src"
  ]
```
7. And lastly push it to github