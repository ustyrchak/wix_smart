# TypeScript

## What is TypeScript?

### JavaScript + Static Types (and more)

TypeScript is an open-source language which builds on JavaScript, one of the world’s most used tools, by adding static type definitions.

Types provide a way to describe the shape of an object, providing better documentation, and allowing TypeScript to validate that your code is working correctly.

Writing types can be optional in TypeScript, because type inference allows you to get a lot of power without writing additional code.

### A Result You Can Trust

All valid JavaScript code is also TypeScript code. You might get type-checking errors, but that won't stop you from running the resulting JavaScript. While you can go for stricter behavior, that means you're still in control.

TypeScript code is transformed into JavaScript code via the TypeScript compiler or Babel. This JavaScript is clean, simple code which runs anywhere JavaScript runs: In a browser, on Node.JS or in your apps.

### Gradual Adoption

Adopting TypeScript is not a binary choice, you can start by annotating existing JavaScript with JSDoc, then switch a few files to be checked by TypeScript and over time prepare your codebase to convert completely.

TypeScript’s type inference means that you don’t have to annotate your code until you want more safety.

## Where to start?

### There are several entry points for different level of previous experience aka "TypeScript in 5 minutes"

CHOOSE ONE which suits you the most in [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html#get-started)

### Start playing with some TypeScript

- [In web playground](https://www.typescriptlang.org/play)
- [Locally with TypeScript tools](https://www.typescriptlang.org/docs/handbook/typescript-tooling-in-5-minutes.html)

### Add TypeScript to the project

To enable TypeScript for your project we need to add `tsconfig.json` file in our project root which indicates project as TypeScript project and configures compile rules and files which considered to be TypeScript files.

Here's simple minimal TS Config example:

```json
{
  "compilerOptions": {
    "target": "ES2015",
    "module": "commonjs",
    "esModuleInterop": true,
    "skipLibCheck": true
  }
}
```

For real project we will need to add some more configurations - here's all [config properties](https://www.typescriptlang.org/tsconfig)

Also, there's predefined [configs](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html#tsconfig-bases) from TypeScript for different use cases

### Get familiar with TypeScript building blocks

To feel a little bit comfortable with TypeScript we will start from [TS handbook](https://www.typescriptlang.org/docs/handbook/intro.html). It describes all concepts needed to start - which basic types are there, how to use interfaces and cover our functions with types and much more.

## What's next?

Start using TypeScript and try to not use `any` :)

Also, we recommend u to read [Everyday types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html).

For more inspiration, some TS patterns, and deeper understanding there's a good article about [Advanced Types](https://www.typescriptlang.org/docs/handbook/advanced-types.html)
