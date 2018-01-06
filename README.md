# Unit tests for [Smudge](https://github.com/rimuz/smudge)
To use this unit tests you need:
- A **POSIX-Compliant** environment (Cygwin or any Unix-like OS)
- [**Smudge**](https://github.com/rimuz/smudge) (the latest version possible)

## How to use
First, clone the repository in your working directory:

```
git clone https://github.com/rimuz/smudge-test
```

Now the directory `smudge-test` will contain a script named `test`.
Running command `./test` will print something like that:

```
Testing unit 0: RESULT
Testing unit 1: RESULT
...
Testing unit N: RESULT

TESTED: X
PASSED: X
FAILED: X
```

Each unit test is contained in a folder named `unit_N` (N is the number of the unit starting from 0) and consist of:
- A script named `main.sm` that will return **zero** in case of **success**, **non-zero** value otherwise.
- Two files named `.out` and `.err` filled with the `stdout` and `stderr` outputs of the unit.
- A file named `.in` that contains the `stdin` to give to the unit.
- Optionally another file named `.expOut` that contains the expected `stdout` output of the unit (if `.expOut` is absent, any output is valid).

A unit test **fails** if it returned a non-zero value **or**
if the output unmet the expected output (given via `.expOut`).

### See also
[The Smudge Programming Language](https://github.com/rimuz/smudge)
