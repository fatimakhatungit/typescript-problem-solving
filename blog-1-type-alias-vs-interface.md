# What are the core differences between type aliases and interface in TypeScript? When should you choose one over the other?
## Introduction

TypeScript is a superset of JavaScript that adds static type checking. It helps developers catch many type-related errors during development. It also provides better IDE support and makes code easier to maintain. Type Alias and Interface are two important features that help us define and organize types in TypeScript.

## What is a Type Alias?

A Type Alias is a custom name for a type. We create it using the `type` keyword. It can represent primitive, object, union, and tuple types.

```ts
type Status = "active" | "inactive";

type Coordinate = [number, number];
```

Here, `Status` allows only two specific values, and `Coordinate` represents a tuple containing two numbers.

## What is an Interface?

An Interface describes the structure of an object. We create it using the `interface` keyword. It defines the properties and their types that an object should have.

```ts
interface Course {
  title: string;
  students: number;
  isPublished: boolean;
}
```

This Interface describes a course with three properties.

## Key Differences

Both Type Alias and Interface can define object structures, but they have some differences.

A Type Alias can directly represent union types, while an Interface cannot directly define a union type.

Interfaces support declaration merging. It means we can declare the same Interface more than once, and TypeScript combines their properties. Type Aliases do not support declaration merging.

We can extend an Interface using the `extends` keyword. With Type Aliases, we can combine types using the intersection (`&`) operator.

## Conclusion

Both Type Alias and Interface are useful in TypeScript. I prefer using Interfaces for defining object structures and Type Aliases for union types and other complex type definitions. The choice depends on the project requirements and coding style.