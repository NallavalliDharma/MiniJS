# MiniJS 1.0 Interpreter

A Python implementation of the MiniJS 1.0 programming language using an AST-walking interpreter.

## Project Structure

* `main.py` - Program entry point and execution flow
* `tokens.py` - Token types and token representation
* `lexer.py` - Tokenizes source code
* `ast_nodes.py` - Defines AST nodes
* `parser.py` - Parses tokens into statements and expressions
* `environment.py` - Manages variables and lexical scopes
* `interpreter.py` - Executes MiniJS programs

## Requirements

* Python3

## Run the Interpreter

Create a MiniJS source file, such as `program.mjs`, and execute:

```powershell
python main.py program.mjs
```

## Run Correctness Tests

for the `correctness_test.py` file run:

```powershell
python correctness_test.py -- python main.py
```