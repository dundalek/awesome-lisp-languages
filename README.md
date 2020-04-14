
# Awesome Lisp Languages

A list of lisp-flavored programming languages implemented on top of existing programming languages.

### Why should I care as a lisp programmer?

If you already love s-expressions then lisp-flavored languages will make it nicer when you need to build on existing platforms. In case the target language does not support advanced features like macros and REPL-driven development, these can often be easily added by using the s-expressions layer.

The second point is about helping to spread lisp and its powerful ideas more. The example of Clojure and its relative popularity shows that being hosted on existing mainstream language and leveraging ecosystems of existing libraries is a key to broader adoption. It also lowers the barrier for people to try lisp and learn about the ideas behind it. Traditionally to learn lisp one needs to learn and get used to very unfamiliar syntax while at the same time being exposed to a completely new environment and ecosystem. Taking the environment out of the equation can make the experience of trying out lisp more approachable.

### Why should I care as a programmer in other language?

Learning about Lisp will make you a [better programmer](http://www.paulgraham.com/avg.html). You can pick any language below based on the language you are familiar with to get you started with the [lisp syntax](https://en.m.wikipedia.org/wiki/S-expression) more easily.

In general when one learns any new programming language it opens new horizons and improves programming insight. Modern programming languages are converging and sometimes are being very similar to each other. The similarities can be missed because they are hidden behind a specific syntax.

If we translate the languages to a common syntax the similarities are more apparent and the different concepts stand out more. That way we can focus on the new innovative concepts and ideas to broaden our horizons.



## Classification

- **Type-A**: Plain mapping from s-expressions - no extra semantics
- **Type-B**: Extra semantics
- **Type-C**: Clojure-like - persistent data structures, namespaces and vars, protocols, etc.
- **Type-L**: Common Lisp
- **Type-S**: Scheme

## Languages

Listed primarily by the language which can be used for interoperability / [FFI](https://en.wikipedia.org/wiki/Foreign_function_interface).

*Language section does not necessarily mean the language of the implementation. For example `Ferret` compiles into `C++` but the compiler is written in `Clojure`. Or `Carp` interops with `C` but it is mostly written in `Haskell`. In case of `SBCL` it contains only small amounts of `C`, but it is implemented almost entirely in `Common Lisp`.*

<!-- TOC depthFrom:3 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [C/C++](#cc)
- [C#](#c)
- [Erlang](#erlang)
- [Fortran](#fortran)
- [Go](#go)
- [Java](#java)
- [JavaScript](#javascript)
- [Lua](#lua)
- [Objective-C](#objective-c)
- [OCaml](#ocaml)
- [Python](#python)
- [Rust](#rust)
- [Shell](#shell)
- [VHDL](#vhdl)
- [WASM](#wasm)

<!-- /TOC -->

### C/C++

- [C-Mera](https://github.com/kiselgra/c-mera) [Type-A] also includes extensions to generate code to run on CUDA, GLSL
- [Carp](https://github.com/carp-lang/Carp) [Type-B] statically typed, no GC (Rust-like borrow checking)
- [Extempore](https://github.com/digego/extempore) [Type-S] designed for live coding and music performances, temporal scheduling based on audio card sample rate
- [FemtoLisp](https://github.com/JeffBezanson/femtolisp) [Type-S] scheme-like lisp, powers the compiler of the Julia language
- [Ferret](https://ferret-lang.org/) [Type-C] aimed towards embedded systems
- [Janet](https://janet-lang.org/) [Type-B] embedable, large standard library, GC
- [Maru](https://www.piumarta.com/software/maru/) [Type-B] minimal self-hosting lisp, multimethods, user-defined types and structures, GC
- [PicoLisp](https://picolisp.com) [Type-B] compiled to bytecode and interpreted, C and Java interop, built-in  database and GUI
- [Owl Lisp](https://gitlab.com/owl-lisp/owl) [Type-S] dialect of the Scheme, code can be interpreted or compiled into C files
- [Toccata](https://github.com/Toccata-Lang/toccata) [Type-C] Clojure-inspired, gradually typed, no nil values, reference counting, compiles into native binaries
- **Common Lisp**
  - [SBCL](http://www.sbcl.org) [Type-L] high performance native code compiler, native threading support, type inference engine
  - [CLISP](https://clisp.sourceforge.io/) [Type-L] uses bytecode compiler, easily portable
  - [Clasp](https://github.com/clasp-developers/clasp) [Type-L] compiled using LLVM, seamless integration with existing libraries
  - [ECL](https://common-lisp.net/project/ecl/) [Type-L] embeddable and portable, can build standalone executables
  - See list of [additional implementations](https://www.cliki.net/Common+Lisp+implementation).
- **Scheme**
  - [Chez Scheme](https://www.scheme.com/) [Type-S] compiles to native binaries, among the fastest available Scheme implementations, R6RS
  - [Chicken Scheme](https://www.call-cc.org/) [Type-S] produces portable and efficient C, supports R5RS and R7RS (work in progress)
  - [Guile](https://www.gnu.org/software/guile/) [Type-S] embedable, useful for extending programs with scripting
  - [Racket](https://racket-lang.org/) [Type-S] large standard library, powerful macro system, includes DrRacket IDE
  - [Microscheme](https://ryansuchocki.github.io/microscheme/) [Type-S] Scheme subset for microcontrollers (like Arduino boards)
  - See list of [additional implementations](http://community.schemewiki.org/?scheme-faq-standards#implementations).

### C#

- [Clojure CLR](https://github.com/clojure/clojure-clr) [Type-C] great for game development with arcadia and unity


### Erlang

- [Clojerl](https://github.com/clojerl/clojerl) [Type-C]
- [Lisp Flavored Erlang](http://lfe.io/) [Type-A]

### Fortran

- [fscheme](https://genepi.qimr.edu.au/Staff/davidD/Scheme/SIOM.html) [Type-S] small scheme interpreter written in Fortran 95

### Go

- [Joker](https://joker-lang.org/) [Type-C] interpreter, linter, great for scripting, Go interop is very limited
- [Zygo](https://github.com/glycerine/zygomys) [Type-B] embedable, call into native Go using reflection, optional infix syntax

### Java

- [ABCL](https://common-lisp.net/project/armedbear/) [Type-L] CL interpreter and compiler, embedable using Java scripting API (JSR-223
- [Clojure](https://clojure.org/) [Type-C]
- [Kawa](https://www.gnu.org/software/kawa/) [Type-S] scheme implementation (R7RS)
- [PicoLisp](https://picolisp.com) [Type-B] compiled to bytecode and interpreted, C and Java interop, built-in  database and GUI

### JavaScript

- [BiwaScheme](https://www.biwascheme.org/) [Type-S] compact Scheme written in JavaScript, integrates well with web browsers and Node
- [ClojureScript](https://clojurescript.org/) [Type-C]
- [LIPS](https://jcubic.github.io/lips/) [Type-S] similar to BiwaScheme, has better notation to call JS functions
- [Lumen](https://github.com/sctb/lumen) [Type-A] self-hosted Lisp for Lua and JavaScript, uses arrays as first-class datastructures
- [Parenscript](https://common-lisp.net/project/parenscript/) [Type-L] Common Lisp to JavaScript translator, native JS types, native calling convention
- [Whalesong](https://www.hashcollision.org/whalesong/) [Type-S] Racket to JavaScript compiler
- [Wisp](https://github.com/Gozala/wisp) [Type-C] Clojure-like, has protocols, no persistent data structures

### Lua

- [Fennel](https://fennel-lang.org/) [Type-A] full Lua compatibility, embedable, compiled code with no runtime dependency
- [Lumen](https://github.com/sctb/lumen) [Type-A] self-hosted Lisp for Lua and JavaScript, uses arrays as first-class datastructures
- [Urn](https://urn-lang.com/) [?] focus on minimalism, should work with LuaJIT, influenced by Common Lisp and Clojure

### Objective-C

- [DreamLisp](https://github.com/jsloop42/dreamlisp) [Type-B] Clojure-inspired, originally based on MAL, added modules, lazy collections
- [nu](https://github.com/programming-nu/nu) [?] interpreted

### OCaml

- [Reason-Lisp](https://github.com/jaredly/myntax) [Type-A] very incomplete

### Python

- [Hy](https://github.com/hylang/hy) [Type-A] compiles to Python AST, use Python ML libraries, runs on PyPy
- [Pixie](https://github.com/pixie-lang/pixie) [Type-B] Clojure inspired, written in RPython, custom GC and JIT

### Rust

- [Ketos](https://github.com/murarth/ketos) [Type-B] scripting and extension language for Rust programs, compiled to bytecode
- [Rustly](https://github.com/timothypratley/rustly) [Type-C] transpiler, only small subset of Clojure supported

### Shell

- [Gherkin](https://github.com/alandipert/gherkin) [Type-B] (dormant) implemented in Bash, shell interop
- [Fleck](https://github.com/chr15m/flk/) [Type-A] Clojure-like, based on [Mal](https://github.com/kanaka/mal/), packaged as single-file Bash script

### VHDL

- [Vhdl Lisp](https://github.com/domus123/vhdlisp) - alternative s-expression based notation to describe programmable integrated circuits (FPGAs)

### WASM

- [clj-wasm](https://github.com/roman01la/clj-wasm) [Type-A] Clojure-flavored WASM's text format
- [Arboreta WASM](https://github.com/Arboreta/arboreta-wasm) [?] Common Lisp tooling for WebAssembly
- [Schism](https://github.com/google/schism) [Type-S] self-hosting compiler from a subset of R6RS Scheme to WebAssembly

## Misc

- [Bel](http://paulgraham.com/bel.html) - self-hosted lisp dialect, currently no implementation exists, see also markdown formatted [mirror](https://github.com/alephyud/bel)
  - [Chime](https://github.com/jeremyschlatter/chime/) - hobby implementation of Bel
- [Loko Scheme](https://gitlab.com/weinholt/loko) [Type-S] runs on bare hardware
- [uLisp](http://www.ulisp.com/) - Lisp for microcontrollers, fits into 2 Kbytes of RAM
- [Bigloo](https://www-sop.inria.fr/mimosa/fp/Bigloo/) [Type-S] compiles into native binaries, interop with C, JVM, .NET
- [STELLA](https://www.isi.edu/isd/LOOM/Stella/index.html) - strongly typed, object-oriented, compiles down to Common Lisp, C++, or Java
- [Shen](https://shen-language.github.io/) [Type-B] implementations in many programming languages, builtin pattern-matching and logic programming, optional static typing and lazy evaluation
- [Mal](https://github.com/kanaka/mal) is an educational lisp with implementations in dozens of languages. It is a great resource for learning about lisp implementation.
- [Zick Standard Lisp](https://github.com/zick/ZickStandardLisp) minimal lisp with 42 implementations
- A list of more [Clojure-like languages](https://github.com/chr15m/awesome-clojure-likes).
- Additional "write C in Lisp" [projects](https://www.reddit.com/r/lisp/comments/e10spm/a_list_of_various_lispflavored_programming/f8n6qxa/) (most of them not ready for a prime time).
- [Build your own lisp](http://www.buildyourownlisp.com/) - a book describing building a Lisp dialect
- See also list of languages  [implemented in Lisp](https://github.com/vindarel/list-of-languages-implemented-in-lisp).

## Contribute

Anything incorrect? Is there an interested project that is missing? Open an issue or PR to request adding a project to the list.
