
LearnTrack - Console-based Student and Course Management

This is a simple console application for practicing core Java. It focuses on basics like classes, objects, constructors, encapsulation, simple inheritance, ArrayList, and basic exception handling. All data is kept in memory.

How to compile and run

Using terminal
1. make sure JDK is installed
2. from project root:
   mkdir -p bin
   find ./src -name "*.java" > sources.txt
   javac -d bin @sources.txt
   java -cp bin com.airtribe.learntrack.ui.Main

Using an IDE
1. open the project in IntelliJ IDEA or VS Code
2. mark src as sources root if needed
3. run com.airtribe.learntrack.ui.Main

Features
1. student management: add, list, search by id, update, deactivate
2. course management: add, list, activate/deactivate, update
3. enrollment management: enroll student, list by student, update status

Package overview
- entity: Person, Student, Trainer, Course, Enrollment, EnrollmentStatus
- service: StudentService, CourseService, EnrollmentService
- exception: EntityNotFoundException, InvalidInputException
- util: IdGenerator, InputValidator
- ui: Main (console menu)

Class diagram (mermaid)
```mermaid
classDiagram
    class Person {
      -int id
      -String firstName
      -String lastName
      -String email
      +getDisplayName()
    }
    class Student {
      -String batch
      -boolean active
      +getDisplayName()
    }
    class Trainer {
      -String specialization
      +getDisplayName()
    }
    class Course {
      -int id
      -String courseName
      -String description
      -int durationInWeeks
      -boolean active
    }
    class Enrollment {
      -int id
      -int studentId
      -int courseId
      -LocalDate enrollmentDate
      -EnrollmentStatus status
    }
    enum EnrollmentStatus {
      ACTIVE
      COMPLETED
      CANCELLED
    }

    Person <|-- Student
    Person <|-- Trainer
    EnrollmentStatus <.. Enrollment
