# 🏗️ Design Patterns in Java

A **comprehensive collection** of classic software design patterns implemented in Java. This repository serves as a practical reference guide for developers learning object-oriented design principles and preparing for technical interviews.

![Java](https://img.shields.io/badge/Java-17+-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Design Patterns](https://img.shields.io/badge/Design%20Patterns-Gang%20of%20Four-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 📖 About

This repository contains clean, well-documented implementations of the most important design patterns from the **Gang of Four** book. Each pattern includes:
- Real-world use cases
- Step-by-step implementation
- Working code examples
- Comments explaining design decisions

Perfect for developers who want to write better, more maintainable code.

---

## 🎯 What are Design Patterns?

Design patterns are **reusable solutions** to common problems in software design. They represent best practices refined over decades of software engineering experience.

### Why Learn Design Patterns?

- **Write cleaner code** - Solve problems with proven solutions
- **Better communication** - Use industry-standard terminology
- **Ace interviews** - Essential knowledge for FAANG and top tech companies
- **Build maintainable systems** - Create flexible, extensible architectures
- **Understand frameworks** - Most frameworks are built using design patterns

---

## 📚 Patterns Implemented

### Creational Patterns
Design patterns that deal with object creation mechanisms.

| Pattern | Description | Use Case |
|---------|-------------|----------|
| **[Singleton](./Singleton%20method)** | Ensure a class has only one instance | Database connections, loggers, configuration managers |
| **[Factory Method](./Factory%20method)** | Create objects without specifying exact class | UI frameworks, document generators |
| **[Abstract Factory](./Abstract%20factory%20method)** | Create families of related objects | Cross-platform UI toolkits, theme systems |
| **[Builder](./Builder%20method)** | Construct complex objects step-by-step | Building immutable objects, configuration objects |

### Structural Patterns
Patterns that deal with object composition and relationships.

| Pattern | Description | Use Case |
|---------|-------------|----------|
| **[Adapter](./Adapter%20method)** | Make incompatible interfaces work together | Legacy system integration, third-party APIs |

### Behavioral Patterns
*(Coming soon!)* Patterns that focus on communication between objects.

- **Observer** - Event handling systems
- **Strategy** - Payment processing, sorting algorithms
- **Command** - Undo/redo functionality
- **State** - Workflow engines, game character states
- And more...

---

## 🚀 Quick Start

### Prerequisites

- **Java 11+** installed
- Basic understanding of OOP concepts
- Any Java IDE (IntelliJ IDEA, Eclipse, VS Code)

### Running the Examples

1. **Clone the repository**
```bash
   git clone https://github.com/GOUTHAM-2002/DesignPatterns-Java.git
   cd DesignPatterns-Java
```

2. **Navigate to a pattern**
```bash
   cd "Singleton method"
```

3. **Compile and run**
```bash
   javac *.java
   java Main
```

4. **Explore the code**
   - Read through the implementation
   - Modify and experiment
   - Understand when to use each pattern

---

## 📂 Repository Structure
```
DesignPatterns-Java/
├── Singleton method/
│   ├── Singleton.java
│   ├── Main.java
│   └── README.md
├── Factory method/
│   ├── Factory.java
│   ├── Product.java
│   ├── ConcreteProducts.java
│   └── README.md
├── Abstract factory method/
│   ├── AbstractFactory.java
│   ├── ConcreteFactories.java
│   └── README.md
├── Builder method/
│   ├── Builder.java
│   ├── Product.java
│   └── README.md
├── Adapter method/
│   ├── Adapter.java
│   ├── Target.java
│   └── README.md
└── README.md
```

---

## 🎓 Learning Path

### For Beginners
1. Start with **Singleton** - simplest pattern
2. Move to **Factory Method** - introduces abstraction
3. Try **Builder** - useful for real projects
4. Learn **Adapter** - common in integration scenarios

### For Interview Prep
Focus on:
- **Singleton** (thread-safe implementation)
- **Factory** vs **Abstract Factory**
- **Builder** pattern advantages
- When to use each pattern

### For Production Code
Master:
- **Factory patterns** for object creation
- **Builder** for complex configurations
- **Adapter** for third-party integrations
- **Strategy** and **Observer** (coming soon)

---

## 💡 Pattern Summary Cards

### Singleton Pattern
```java
// Thread-safe Singleton
public class Singleton {
    private static volatile Singleton instance;
    
    private Singleton() {}
    
    public static Singleton getInstance() {
        if (instance == null) {
            synchronized (Singleton.class) {
                if (instance == null) {
                    instance = new Singleton();
                }
            }
        }
        return instance;
    }
}
```
**When to use**: Database connections, configuration managers, thread pools

---

### Factory Method Pattern
```java
// Product interface
interface Product {
    void use();
}

// Factory
abstract class Creator {
    abstract Product createProduct();
}
```
**When to use**: When you don't know exact types/dependencies beforehand

---

### Builder Pattern
```java
// Builder for complex objects
public class User {
    private final String name;
    private final int age;
    
    private User(Builder builder) {
        this.name = builder.name;
        this.age = builder.age;
    }
    
    public static class Builder {
        private String name;
        private int age;
        
        public Builder setName(String name) {
            this.name = name;
            return this;
        }
        
        public Builder setAge(int age) {
            this.age = age;
            return this;
        }
        
        public User build() {
            return new User(this);
        }
    }
}
```
**When to use**: Objects with many optional parameters

---

## 🔧 Common Interview Questions

### Frequently Asked

1. **What is the difference between Factory and Abstract Factory?**
   - Factory creates one product
   - Abstract Factory creates families of related products

2. **Why is Singleton considered an anti-pattern?**
   - Makes testing difficult
   - Global state issues
   - Consider Dependency Injection instead

3. **When would you use the Builder pattern?**
   - Many constructor parameters
   - Immutable objects
   - Step-by-step construction needed

4. **What are the downsides of the Adapter pattern?**
   - Adds complexity
   - Extra indirection
   - May impact performance

---

## 🚀 Roadmap

- [x] Singleton Pattern
- [x] Factory Method Pattern
- [x] Abstract Factory Pattern
- [x] Builder Pattern
- [x] Adapter Pattern
- [ ] Decorator Pattern
- [ ] Observer Pattern
- [ ] Strategy Pattern
- [ ] Command Pattern
- [ ] State Pattern
- [ ] Template Method Pattern
- [ ] Proxy Pattern
- [ ] Composite Pattern
- [ ] Facade Pattern
- [ ] Chain of Responsibility

---

## 📖 Additional Resources

### Books
- **"Design Patterns: Elements of Reusable Object-Oriented Software"** - Gang of Four (Must-read!)
- **"Head First Design Patterns"** - Eric Freeman (Great for beginners)
- **"Refactoring to Patterns"** - Joshua Kerievsky

### Online Resources
- [Refactoring.Guru](https://refactoring.guru/design-patterns) - Interactive diagrams
- [SourceMaking](https://sourcemaking.com/design_patterns) - Clear explanations
- [Java Design Patterns](https://java-design-patterns.com/) - Java-specific examples

### Video Tutorials
- "Design Patterns" by Christopher Okhravi (YouTube)
- Udemy courses on design patterns
- Pluralsight design patterns path

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Add new patterns** - Implement missing patterns
2. **Improve documentation** - Add clearer explanations
3. **Add real-world examples** - Show practical use cases
4. **Fix bugs** - Report or fix issues
5. **Add tests** - Write unit tests for patterns

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/NewPattern`)
3. Follow existing code structure
4. Add clear comments and documentation
5. Commit your changes (`git commit -m 'Add Strategy Pattern'`)
6. Push to the branch (`git push origin feature/NewPattern`)
7. Open a Pull Request

---

## 📝 Code Style

- Use descriptive variable names
- Add comments explaining "why", not "what"
- Follow Java naming conventions
- Keep classes focused and single-purpose
- Include a `Main.java` with usage examples

---

## 🎯 Who is This For?

- **Students** learning object-oriented design
- **Junior developers** preparing for interviews
- **Senior developers** needing a quick reference
- **Anyone** wanting to write better code

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

**Goutham N**

- GitHub: [@GOUTHAM-2002](https://github.com/GOUTHAM-2002)
- Email: goutham3336@gmail.com
- LinkedIn: [Connect with me](https://www.linkedin.com/in/goutham-n/)

---

## 🌟 Show Your Support

If this repository helped you:
- ⭐ **Star** this repo
- 🍴 **Fork** it for your own learning
- 📢 **Share** with fellow developers
- 💬 **Provide feedback** via issues

---

## 🙏 Acknowledgments

- Gang of Four for defining these patterns
- The Java community for continuous learning
- All contributors who help improve this repository

---

**Happy Coding! 🚀**

*"Design patterns are not about code, they're about communication and solving problems elegantly."*
