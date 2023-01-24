# Introduction to Dart

## Few Notes on Dart

### Object-oriented language

- objects, classes

### Statically typed

- variables contain data of a single type

### C-Style Syntax

- syntax is similar to C, C#, JS

### Multiple Runtime Environments

- transpiled to JS to run in the browser
- runs in the `Dart VM` to execute from a command line
- compiled to machine code to run on mobile devices

---

## Dartpad Editor

> [DartPad](https://dartpad.dartlang.org/)

### Code Examples

```dart
void main() {
  for (int i = 0; i < 5; i++) {
    print('hello ${i + 1}');
  }
}
```

```dart
// dart finds and runs the `main` function
void main() {
  var name = myName();

  print('My name is $name');
}
// annotate return type
String myName() {
  return 'Brandon';
}
```

---

## Types in Dart

- every value and variable has a type
- a variable's type can reference
- a variable's type cannot be changed once assigned
- Dart can guess the type of a variable

```dart
String name = 'Brandon';
int age = 38;
double height = 5.9;
dynamic weakType = 'Brandon' | 38 | 5.9;
```

---

## String

> _**interpolation**_: the insertion of something of a different nature into something else.

- string interpolation

  ```dart
  String name = 'Brandon';
  print('My name is $name');
  print('My name is ${name.length}');
  ```

---

## Object-oriented programming

### Class

```dart
class Person {
  String firstName;
  // above causing non-nullable instance field error
  // solution #1
  Person(this.firstName); // `this` is a must
  // solution #2
  String? firstName;

  printName() {
    print(this.firstName); // `this` not required
    print(firstName); // Dart will understand
  }
}
```

### Constructor

```dart
void main() {
  var person = new Person('Brandon');
  person.printName();
}

class Person {
  String? firstName;
  // style #1
  Person(String name) {
    this.firstName = name;
  }
  // style #2
  Person(this.firstName);

  printName() {
    print(this.firstName);
  }
}
```
