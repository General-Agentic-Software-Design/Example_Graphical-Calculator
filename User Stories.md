
# 🧮 Graphical Calculator Web App

## Product Requirements, Epics, User Stories & UX Markup

*(Standalone Client-Side Application)*

---

# 📘 1. Product Overview

The **Graphical Calculator Web App** is a fully standalone, browser-based application that enables users to:

* Perform arithmetic and scientific calculations
* Plot mathematical functions
* Interact with graphs
* Solve equations
* View and reuse calculation history
* Operate entirely offline

There are **no backend services**, **no APIs**, and **no external dependencies** required.

---

# 🎯 2. Target Users

| Persona           | Description                           |
| ----------------- | ------------------------------------- |
| Student (Primary) | High school / university STEM student |
| Educator          | Demonstrating math visually           |
| Professional      | Quick scientific calculations         |

---

# 🧩 3. EPICS & USER STORIES

---

# 🧩 EPIC 1: Core Calculation Engine

## Goal

Enable fast and accurate mathematical computation.

---

### 🧾 User Story 1.1 – Basic Arithmetic

**As a** user
**I want** to perform +, −, ×, ÷
**So that** I can calculate quickly

#### Acceptance Criteria

* Supports parentheses
* Follows PEMDAS
* "=" evaluates expression
* Division by zero shows clear error
* No app crashes

---

### 🧾 User Story 1.2 – Decimal Precision

**As a** user
**I want** accurate decimal calculations
**So that** floating-point errors are minimized

#### Acceptance Criteria

* Up to 12 decimal places
* Correct rounding
* Stable under repeated operations

---

### 🧾 User Story 1.3 – Real-Time Validation

**As a** user
**I want** immediate feedback on invalid input
**So that** I can correct mistakes quickly

#### Acceptance Criteria

* Invalid syntax detected
* Clear error messages
* Error position highlighted

---

# 🧩 EPIC 2: Scientific Functions

---

### 🧾 User Story 2.1 – Trigonometric Functions

Supports:

* sin, cos, tan
* inverse trig
* Degree/Radian toggle

Acceptance Criteria:

* Accurate results
* Domain validation
* Mode switch affects output

---

### 🧾 User Story 2.2 – Logarithmic & Exponential Functions

Supports:

* log, ln
* exponentiation
* sqrt
* factorial

Acceptance Criteria:

* Domain errors handled
* Correct scientific output

---

# 🧩 EPIC 3: Graph Plotting

---

### 🧾 User Story 3.1 – Plot Function

**As a** user
**I want** to input f(x)
**So that** I can visualize it

Acceptance Criteria:

* Cartesian grid
* Smooth rendering
* Auto-scale option

---

### 🧾 User Story 3.2 – Zoom & Pan

Acceptance Criteria:

* Zoom in/out controls
* Drag to pan
* Reset view button

---

### 🧾 User Story 3.3 – Multiple Functions

Acceptance Criteria:

* Multiple function inputs
* Color-coded lines
* Legend display

---

# 🧩 EPIC 4: Graph Interaction

---

### 🧾 User Story 4.1 – Hover Coordinates

Acceptance Criteria:

* Real-time (x,y) display
* Precision formatting

---

### 🧾 User Story 4.2 – Detect Key Points

Acceptance Criteria:

* Detect intercepts
* Approximate extrema
* Highlight visually

---

# 🧩 EPIC 5: Equation Solving

---

### 🧾 User Story 5.1 – Linear Equations

Acceptance Criteria:

* Solve single-variable linear equations
* Display formatted result

---

### 🧾 User Story 5.2 – Quadratic Equations

Acceptance Criteria:

* Real and complex roots supported
* Clear formatted display

---

# 🧩 EPIC 6: Calculation History

---

### 🧾 User Story 6.1 – View History

Acceptance Criteria:

* Scrollable history panel
* Stored in browser storage
* Includes expression + result

