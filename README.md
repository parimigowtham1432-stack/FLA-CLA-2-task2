# Formal Language and Automata – CLA-2 Assignment 2

## Finite Automata for Real-Time Input Validation

### Student Details

| Field | Details |
|---|---|
| Student Name | PARIMI GOWTHAM |
| Registration Number | RA2411026050033 |
| University | SRM Institute of Science and Technology |
| Campus | Tiruchirappalli |
| Department | Artificial Intelligence and Machine Learning |
| Programme | B.Tech |
| Year | III Year |
| Course Code | 21CSC301T |
| Course Name | Formal Language and Automata |
| Academic Year | 2026–2027 |

---

## 1. Project Overview

This project demonstrates the practical application of **Deterministic Finite Automata (DFA)** in real-time input validation systems.

The objective is to design and implement three different finite automata that validate specific input formats.

The project uses Python to simulate DFA state transitions, validate input strings, generate state diagrams, and display test results.

### Applications Developed

1. Indian Mobile Number Validator
2. University Course Code Validator
3. Hexadecimal Colour Code Validator

---

## 2. Project Objectives

- Understand the practical applications of finite automata.
- Design DFA models for real-world validation problems.
- Define alphabets, states and transition functions.
- Implement DFA simulations using Python.
- Generate DFA state transition diagrams.
- Create transition tables for each application.
- Test valid and invalid input strings.
- Understand the difference between syntax and semantic validation.

---

## 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python 3 | Main programming language |
| Google Colab | Cloud-based development environment |
| Pandas | Transition tables and test reports |
| Matplotlib | DFA state diagram visualisation |
| Dataclasses | DFA model implementation |

---

## 4. Applications and Working Principles

### Application 1: Indian Mobile Number Validator

**Objective:** Validate an Indian mobile-number format.

**Validation Rules:**
- The number must contain exactly 10 digits.
- The first digit must be between 6 and 9.
- Only numeric digits are accepted.

**Example:**

Accepted:
- 9876543210
- 9123456789
- 8765432109

Rejected:
- 5123456789
- 987654321
- 98765432109

**DFA Concept:** The automaton uses states to count the number of digits received and a trap state to reject invalid input.

### Application 2: University Course Code Validator

**Objective:** Validate a predefined university course-code format.

**Validation Rules:**
- First two characters must be uppercase letters.
- Next three characters must be digits.
- Final character must be an uppercase letter.

**Regular Expression:**

`[A-Z]{2}[0-9]{3}[A-Z]`

**Example:**

Accepted:
- CS101T
- AI205L
- MA110T

Rejected:
- cs101T
- C101T
- CS1017

**DFA Concept:** Each state represents the expected character position and type.

### Application 3: Hexadecimal Colour Code Validator

**Objective:** Validate hexadecimal colour codes.

**Validation Rules:**
- The input must begin with `#`.
- Exactly six hexadecimal characters must follow.
- Valid hexadecimal characters include 0–9, A–F and a–f.

**Regular Expression:**

`#[0-9A-Fa-f]{6}`

**Example:**

Accepted:
- #1A2B3C
- #ffffff
- #00FF7A

Rejected:
- 1A2B3C
- #12345
- #12G45Z

**DFA Concept:** The automaton checks the prefix and counts the six hexadecimal characters.

---

## 5. Project Structure

```text
FLA-Assignment-2/
│
├── README.md
│
├── assignment_2.py
│
├── diagrams/
│   ├── mobile_dfa.png
│   ├── course_code_dfa.png
│   └── hex_colour_dfa.png
│
└── reports/
    └── Assignment_2_Report.pdf
```

Note: The diagrams and report folders are optional organisational folders. Save the generated outputs there if you export them separately.

---

## 6. Installation and Requirements

No complicated installation is required when using Google Colab.

The project uses the following Python libraries:

```python
import pandas as pd
import matplotlib.pyplot as plt
from dataclasses import dataclass
from typing import Dict, Tuple, List, Callable
```

If running locally, install the external dependencies:

```bash
pip install pandas matplotlib
```

Python 3.9 or later is recommended.

---

## 7. How to Run the Project

### Method 1: Google Colab

1. Open Google Colab.
2. Create a new notebook.
3. Copy the complete Python implementation into a code cell.
4. Run the cell.
5. Observe the DFA transition tables.
6. View the generated state diagrams.
7. Check the accepted and rejected test cases.
8. Review the final test summary.

Google Colab:

https://colab.research.google.com/

### Method 2: Local Python Environment

1. Install Python 3.
2. Install the required libraries.
3. Save the implementation as `assignment_2.py`.
4. Open a terminal.
5. Execute:

```bash
python assignment_2.py
```

---

## 8. DFA Model

A Deterministic Finite Automaton is represented by the following mathematical tuple:

**M = (Q, Σ, δ, q₀, F)**

Where:

- Q = Set of finite states.
- Σ = Input alphabet.
- δ = Transition function.
- q₀ = Initial state.
- F = Set of accepting states.

Each application contains:
- An initial state.
- Intermediate states.
- An accepting state.
- A trap state.

The automaton processes input characters sequentially and determines whether the input belongs to the specified language.

---

## 9. Testing and Validation

Each application contains:

- Five accepted test cases.
- Five rejected test cases.
- State transition tracing.
- Expected and actual results.
- PASS/FAIL verification.

### Expected Test Summary

| Application | Accepted | Rejected | Total |
|---|---:|---:|---:|
| Mobile Number | 5 | 5 | 10 |
| Course Code | 5 | 5 | 10 |
| Hexadecimal Colour | 5 | 5 | 10 |
| **Total** | **15** | **15** | **30** |

The expected outcome is 30 passed tests when the notebook is executed with the supplied test cases.

---

## 10. Syntax Validation vs Semantic Validation

| Syntax Validation | Semantic Validation |
|---|---|
| Checks input format | Checks actual meaning or validity |
| Uses DFA transitions | May require databases or application logic |
| Checks character positions | Checks external information |

Examples:

- A mobile DFA checks the number format, not whether the number is active.
- A course-code DFA checks the pattern, not whether the course exists.
- A colour-code DFA checks hexadecimal syntax, not whether a design system permits that colour.

---

## 11. Advantages

- Simple and efficient validation.
- Predictable state transitions.
- Easy-to-understand mathematical model.
- Supports automated testing.
- Provides visual representation of input processing.
- Suitable for fixed-format input validation.

## 12. Limitations

- Cannot validate external database information.
- Requires predefined input patterns.
- Does not support arbitrary nested structures.
- Changes in validation rules require changes to the DFA.

---

## 13. Conclusion

This project demonstrates the practical implementation of Deterministic Finite Automata in three input validation applications.

The mobile number validator, university course-code validator and hexadecimal colour-code validator demonstrate how DFA can process strings using finite states and transition functions.

The implementation provides state diagrams, transition tables, test cases and execution traces.

Overall, this assignment provides practical knowledge of finite automata and their importance in computer science, programming languages and input validation systems.

---

## 14. References

1. Hopcroft, J. E., Motwani, R., and Ullman, J. D. *Introduction to Automata Theory, Languages, and Computation*, 3rd Edition, Pearson.
2. Sipser, M. *Introduction to the Theory of Computation*, 3rd Edition, Cengage Learning.
3. Aho, A. V., Lam, M. S., Sethi, R., and Ullman, J. D. *Compilers: Principles, Techniques, and Tools*, 2nd Edition, Pearson.

---

**Developed by:** PARIMI GOWTHAM  
**Registration Number:** RA2411026050033  
**Course:** 21CSC301T – Formal Language and Automata  
**University:** SRM Institute of Science and Technology
