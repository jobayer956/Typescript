# What are the core differences between type aliases and interface in TypeScript? When should you choose one over the other?

## Introduction

Type Alias and interface both are used in TypeScript to decide the shape and structure of data.Through these we can specify the properties ,data types and function structures of an object.But there is some important difference between them. Using the right approach in the right situation makes code cleaner, easier to maintain, and reusable.

## Detailed Body

### Type Alias

Using type, we can define a data type under a new name. It can be used to create object, primitive, union, and intersection types.

```typescript
Type Student = {

name : string;

age : number;

};

Let student : Student = {

 name : “Jobayer”,

Age : 22

};
```

Here Student is a type alias, which specify the student name and age

### Interface

It is basically used to specify the structure of an object.It is useful in Object Oriented Programmin(OOP).

```typescript
interface Student {

    name: string;

    age: number;

}

let student: Student = {

    name: "Jobayer",

    age: 22

};
```

Here, for the student object a specific structure has been created.

### Difference between Type Alias and Interface

The most important difference is that type can be used to create primitive, union, and intersection types. On the other hand, interface is primarily used to define object structures.

Example :

```typescript
type Status = “Active” | “Inactive”;

interface User {

    name: string;

}
```

Another Differnce is multiple interfaces with the same name can automatically be merged but type alias with the same name can’t be declared a second time.

Example

```typescript
interface User {

    name: string;

}

interface User {

    age: number;

}
```

Here, two interfaces are combined to include both the name and age properties.

## Conclusion

In conclusion, both type and interface are important in TypeScript. It is generally better to use interface for defining standard object structures, whereas type is more suitable for creating unions, intersections, primitives, and complex types. However, in many cases, either can be used.Therefore, we should choose the one that best fits out project's requirements and the nature of our code.