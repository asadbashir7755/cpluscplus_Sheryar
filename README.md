# C++ Foundations

C++ teaching material I wrote while mentoring a junior developer. Each topic is a
folder of small programs that show one thing at a time, in the order I taught
them.

It is meant to be read in order rather than dipped into.

Portfolio: [committodeploy.dev](https://committodeploy.dev)

## Order

| # | Topic | Folder |
|---|---|---|
| 1 | Hello world, program structure, compiling | `cpp-foundations/Basic Hello world/` |
| 2 | Variables and types | `cpp-foundations/variable/` |
| 3 | A first real program, addition | `cpp-foundations/Addition program/` |
| 4 | Operators: arithmetic, assignment, comparison, logical | `cpp-foundations/Operators _&_ its Types/` |
| 5 | Constants and stream manipulators | `cpp-foundations/Constant and Manipulator/` |
| 6 | Control structures: if and else, switch, loops, break and continue | `cpp-foundations/C++ Control_Structure/` |
| 7 | Arrays, looped with for, while and do while | `cpp-foundations/Arrays/` |
| 8 | Pointers and how they relate to arrays | `cpp-foundations/Pointers-in_C++/` |
| 9 | Functions, including inline functions | `cpp-foundations/Function/` |
| 10 | Combined exercises | `cpp-foundations/Multi-Operations/`, `Multiplication/` |

## How it is structured

Each concept gets several small programs instead of one big one. The arrays folder
walks the same array three different ways, with for, while and do while, so the
loop is the only thing that changes and the difference between them is the only
thing you have to think about. The inline function folder works the same way, four
versions so you can see what actually changes when you add `inline`.

## Building

Every file is standalone:

```bash
g++ -std=c++17 -Wall -Wextra -o demo "cpp-foundations/Arrays/array_for_loop.cpp"
./demo
```

Or build a whole topic at once:

```bash
for f in "cpp-foundations/Operators _&_ its Types"/*.cpp; do
  g++ -std=c++17 -Wall -Wextra -o "/tmp/$(basename "${f%.cpp}")" "$f" && echo "built: $(basename "$f")"
done
```

Compiled binaries are gitignored.

## For anyone learning from this

Read the code first, work out what you think it will print, then run it and see if
you were right. Where you were wrong is the actual lesson.

## Tech stack

C++, g++
