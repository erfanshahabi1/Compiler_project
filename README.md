# C-Minus Compiler — Lexical & Syntax Analysis

A university compiler-construction project in **Python**, developed in **Google Colab**, for a modified **C-Minus** language. The repository focuses on the first two compilation stages and uses **ANTLR4** for an additional grammar-based implementation and comparison.

## Implemented features

**Phase 1 — Lexical analysis**
- A Python scanner that identifies keywords, identifiers, integers, and language symbols.
- Handling of whitespace, line/block comments, and selected lexical errors.
- Generation of `tokens.txt`, `lexical_errors.txt`, and `symbol_table.txt`.
- An ANTLR4 lexer and a token-output comparison utility.

**Phase 2 — Syntax analysis**
- An ANTLR4 parser grammar covering declarations, functions, arrays, expressions, and control-flow statements in modified C-Minus.
- Parse-tree formatting and export to `parse_tree.txt`.
- Syntax-error collection and export to `syntax_errors.txt`.

## Repository contents

- `Compiler_Phase1_2_3.ipynb` — main notebook containing the scanner, ANTLR lexer/parser grammars, parse-tree formatting, and output-generation code.
- **Test case file(s)** — sample compiler inputs provided in the repository for checking behavior. Use these as input when running the notebook.
- Generated output files (when present): `tokens.txt`, `lexical_errors.txt`, `symbol_table.txt`, `1p_ANTLR.txt`, `parse_tree.txt`, and `syntax_errors.txt`.

> **Scope:** Despite the notebook filename, the uploaded implementation demonstrates **Phases 1 and 2 only**. Semantic analysis and intermediate-code generation (Phase 3) are not implemented in the reviewed notebook.

## Running the project

1. Open `Compiler_Phase1_2_3.ipynb` in **Google Colab**.
2. Run the setup cells to install the ANTLR4 Python runtime and generate the lexer/parser from their `.g4` grammars.
3. Upload a C-Minus source file (for example, one of the repository's test cases) when prompted.
4. Run the remaining cells to generate lexical-analysis outputs, compare lexer results, and export the parse tree and syntax errors.

**Requirements:** Python 3, Java (for ANTLR code generation), ANTLR4, and Google Colab upload/download utilities. The notebook contains setup cells for different ANTLR versions; use a consistent ANTLR tool/runtime version when reproducing results.

## Notes and limitations

- The scanner and ANTLR lexer do not have identical identifier rules, and some malformed-token/comment edge cases may not be handled consistently.
- The parser uses broad `KEYWORD` and `SYMBOL` token categories in several rules, so its grammar does not fully validate every specific keyword or punctuation mark.
- The parser is **ANTLR-generated**, not a separately implemented predictive-parser engine; therefore, it should not be described as a complete hand-written LL(1) parser.
- The notebook is an educational prototype rather than a production-ready compiler.

## Academic context

Course project on compiler design, inspired by standard compiler-construction concepts such as tokenization, context-free grammars, parsing, and error reporting.
