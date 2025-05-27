# 📘 Dart Essentials – Summary

A quick reference to key Dart programming concepts including object handling, control flow, function types, OOP principles, design patterns, and Flutter routing.

---

## 🚀 1. Cascade Operators (`..`)

Allows multiple operations on the same object without repeating its name.

### ✅ Example

```dart
var person = Person()
  ..setName('Alice')
  ..setAge(30)
  ..greet();
```

### 🔹 Use When:

* Initializing and modifying the same object fluently.
* Writing cleaner and shorter object setup code.

---

## 🧱 2. Method Calling in Classes

### Without Cascade:

```dart
var car = Car();
car.start();
car.drive();
```

### With Cascade:

```dart
var car = Car()
  ..start()
  ..drive();
```

---

## 🔄 3. `.` vs `..`

| Operator | Action                   | Returns              |
| -------- | ------------------------ | -------------------- |
| `.`      | Call method or get value | Result of the method |
| `..`     | Cascade multiple calls   | Original object      |

---

## 🧠 4. Tracing Code

Step-by-step analysis of how code executes.

### Example

```dart
void main() {
  String user = 'Alice';
  greet(user); // Traces to: Hello, Alice
}
```

Used for debugging, code comprehension, and learning.

---

## 🧭 5. Design Principles

| Principle | Description                  |
| --------- | ---------------------------- |
| DRY       | Don't repeat yourself        |
| KISS      | Keep it simple               |
| YAGNI     | Don't build it unless needed |
| SOLID     | Five core OOP principles     |

### 🔹 SOLID Breakdown

* **S**: Single Responsibility
* **O**: Open/Closed
* **L**: Liskov Substitution
* **I**: Interface Segregation
* **D**: Dependency Inversion

---

## 🧩 6. Design Patterns

Reusable solutions to common software problems.

| Category   | Examples                    |
| ---------- | --------------------------- |
| Creational | Singleton, Factory          |
| Structural | Adapter, Decorator          |
| Behavioral | Observer, Strategy, Command |

### ✅ Singleton Example:

```dart
class Logger {
  static final Logger _instance = Logger._internal();
  Logger._internal();

  factory Logger() => _instance;

  void log(String msg) => print('Log: $msg');
}
```

---

## 🌐 7. Routing in Flutter

Used to navigate between screens.

### Named Routes

```dart
MaterialApp(
  routes: {
    '/': (context) => HomePage(),
    '/about': (context) => AboutPage(),
  },
);
Navigator.pushNamed(context, '/about');
```

### Direct Route

```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => AboutPage()),
);
```

---

## 🎯 8. Switch Statement & Ranges

### ❌ Invalid (Dart pre-3.0):

```dart
case >= 90: // Not allowed
```

### ✅ If-Else Alternative:

```dart
if (grade >= 90) print('A');
```

### ✅ Dart 3 Pattern Matching:

```dart
switch (grade) {
  case >= 90:
    print('A');
    break;
}
```

---

## 🔧 9. Types of Functions in Dart

| Type      | Syntax                  | Use Case            |
| --------- | ----------------------- | ------------------- |
| Named     | `void greet() {}`       | Reusable functions  |
| Anonymous | `(x) { return x * 2; }` | Inline callbacks    |
| Arrow     | `(x) => x * 2`          | One-liner shorthand |

---

### 📌 Function Examples

#### Named Function:

```dart
void greet(String name) {
  print('Hello, $name');
}
```

#### Anonymous Function:

```dart
var list = [1, 2, 3];
list.forEach((num) {
  print(num * 2);
});
```

#### Arrow Function:

```dart
int square(int x) => x * x;
```

---

## ✅ Summary Table

| Concept               | Use It For                               |
| --------------------- | ---------------------------------------- |
| `..` Cascade          | Fluent configuration                     |
| `.` Method Call       | Normal property/method access            |
| Tracing Code          | Debugging & learning flow                |
| Design Principles     | Writing scalable, clean code             |
| Design Patterns       | Solving common design problems           |
| Routing in Flutter    | Navigation between screens               |
| Dart 3 Switch Pattern | Cleaner range logic in switch statements |
| Function Types        | Different function writing styles        |

