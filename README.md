# RoadC

A programming language built on English grammar. Python-style indentation, 7 sentence patterns, full toolchain from lexer to C99 compiler.

## What It Does

RoadC maps the 7 English sentence structures (Greenbaum & Nelson) to 7 function patterns. Code reads like structured English. The toolchain compiles to real C99.

## Toolchain

| Component | Lines of Code | What It Does |
|-----------|--------------|--------------|
| **Lexer** | 618 | Tokenization with indentation tracking |
| **Parser** | 826 | AST generation from token stream |
| **Interpreter** | 320 | Direct execution of the AST |
| **Compiler** | 618 | C99 code generation |

Total: 2,382 lines of hand-written language toolchain.

## The 7 Patterns

Based on English sentence structures (SV, SVA, SVC, SVO, SVOO, SVOA, SVOC):

```
show "hello"                    # SV  — Subject-Verb
move x to 10                    # SVA — Subject-Verb-Adverbial
let result be 42                # SVC — Subject-Verb-Complement
compute sum from a and b        # SVO — Subject-Verb-Object
give player item at slot        # SVOO — Subject-Verb-Object-Object
put value into array at index   # SVOA — Subject-Verb-Object-Adverbial
make x equal to y plus z        # SVOC — Subject-Verb-Object-Complement
```

## Run

```bash
# Interpret directly
python roadc.py run program.rc

# Compile to C99
python roadc.py compile program.rc -o program.c
gcc program.c -o program
./program
```

## Example

```
let greeting be "hello world"
show greeting
let count be 0
repeat 5 times
    let count be count plus 1
    show count
```

## Stack

- **Toolchain**: Python 3
- **Output**: C99 (compiled mode)
- **Parsing**: Recursive descent with indentation-based scoping
- **Web REPL**: See [roadc-playground](https://github.com/BlackRoad-OS-Inc/roadc-playground)

## Why

Programming languages are built on math notation. RoadC is built on English grammar. Natural language already has formal structure — 7 sentence types that map cleanly to computational patterns. Same expressive power, different foundation.

## License

Proprietary. Copyright (c) 2024-2026 BlackRoad OS, Inc. All rights reserved.

---

*Remember the Road. Pave Tomorrow.*
