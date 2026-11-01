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

## To Evaluate The Execution Time

To evaluate the performance of the AST interpreter, I conducted a benchmark using a MiniJS program that calculates the sum of numbers from `0` to `999,999` using a `while` loop.

### Benchmark Program

```javascript
let i = 0;
let sum = 0;

while (i < 1000000) {
    sum = sum + i;
    i = i + 1;
}

print(sum);
```

### Benchmark Results

The benchmark was executed **8 times** to measure execution time and calculate the average performance.

|     Run     | Execution Time (seconds) |
| :---------: | -----------------------: |
|      1      |                 3.506639 |
|      2      |                 3.583509 |
|      3      |                 3.870669 |
|      4      |                 3.634937 |
|      5      |                 3.766318 |
|      6      |                 3.855072 |
|      7      |                 3.368240 |
|      8      |                 3.552852 |
| **Average** |             **3.642230** |

### Expected Output

```text
499999500000
```

### Benchmark Summary

| Metric                 | Result                  |
| ---------------------- | ----------------------- |
| Interpreter            | AST-walking interpreter |
| Loop Iterations        | 1,000,000               |
| Benchmark Runs         | 8                       |
| Average Execution Time | **3.642230 seconds**    |
| Output Validation      | Passed (8/8 runs)       |

### Conclusion

The AST-walking interpreter successfully executed one million loop iterations in all eight benchmark runs.

The average execution time was approximately **3.64 seconds**, and all executions produced the expected output (`499999500000`).
