# 🧠 Virtual Compiler Implementation using Python

📌 Project Overview
This project demonstrates the complete working of a compiler through its six major phases using Python.
It simulates how a real compiler processes source code step-by-step and converts it into target machine instructions.


🏗️ Compiler Phases Implemented
1. Lexical Analysis
2. Syntax Analysis
3. Semantic Analysis
4. Intermediate Code Generation
5. Code Optimization
6. Code Generation


📂 Project Structure
```
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
```

🔵 Phase 1 – Lexical Analysis
Converts source code into tokens such as keywords, identifiers, operators, numbers, and separators.

Sample Input:
int a = 5;

Sample Output:
KEYWORD     : int
IDENTIFIER  : a
OPERATOR    : =
NUMBER      : 5
SEPARATOR   : ;


🔵 Phase 2 – Syntax Analysis
Checks whether the given expression follows correct grammar rules.

Grammar Used:
identifier = identifier operator identifier

Sample Input:
a = b + c

Sample Output:
Syntax is VALID


🔵 Phase 3 – Semantic Analysis
Performs:
• Variable declaration checking
• Redeclaration detection
• Usage before declaration detection

Sample Input:
int a
a = 10

Sample Output:
Semantic Analysis Successful


🔵 Phase 4 – Intermediate Code Generation (ICG)
Generates Three Address Code (TAC).

Sample Input:
a = b + c * d

Sample Output:
t1 = c * d
t2 = b + t1
a = t2


🔵 Phase 5 – Code Optimization
Removes redundant temporary variables and simplifies expressions.

Sample Input:
t1 = c * d
t2 = b + t1
a = t2

Sample Output:
a = t2


🔵 Phase 6 – Code Generation
Generates simple target machine instructions.

Instructions Used:
• MOV
• ADD
• MUL

Sample Input:
t1 = c * d
t2 = b + t1

Sample Output:
MOV R1, c
MUL R1, d
MOV t1, R1
MOV R2, b
ADD R2, t1
MOV t2, R2


⚙️ Technologies Used
• Python 3
• Regular Expressions
• File Handling
• Compiler Design Concepts


▶️ How to Run
Navigate into any phase folder and run:

python filename.py

Each phase reads from its respective input file and generates output accordingly.


🎯 Learning Outcomes
Through this project, we understand:
• Tokenization
• Grammar validation
• Semantic checking
• Three-address code generation
• Code optimization
• Target code generation

This project demonstrates the internal working of a compiler in a simplified and structured manner.
"""

# Save as TXT using pypandoc as required
import pypandoc

output_path = "/mnt/data/Virtual_Compiler_README.txt"
pypandoc.convert_text(readme_content, 'plain', format='md', outputfile=output_path, extra_args=['--standalone'])

output_path
