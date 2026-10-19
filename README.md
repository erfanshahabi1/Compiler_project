C-Minus Compiler — Lexical & Syntax Analysis
A university compiler-design project developed in Python and Google Colab for a modified version of the C-Minus programming language. The project explores source-code tokenization, grammar-based parsing, error reporting, and parse-tree generation, with ANTLR4 used alongside a Python lexical scanner.
Features
Phase 1 — Lexical Analysis
- Python-based scanner for recognizing keywords, identifiers, numbers, and symbols.
- Processing of whitespace and comments, with lexical-error reporting.
- Generation of token lists and a symbol table.
- ANTLR4 lexer implementation and token-output comparison.
Phase 2 — Syntax Analysis
- ANTLR4 grammar for C-Minus declarations, functions, arrays, expressions, and control-flow statements.
- Parse-tree generation and text export.
- Syntax-error reporting.
Technologies
Python · ANTLR4 · Google Colab · Java (ANTLR tooling)
Repository Files
File	Description
Compiler_Phase1_2_3.ipynb	Main notebook containing the scanner, ANTLR lexer/parser definitions, and output-generation workflow.
Test case file(s)	Sample C-Minus inputs for testing the compiler components.


The notebook generates output files including tokens.txt, lexical_errors.txt, symbol_table.txt, 1p_ANTLR.txt, parse_tree.txt, and syntax_errors.txt.

Developed as an academic compiler-construction project to apply fundamental concepts from lexical analysis, formal grammars, and syntax analysis to a C-like educational language.
