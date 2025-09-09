# COBOL Fibonacci Sequence

This project demonstrates how to generate Fibonacci numbers using **COBOL**. It includes a **loop-based implementation** of the Fibonacci sequence and is intended for educational purposes to learn COBOL syntax, loops, and basic arithmetic operations.

---

## Features

- Generate Fibonacci numbers for a user-specified number of terms.
- Loop-based implementation for efficiency.
- Compatible with modern COBOL compilers and online IDEs.
- Can be extended to recursive versions using modern COBOL recursion.

---

## Example Output

```
Enter number of Fibonacci terms: 10
Fibonacci sequence using loop:
0
1
1
2
3
5
8
13
21
34
```

---

## Getting Started

### Prerequisites

- **COBOL compiler** (any modern compiler like GnuCOBOL).  
- **Online IDE options**:
  - [JDoodle – COBOL](https://www.jdoodle.com/execute-cobol-online/)
  - [TutorialsPoint – COBOL Compiler](https://www.tutorialspoint.com/compile_cobol_online.php)
  - [Replit – COBOL](https://replit.com/languages/cobol)

### Running the Program

1. Save the code in a file with `.cob` or `.cbl` extension, e.g., `fibonacci.cob`.
2. Run the program using a COBOL compiler or an online IDE.
3. Input the number of Fibonacci terms when prompted.

---

## COBOL Code Snippet (Loop-Based Fibonacci)

```cobol
       IDENTIFICATION DIVISION.
       PROGRAM-ID. FIBONACCI.

       DATA DIVISION.
       WORKING-STORAGE SECTION.
       77 N            PIC 9(3).
       77 I            PIC 9(3).
       77 F1           PIC 9(9) VALUE 0.
       77 F2           PIC 9(9) VALUE 1.
       77 TEMP         PIC 9(9).

       PROCEDURE DIVISION.
       DISPLAY "Enter number of Fibonacci terms: ".
       ACCEPT N.

       DISPLAY "Fibonacci sequence using loop: ".
       PERFORM VARYING I FROM 1 BY 1 UNTIL I > N
           DISPLAY F1
           ADD F1 TO F2 GIVING TEMP
           MOVE F2 TO F1
           MOVE TEMP TO F2
       END-PERFORM.

       STOP RUN.
```

---

## Notes

- **Variables**: `F1` and `F2` store the previous two Fibonacci numbers. `TEMP` is used for updating values.  
- **Loop**: `PERFORM VARYING` is used to generate the sequence efficiently.  
- **Recursion**: COBOL supports recursion in modern compilers, but loops are more idiomatic for simple sequences.

---

## File Extension

- Use `.cob` or `.cbl` for COBOL source files.  
- `.cpy` is reserved for copybooks (reusable code snippets).

---

## License

This project is for **educational purposes**. You may freely use, modify, and share the code.

---

## References

- [GnuCOBOL Documentation](https://open-cobol.sourceforge.io/)
- [JDoodle – COBOL Online Compiler](https://www.jdoodle.com/execute-cobol-online/)
- [TutorialsPoint – COBOL Compiler](https://www.tutorialspoint.com/compile_cobol_online.php)

## Screenshot

![screenshot](Screenshot.jpg)
