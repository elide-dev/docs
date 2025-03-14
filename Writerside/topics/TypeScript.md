# TypeScript

%product% can run TypeScript using the built-in [JavaScript engine](JavaScript.md).

```Console
elide ./script.{ts,cts,mts}
```
```Typescript
export function hello(name: string): void {
  console.log(`Hello from TypeScript, ${name}!`)
}
```

## Language Engine

%product% can execute TypeScript under the following conditions.

| -------- | ---------------------------------------------------- |
| Language | **TypeScript**                                       |
| Standard | `5.8.x`                                              |
| Maturity | ![Beta](https://img.shields.io/badge/-beta-purple)   |
| Engine   | [GraalJs](https://github.com/oracle/graaljs) + [OXC](https://oxc.rs)               |
