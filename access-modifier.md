# Explain how Access Modifiers (public, private, protected, and readonly) work in TypeScript OOP with examples.

## Introduction

In TypeScript Object-Oriented Programming (OOP), access modifiers are used to control access to a class properties and methods.These are used to determine whether a property or method of a class can be accessed from outside of the class or only from within the class itself or from a child class.In TypeScript the primary access modifiers used are public,private , protected and readonly.

## Detailed Body

### 1. Public Modifier

If we use public then the property or method of the class can be accessed from anywhere.It is a default access modifier in TypeScript.

**Example**

```typescript
class Student {
  public name: string = "Jobayer";
}

let student = new Student();

console.log(student.name);
```

Here the name property can be access from outside

### 2. Private Modifier

When private is used, a property or method can only be accessed from within its own class; it cannot be accessed directly from outside.

**Example**

```typescript
class Student {
  private age: number = 22;
}

let student = new Student();

// console.log(student.age); // Error
```

Here , age can only be accessed from Student class.

### 3. Protected Modifier

When protected is used, a property or method can be accessed from within its own class and its child classes. However, it cannot be accessed directly from outside the class.

**Example**

```typescript
class Person {
  protected name: string = "Jobayer";
}

class Student extends Person {
  showName() {
    console.log(this.name);
  }
}
```

Here, Student is a child class of Person. Therefore, it is able to use the name property.

### 4. ReadOnly Modifier

When readonly is used, the value of a property cannot be changed once it has been set. Typically, this value is assigned either at the time of declaration or within a constructor.

**Example**

```typescript
class Student {
  readonly id: number = 101;
}

let student = new Student();

console.log(student.id);

// student.id = 102; // Error
```

Here the value of id won’t be changed.

## Conclusion

In conclusion, access modifiers in TypeScript OOP play a crucial role in controlling class data and methods. public makes access open to everyone, private restricts access to the class itself, protected allows access to child classes, and readonly prevents the value of a property from being changed. Using the appropriate access modifiers makes code more secure, organized, and easier to maintain.
