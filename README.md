# 🧮 Graphical Calculator

A standalone Graphical Calculator application featuring arithmetic evaluation, scientific functions, and interactive graph plotting.

## 🚀 Overview

The **Graphical Calculator** is designed as a premium, standalone tool for students, educators, and professionals. It operates entirely offline with no external dependencies.

### Key Features
* **Core Calculation**: High-precision arithmetic and scientific functions.
* **Graphing Engine**: Plot functions like `f(x) = sin(x)` with zooming and panning.
* **Equation Solver**: Solve linear and quadratic equations (including complex roots).
* **History Management**: View and reuse previous calculations.

---

## 🏗️ Technical Architecture (GASD)

This project follows the **General Agentic Software Design (GASD)** specification.

### Generating GASD from User Stories
To generate or update the system design from requirements, follow the steps outlined in [Build Plan.md](file:///Users/ming/Anitgarvity/Graphical%20Calculator/Build/Build%20Plan.md):

1. **Reference Specification**: Read [gasd-1.0.0.gasd](file:///Users/ming/Anitgarvity/Graphical%20Calculator/gasd-1.0.0.gasd) to understand the official syntax and keywords.
2. **Review Requirements**: Analyze the [User Stories.md](file:///Users/ming/Anitgarvity/Graphical%20Calculator/Requirements/User%20Stories.md).
3. **Draft Design**: Generate GASD files using official keywords (e.g., `TRACE`, `MATCH`, `ENSURE`).
4. **Placement**: Save all `.gasd` files in the [Design/](file:///Users/ming/Anitgarvity/Graphical%20Calculator/Design/) folder.
5. **Review**: Request a human architectural review before proceeding to implementation.

---

## 💻 Running the Application

The application is implemented in Java using Swing for the UI.

### Prerequisites
* Java Development Kit (JDK) 8 or higher.

### Compile and Run
Navigate to the project root and run the following commands:

```bash
# Compile the source code
javac -d bin Implementation/src/org/calculator/*.java

# Run the Graphical Calculator UI
java -cp bin org.calculator.CalculatorUI
```

### Headless Verification
To run a feature verification demo (no UI):
```bash
java -cp bin org.calculator.DemoRunner
```

---

## 📂 Project Structure

* `Build/`: GASD build plans and meta-design.
* `Design/`: Official GASD design specifications.
* `Implementation/`: Java source code and compiled classes.
* `Requirements/`: Product requirements and user stories.
* `gasd-1.0.0.gasd`: The authoritative GASD language specification.
