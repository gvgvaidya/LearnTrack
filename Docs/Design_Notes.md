
Design notes

Why ArrayList instead of array
- dynamic resizing is helpful when the number of items is not known in advance
- ArrayList offers methods like add and remove, which simplifies code

Use of static members
- IdGenerator maintains counters for IDs
- static methods like getNextStudentId ensure a single sequence across the app

Inheritance and polymorphism
- Person is a base class
- Student and Trainer extend Person
- getDisplayName is overridden to show role-specific text
- this reduces duplication and allows reuse

Separation of concerns
- entity classes store data
- service classes perform operations and hold in-memory lists
- ui reads input and prints output, and calls service methods
- exceptions signal problems without crashing

Clean code choices
- small methods with clear names
- private fields with getters and setters to encapsulate state
- basic input validation to avoid bad state
