# C Quiz Arena

A simple, terminal-based multiple-choice quiz game written in C that helps you practice C programming fundamentals using a randomized set of questions each run.

## Overview

C Quiz Arena is a command-line MCQ quiz application that presents 10 randomly selected questions from a bank of 50 C programming questions. It uses a struct-based question model and a shuffle algorithm to keep each playthrough unique while tracking the user’s score and percentage. This design follows common patterns used in beginner-friendly C quiz examples that rely on arrays of structs and basic I/O.

## Features

C Quiz Arena focuses on clarity and learning, making it suitable for beginners exploring C language basics. It emphasizes clean terminal interaction and simple data structures.

- **Extensive Question Bank**: Includes 50 hardcoded questions covering C fundamentals such as data types, control flow, functions, pointers, and basic syntax.
- **Randomization**: Uses the Fisher–Yates (Knuth) shuffle algorithm to randomize the question array so each run presents a different set of 10 questions.
- **Score Tracking**: Counts the number of correct answers and computes the final percentage based on 10 attempted questions.
- **Simple Terminal I/O**: Uses standard input/output functions, accepts answers as single characters (`A`–`D`), and normalizes lowercase input to uppercase automatically.
- **Deterministic Structure**: All questions and logic are stored in a single C source file for easy reading and modification.

## Prerequisites

To build and run this program, you need a C compiler installed on your system.
- **GCC** (GNU Compiler Collection) is recommended.
- Works on Linux, macOS, and Windows (via MinGW or similar).

## How to Compile and Run

Follow these steps to compile and execute the quiz on your terminal or command prompt.

### 1. Save the Code
Save your C source code into a file named `quiz.c`.

### 2. Compile
Open your terminal or command prompt and use the GCC compiler to compile the file:

**Linux/macOS:**
```
gcc quiz.c -o quiz
```

### Execute the compiled program to start the quiz:
```
./quiz
```

**Windows:**
```
gcc quiz.c -o quiz.exe
```

### Execute the compiled program to start the quiz:
```
quiz exe
```
