# What is Index Signatures in Typescript?

Index signatures allows to define a type for objects with a flexible set of
properties, where the property names aren't known in advances but follow a
specific pattern.

The purpose of this feature is to type objects with dynamic property names. \
Useful in defining types to external API responses.

```ts
// Syntax
interface DynamicObject {
    [key: string]: ValueType
}

// Example
interface Response {
    [userId: number]: string
}
```

The `userId` is arbitrary and can be labeled with anything.
