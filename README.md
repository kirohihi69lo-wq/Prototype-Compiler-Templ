Tiny Compiler (Python, single-file)

This project is a small educational compiler and virtual machine, written entirely in Python.
It takes in a tiny C-like language, and walks through all the classic phases:
	•	Lexing → split text into tokens
	•	Parsing → build a small abstract syntax tree (AST)
	•	Code generation → translate into bytecode
	•	Execution → run the bytecode on a simple stack-based VM

All of it lives in one file, so you can read it end-to-end and see the flow without jumping across modules.

⸻

Features
	•	Variables and assignment (let x = 10;)
	•	Arithmetic and boolean expressions (+ - * / %, < > == !=, && ||)
	•	if / else conditional blocks
	•	while loops
	•	Function definitions and calls (supports recursion)
	•	return statements
	•	Simple output with print(expr);
	•	Both integers and booleans as basic types

Example Program

fn add(a, b) { return a + b; }

fn fact(n) {
  let r = 1;
  while (n > 1) {
    r = r * n;
    n = n - 1;
  }
  return r;
}

let x = add(2, 3);
print(x);       // 5
print(fact(6)); // 720

How to Run

You only need Python 3.

python tiny_compiler.py < source.txt

If you run it without any input, it will execute a small demo program built into the file.

Why This Exists

This isn’t meant to replace production compilers.
It’s a single-file study piece: compact enough to digest in one sitting,
but complete enough to show how lexing, parsing, bytecode, and a VM all tie together.

It’s written with clarity in mind, so you can take it as a starting point,
modify it, extend the language, or just learn from reading through.

⸻

License

MIT / HIROKI