---

### 🧾 User Story 6.2 – Reuse Entry

Acceptance Criteria:

* Click repopulates input
* Editable after selection

---

# 🧩 EPIC 7: Offline & Performance

---

### 🧾 User Story 7.1 – Offline Use

Acceptance Criteria:

* Fully functional without internet
* No external calls

---

### 🧾 User Story 7.2 – Fast Response

Acceptance Criteria:

* Expression evaluation < 50ms
* Graph render < 200ms
* No UI blocking

---

# 🧩 EPIC 8: Usability & Accessibility

---

### 🧾 User Story 8.1 – Keyboard Support

Acceptance Criteria:

* Full keyboard entry
* Enter triggers evaluation
* Shortcuts supported

---

### 🧾 User Story 8.2 – Responsive Design

Acceptance Criteria:

* Works on desktop & tablet
* Scalable graph canvas
* Touch-friendly buttons

---

# 🎨 4. UX MARKUP (Low-Fidelity Wireframes)

---

# 🖥 4.1 Main Calculator View

```
 -------------------------------------------------------
| Graphical Calculator                                 |
|------------------------------------------------------|
| Expression: [ 2*sin(45) + 5^2               ]  [=] |
|------------------------------------------------------|
| Result:  26.4142                                     |
|------------------------------------------------------|
| [Calculator] [Graph] [History]                       |
|------------------------------------------------------|
| Buttons:                                             |
| [7][8][9][÷][sin]                                    |
| [4][5][6][×][cos]                                    |
| [1][2][3][-][tan]                                    |
| [0][.][=][+][log]                                    |
| [π][e][√][^][()]                                     |
|------------------------------------------------------|
| Mode: (● DEG) (○ RAD)                                |
 -------------------------------------------------------
```

---

# 📈 4.2 Graph View

```
 -------------------------------------------------------
| Function: [ x^2 - 4 ] [Plot]                        |
|------------------------------------------------------|
|                                                      |
|                  GRAPH CANVAS                        |
|                                                      |
|         +--------------------------------+          |
|         |                                |          |
|         |         Cartesian Grid          |          |
|         |                                |          |
|         +--------------------------------+          |
|                                                      |
|------------------------------------------------------|
| Zoom: [-] [+]  Reset  Auto-Scale                    |
| Coordinates: (x: 1.23 , y: -2.45)                   |
 -------------------------------------------------------
```

---

# 📜 4.3 History Panel

```
 -------------------------------------------------------
| History                                              |
|------------------------------------------------------|
| 2 + 2 = 4                                            |
| sin(90) = 1                                          |
| x^2 - 4  → plotted                                   |
| 5! = 120                                             |
|------------------------------------------------------|
| [Clear History]                                      |
 -------------------------------------------------------
```

---

# 🔄 5. Interaction Flow

---

## Evaluate Expression Flow

1. User types expression
2. Clicks "=" or presses Enter
3. Expression validated
4. AST built
5. Result calculated
6. Result displayed
7. Saved to local history

---

## Graph Plot Flow

1. User enters function
2. Clicks "Plot"
3. Input validated
4. Points sampled
5. Canvas renders graph
6. Hover displays coordinates

---

# 🏁 6. Definition of Done

The application is complete when:

* All user stories meet acceptance criteria
* Works fully offline
* No unhandled runtime errors
* No use of unsafe eval execution
* Graph rendering is smooth
* History persists locally
* UI responsive across devices

---

# ✅ 7. Final Scope Summary

| Feature           | Included |
| ----------------- | -------- |
| Arithmetic        | ✔        |
| Scientific        | ✔        |
| Graph Plotting    | ✔        |
| Graph Interaction | ✔        |
| Equation Solving  | ✔        |
| Local History     | ✔        |
| Offline Mode      | ✔        |
| Backend           | ✖        |
| Database          | ✖        |
| Authentication    | ✖        |

---
