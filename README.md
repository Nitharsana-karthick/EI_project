# EI_project
# Exercise 1
A console-based Java project demonstrating 6 fundamental design patterns across Behavioral, Creational, and Structural categories.
This project showcases Object-Oriented Programming (OOP), SOLID principles, and proper design pattern application.

# Features

Behavioral Patterns
Observer: Real-time notification system (e.g., Weather Station & Displays).
Strategy: Selectable algorithm at runtime (e.g., Payment System).

Creational Patterns
Singleton: Ensures a single instance (e.g., Logger).
Factory: Creates objects without exposing instantiation logic (e.g., Shapes).

Structural Patterns
Adapter: Converts interface to be compatible with client (e.g., Voltage converter).
Decorator: Dynamically adds behavior to objects (e.g., Coffee with Milk/Sugar).

Interactive user input for all examples.
Each design pattern is implemented correctly and independently.
Easy-to-extend code for practice or learning new patterns.

##  Project Structure

Exercise1/
 ├── src/
 │    ├── Behavioral/
 │    │     ├── ObserverDemo.java        # Observer pattern with user input
 │    │     └── StrategyDemo.java        # Strategy pattern with user input
 │    ├── Creational/
 │    │     ├── SingletonDemo.java       # Singleton pattern with user input
 │    │     └── FactoryDemo.java         # Factory pattern with user input
 │    ├── Structural/
 │    │     ├── AdapterDemo.java         # Adapter pattern with user input
 │    │     └── DecoratorDemo.java       # Decorator pattern with user input
 └── README.md                             # Project documentation


# How to run
cd src/Behavioral       # For Observer or Strategy
cd src/Creational       # For Singleton or Factory
cd src/Structural       # For Adapter or Decorator

#Compile
javac ObserverDemo.java

#Run
java ObserverDemo

# Design Decisions

Observer Pattern: Implements one-to-many dependency; observers automatically update when the subject changes.
Strategy Pattern: Algorithms are encapsulated and interchangeable at runtime.
Singleton Pattern: Guarantees a single instance across the system.
Factory Pattern: Encapsulates object creation logic; client uses interface only.
Adapter Pattern: Converts incompatible interfaces to make them compatible.
Decorator Pattern: Adds functionality dynamically without modifying the original class.
Separation of Concerns: Each pattern is in its own file/folder.
User Input Integration: All patterns accept input at runtime for testing.
Extensibility: Easy to add new patterns or extend existing ones.

# Exercise 2
# Satellite Command System 

A console-based simulation of a **Satellite Command System** built in **Java**.
This project demonstrates **Object-Oriented Programming (OOP)**, **SOLID principles**, and the **Command Design Pattern**.

---

##  Features

* Rotate satellite in 4 directions: `North`, `South`, `East`, `West`.
* Activate or deactivate solar panels.
* Collect data (only if solar panels are active).
* Command Pattern implementation for clean and extensible command handling.
* Defensive coding with **error handling** and **input validation**.
* Easy-to-extend design (new commands can be added without changing existing logic).

---

##  Project Structure

```
SatelliteCommandSystem/
 ├── src/
 │    ├── Main.java                  # Entry point – reads user input, invokes commands
 │    ├── Satellite.java              # Represents satellite state and operations
 │    ├── Command.java                # Command interface
 │    ├── RotateCommand.java          # Rotate satellite
 │    ├── ActivatePanelsCommand.java  # Activate solar panels
 │    ├── DeactivatePanelsCommand.java# Deactivate solar panels
 │    ├── CollectDataCommand.java     # Collects data (if panels active)
 │    └── CommandInvoker.java         # Executes commands
 └── README.md                        # Documentation
```

---

##  Tech Stack

* **Language:** Java (JDK 8 or higher)
* **Paradigms:** OOP, SOLID principles
* **Design Patterns:** Command Pattern

---

##  How to Run

1. **Navigate to project folder:**

   ```bash
   cd SatelliteCommandSystem/src
   ```

2. **Compile the code:**

   ```bash
   javac *.java
   ```

3. **Run the program:**

   ```bash
   java Main
   ```

---

##  Example Usage

```
 Satellite Command System Started
Available commands: rotate <North|South|East|West>, activatePanels, deactivatePanels, collectData, exit

Enter command: rotate South
 Satellite rotated to South
 Current State → Orientation: South, Solar Panels: Inactive, Data Collected: 0

Enter command: activatePanels
 Solar panels activated.
 Current State → Orientation: South, Solar Panels: Active, Data Collected: 0

Enter command: collectData
 Data collected: +10 units.
 Current State → Orientation: South, Solar Panels: Active, Data Collected: 10
```

---

##  Design Decisions

* **Command Pattern**: Each action (`rotate`, `activatePanels`, `collectData`, etc.) is encapsulated as a separate class, ensuring **Open/Closed Principle** compliance.
* **Encapsulation**: Satellite state is private and updated only via methods.
* **Separation of Concerns**: Input handling is in `Main.java`, logic is in `Satellite.java`, and command execution is handled by `CommandInvoker`.
* **Extensibility**: Adding new commands requires only creating a new command class.

---

