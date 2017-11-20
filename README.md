iCoq
====

iCoq is a regression proof selection tool for Coq.

Requirements
------------

- [`Coq 8.5.3`](https://github.com/proofengineering/coq) (modified version with `coqdigest` tool and proof-checking dependency extension)
- [`coq-ast`](https://github.com/proofengineering/coq-ast)
- [`coq-depends`](https://github.com/proofengineering/coq-depends)

Installation
------------

We recommend installing iCoq via [OPAM](http://opam.ocaml.org/doc/Install.html), which will automatically build and install all its dependencies:
```
opam repo add proofengineering-dev http://opam-dev.proofengineering.org
opam install icoq
```

Usage
-----

iCoq must be pointed at the directory where the `_CoqProject` file for your project resides.

We recommend adding an iCoq task in your `Makefile`, as follows:
```
icoq: _CoqProject
        icoq $(shell pwd) -timer
```
Then, you can simply run `make icoq`.

To run iCoq from the command line, go the directory with the `_CoqProject` file and run:
```
icoq $PWD
```
