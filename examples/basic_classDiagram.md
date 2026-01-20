# Basic Class Diagram Example

Class diagrams are used to represent the structure of a system by showing classes, their attributes, methods, and relationships.

## Simple Class Diagram

```mermaid
classDiagram
    class Animal {
        +String name
        +int age
        +makeSound()
    }
    class Dog {
        +String breed
        +bark()
    }
    class Cat {
        +String color
        +meow()
    }
    Animal <|-- Dog
    Animal <|-- Cat
```

## Class Diagram with Relationships

```mermaid
classDiagram
    class Vehicle {
        +String model
        +int year
        +start()
        +stop()
    }
    class Car {
        +int doors
        +openTrunk()
    }
    class Motorcycle {
        +String type
        +wheelie()
    }
    Vehicle <|-- Car
    Vehicle <|-- Motorcycle
    Car "1" --> "4" Wheel : has
    Motorcycle "1" --> "2" Wheel : has
    class Wheel {
        +int diameter
        +rotate()
    }
```

## Resources

- [Mermaid Class Diagram Documentation](https://mermaid.js.org/syntax/classDiagram.html)
