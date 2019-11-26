
# Awesome Lisp Languages

A list of lisp-flavored programming languages implemented on top of existing programming languages.

### Why should I care as a lisp programmer?

If you already love s-expressions then lisp-flavored languages will make it nicer when you need to build on existing platforms. In case the target language does not support advanced features like macros and REPL-driven development, these can often be easily added by using the s-expressions layer.

The second point is about helping to spread lisp and its powerful ideas more. The example of Clojure and its relative popularity shows that being hosted on existing mainstream language and leveraging ecosystems of existing libraries is a key to broader adoption. Being constrained by existing platforms can help overcoming the [lisp curse](http://winestockwebdesign.com/Essays/Lisp_Curse.html).

It also lowers the barrier for people to try lisp and learn about the ideas behind it. Traditionally to learn lisp one needs to learn and get used to very unfamiliar syntax while at the same time being exposed to a completely new environment and ecosystem. Taking the environment out of the equation can make the experience of trying out lisp more approachable.

### Why should I care as a programmer in other language?

Learning about Lisp will make you a [better programmer](http://www.catb.org/~esr/faqs/hacker-howto.html). You can pick any language below based on the language you are familiar with to get you started with the [lisp syntax](https://en.m.wikipedia.org/wiki/S-expression) more easily.

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
- [Ferret](https://ferret-lang.org/) [Type-C] aimed towards embedded systems
- [Janet](https://janet-lang.org/) [Type-B] embedable, large standard library, GC
- [Toccata](https://github.com/Toccata-Lang/toccata) [Type-C] Clojure-inspired, gradually typed, no nil values, reference counting, compiles into native binaries
- **Common Lisp**
  - [SBCL](http://www.sbcl.org) [Type-L] high performance native code compiler, native threading support, type inference engine
  - [CLISP](https://clisp.sourceforge.io/) [Type-L] uses bytecode compiler, easily portable
  - [Clasp](https://github.com/clasp-developers/clasp) [Type-L] compiled using LLVM, seamless integration with existing libraries
  - See list of [additional implementations](https://www.cliki.net/Common+Lisp+implementation).
- **Scheme**
  - [Chez Scheme](https://www.scheme.com/) [Type-S] compiles to native binaries, among the fastest available Scheme implementations, R6RS
  - [Chicken Scheme](https://www.call-cc.org/) [Type-S] produces portable and efficient C, supports R5RS and R7RS (work in progress)
  - [Guile](https://www.gnu.org/software/guile/) [Type-S] embedable, useful for extending programs with scripting
  - [Racket](https://racket-lang.org/) [Type-S] large standard library, powerful macro system, includes DrRacket IDE
  - See list of [additional implementations](http://community.schemewiki.org/?scheme-faq-standards#implementations).

### C#

- [Clojure CLR](https://github.com/clojure/clojure-clr) [Type-C] great for game development with arcadia and unity


### Erlang

- [Clojerl](https://github.com/clojerl/clojerl) [Type-C]
- [Lisp Flavored Erlang](http://lfe.io/) [Type-A]

### Go

- [Joker](https://joker-lang.org/) [Type-C] interpreter, linter, great for scripting, Go interop is very limited
- [Zygo](https://github.com/glycerine/zygomys) [Type-B] embedable, call into native Go using reflection, optional infix syntax

### Java

- [ABCL](https://common-lisp.net/project/armedbear/) [Type-L] CL interpreter and compiler, embedable using Java scripting API (JSR-223
- [Clojure](https://clojure.org/) [Type-C]
- [Kawa](https://www.gnu.org/software/kawa/) [Type-S] scheme implementation (R7RS)

### JavaScript

- [ClojureScript](https://clojurescript.org/) [Typec-C]
- [Whalesong](https://www.hashcollision.org/whalesong/) [Type-S]

### Lua

- [Fennel](https://fennel-lang.org/) [Type-A] full Lua compatibility, embedable, compiled code with no runtime dependency
- [Urn](https://urn-lang.com/) [?] focus on minimalism, should work with LuaJIT, influenced by Common Lisp and Clojure

### Objective-C

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

### VHDL

- [Vhdl Lisp](https://github.com/domus123/vhdlisp) - alternative s-expression based notation to describe programmable integrated circuits (FPGAs)

### WASM

- [clj-wasm](https://github.com/roman01la/clj-wasm) [Type-A] Clojure-flavored WASM's text format
- [Arboreta WASM](https://github.com/Arboreta/arboreta-wasm) [?] Common Lisp tooling for WebAssembly

## Misc

- [Bel](http://paulgraham.com/bel.html) - self-hosted lisp dialect, currently no implementation exists, see also markdown formatted [mirror](https://github.com/alephyud/bel)
- [Bigloo](https://www-sop.inria.fr/mimosa/fp/Bigloo/) [Type-S] - compiles into native binaries, interop with C, JVM, .NET
- [Mal](https://github.com/kanaka/mal) is an educational lisp with implementations in dozens of languages. It is a great resource for learning about lisp implementation.
- Additional "write C in Lisp" [projects](https://www.reddit.com/r/lisp/comments/e10spm/a_list_of_various_lispflavored_programming/f8n6qxa/) (most of them not ready for a prime time).
- See also list of languages  [implemented in Lisp](https://github.com/vindarel/list-of-languages-implemented-in-lisp).

## Contribute

Anything incorrect? Is there an interested project that is missing? Open an issue or PR to request adding a project to the list.
