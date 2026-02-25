# Virtual Compiler Implementation using Python
📌 Project Overview

This project presents a simplified implementation of a compiler using Python.
It demonstrates how a high-level source program is processed step by step through all the major phases of compilation.

The purpose of this project is to understand the internal workflow of a compiler in a structured and practical manner. Each phase is implemented independently to clearly show its individual responsibility in the compilation process.

🧠 Objective

The main objective of this project is to:

Understand the working of compiler phases

Learn how source code is analyzed and transformed

Implement theoretical compiler concepts using Python

Simulate the transformation from source code to machine-level instructions

🏗️ Compiler Phases Implemented
1️⃣ Lexical Analysis

This phase scans the source code and converts it into tokens.
Tokens include keywords, identifiers, operators, numbers, and separators.

Example:

int a = 5;

Output:

KEYWORD      : int
IDENTIFIER   : a
OPERATOR     : =
NUMBER       : 5
SEPARATOR    : ;
2️⃣ Syntax Analysis

This phase checks whether the sequence of tokens follows the defined grammar rules.
It ensures that the structure of the statement is valid.

Example:

a = b + c

Output:

Syntax is VALID
3️⃣ Semantic Analysis

This phase performs logical validation such as:

Checking if variables are declared before use

Detecting redeclaration errors

Ensuring correct variable usage

Example:

int a
a = 10

Output:

Semantic Analysis Successful
4️⃣ Intermediate Code Generation (ICG)

This phase generates an intermediate representation of the code, typically in the form of Three Address Code (TAC).

Example:

a = b + c * d

Output:

t1 = c * d
t2 = b + t1
a = t2
5️⃣ Code Optimization

This phase improves the intermediate code by removing redundant operations and simplifying expressions wherever possible.

Example:

t1 = c * d
t2 = b + t1
a = t2

Optimized Output:

a = b + c * d
6️⃣ Code Generation

This final phase converts the optimized intermediate code into simple machine-like instructions.

Supported Instructions:

MOV

ADD

MUL

SUB

Example:

t1 = c * d

Output:

MOV R1, c
MUL R1, d
MOV t1, R1
📂 Project Structure
Compiler-Design/
│
├── Phase1_Lexical/
│   ├── lexer.py
│   ├── input.txt
│   ├── output.txt
│   └── README.md
│
├── Phase2_Syntax/
│   ├── syntax.py
│   ├── input.txt
│   ├── output.txt
│   └── README.md
│
├── Phase3_Semantic/
│   ├── semantic.py
│   ├── input.txt
│   ├── output.txt
│   └── README.md
│
├── Phase4_ICG/
│   ├── icg.py
│   ├── input.txt
│   ├── output.txt
│   └── README.md
│
├── Phase5_Optimizer/
│   ├── optimizer.py
│   ├── input.txt
│   ├── output.txt
│   └── README.md
│
├── Phase6_CodeGen/
│   ├── codegen.py
│   ├── input.txt
│   ├── output.txt
│   └── README.md
│
└── README.md

Each phase works independently and reads from its respective input file to generate output.

⚙️ Technologies Used

Python 3

Regular Expressions

File Handling

Basic Parsing Techniques

Core Compiler Design Concepts

▶️ How to Run

Navigate to the required phase folder and execute:

python filename.py

Each module processes its input file and generates the corresponding output file.

🎯 Learning Outcomes

Through this project, the following concepts are understood:

Tokenization process

Grammar validation

Semantic checking

Three-address code generation

Code optimization techniques

Basic machine instruction generation

This project provides a clear understanding of how a compiler transforms source code into executable instructions in a structured and systematic way.
