Higgs
=====

Higgs JavaScript Virtual Machine

An interpreter and JIT compiler for JavaScript targetting x86-64 platforms.

**Requirements:**

- D compiler (DMD recommended)
- POSIX compliant OS (Linux, Unix, MacOS X)
- x86 64-bit CPU (if using the JIT compiler)
- Python 2.7 (if regenerating object layouts or instruction encodings)

**Quickstart:**

*Get the source:*
 
`git clone https://github.com/maximecb/Higgs.git && cd Higgs/source`

*Compile a binary:*
 
`make all`
generates a binary `higgs` in the source directory.

*Install (optional):*
 
`make install` 
copies the `higgs` binary to `/usr/bin` and the runtime files to `/etc/higgs`.

*Cleanup:*

`make clean`
will remove any binaries in the source directory.

*You may wish to run the unit tests:*
 
`make test`
generates a binary `test-higgs` and tests its proper functioning.

For further info, see the `makefile`.

**Usage:**

`higgs` will start Higgs and give you a REPL (read-eval-print loop).

To execute one or more files, pass them to `higgs`:

`higgs file1.js file2.js`

The `--e` option accepts a string to execute:

`higgs --e "var x = 4; x = x + 5; print(x)"`

The `--repl` option will start a REPL after evaluating a string and/or files:

`higgs --repl file1.js` will evaluate `file1.js` and then start a REPL.

`higgs file1.js` will evaluate `file1.js` and then exit.

The `--jit_disable` option will disable the JIT compiler and rely solely on the interpreter.

The `--jit_dumpasm` option will dump the assembler code generated by the JIT to the console.

**Notes:**
 - You may wish to use `rlwrap` for a better REPL experience.

More
=====

Documentation for Higgs and included libraries can be found in the [Higgs Wiki](https://github.com/maximecb/Higgs/wiki)

You can follow the development of Higgs on [Maxime's blog](http://pointersgonewild.wordpress.com/category/higgs/).

Come chat with us in \#higgsjs on [Freenode](http://freenode.net/)
