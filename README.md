
# Awesome Lisp Languages

A list of lisp-flavored programming languages implemented on top of existing programming languages.

### Why should I care as a lisp programmer?

If you already love s-expressions then lisp-flavored languages will make it nicer when you need to build on existing platforms. In case the target language does not support advanced features like macros and REPL-driven development, these can often be easily added by using the s-expressions layer.

The second point is about helping to spread lisp and its powerful ideas more. The example of Clojure and its relative popularity shows that being hosted on existing mainstream language and leveraging ecosystems of existing libraries is a key to broader adoption. It also lowers the barrier for people to try lisp and learn about the ideas behind it. Traditionally to learn lisp one needs to learn and get used to very unfamiliar syntax while at the same time being exposed to a completely new environment and ecosystem. Taking the environment out of the equation can make the experience of trying out lisp more approachable.

### Why should I care as a programmer in other language?

Learning about Lisp will make you a [better programmer](http://www.paulgraham.com/avg.html). You can pick any language below based on the language you are familiar with to get you started with the [lisp syntax](https://en.m.wikipedia.org/wiki/S-expression) more easily. It is also worth to read a post to get [intuition for lisp syntax](https://stopa.io/post/265).

In general when one learns any new programming language it opens new horizons and improves programming insight. Modern programming languages are converging and sometimes are being very similar to each other. The similarities can be missed because they are hidden behind a specific syntax.

If we translate the languages to a common syntax the similarities are more apparent and the different concepts stand out more. That way we can focus on the new innovative concepts and ideas to broaden our horizons.



## Classification

- **Type-A**: Simple syntax mapping  
*These languages usually just provide s-expressions (parentheses) syntax and are translated to the target language without extra features/semantics. Also sometimes being called transpilers.*

- **Type-B**: Syntax and additional semantics  
*In addition to translating the syntax some additional features/semantics that are not present in the target language are added. Usually if a language does not fit in other category, it can be considered being a Type-B.*

- **Type-C**: [Clojure](https://clojure.org/)-like  
*Distintive syntax that besides parentheses also uses brackets and curly braces. Distinctive features are persistent data structures, namespaces and vars, protocols.*

- **Type-L**: [Common Lisp](https://en.wikipedia.org/wiki/Common_Lisp)  
*Implementing ANSI Common Lisp standard or being inspired by it.*

- **Type-S**: [Scheme](https://en.wikipedia.org/wiki/Scheme_%28programming_language%29)  
*Implementing some of RxRS standards or being inspired by Scheme.*

## Languages

Listed primarily by the language which can be used for interoperability / [FFI](https://en.wikipedia.org/wiki/Foreign_function_interface).

*Language section does not necessarily mean the language of the implementation. For example `Ferret` compiles into `C++` but the compiler is written in `Clojure`. Or `Carp` interops with `C` but it is mostly written in `Haskell`. In case of `SBCL` it contains only small amounts of `C`, but it is implemented almost entirely in `Common Lisp`.*

<!-- TOC depthFrom:3 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Multi Lang](#multi-lang)
- [Common Lisp](#common-lisp)
- [Scheme](#scheme)
- [C/C++](#cc)
- [C#](#c)
- [Erlang](#erlang)
- [Fortran](#fortran)
- [Go](#go)
- [Java](#java)
- [JavaScript](#javascript)
- [Julia](#julia)
- [Lua](#lua)
- [Objective-C](#objective-c)
- [OCaml](#ocaml)
- [Python](#python)
- [R](#r)
- [Rust](#rust)
- [Shell](#shell)
- [VHDL](#vhdl)
- [WASM](#wasm)

<!-- /TOC -->

### Multi Lang

- [![last-commit](https://img.shields.io/github/last-commit/manuel-serrano/bigloo.svg)](https://github.com/manuel-serrano/bigloo) [Bigloo](https://www-sop.inria.fr/mimosa/fp/Bigloo/) [Type-S] compiles into native binaries, interop with C, JVM, .NET
- [![last-commit](https://img.shields.io/github/last-commit/LuxLang/lux.svg)](https://github.com/LuxLang/lux) [Lux](https://github.com/LuxLang/lux) [Type-B] functional, statically-typed Lisp that will run on several platforms
- [![last-commit](https://img.shields.io/github/last-commit/kanaka/mal.svg)](https://github.com/kanaka/mal) [Mal](https://github.com/kanaka/mal) is an educational lisp with implementations in dozens of languages. It is a great resource for learning about lisp implementation.
- [STELLA](https://www.isi.edu/isd/LOOM/Stella/index.html) - strongly typed, object-oriented, compiles down to Common Lisp, C++, or Java
- [![last-commit](https://img.shields.io/github/last-commit/Shen-Language/shen-cl.svg)](https://github.com/Shen-Language/shen-cl) [Shen](https://shen-language.github.io/) [Type-B] implementations in many programming languages, builtin pattern-matching and logic programming, optional static typing and lazy evaluation
- [![last-commit](https://img.shields.io/github/last-commit/LingDong-/wax.svg)](https://github.com/LingDong-/wax) [Wax](https://github.com/LingDong-/wax) [Type-A] tiny programming language, strongly statically typed, manual memory management, transpiles to C, C++, Java, TypeScript, Python, C#, Swift, Lua and WebAssembly
- [![last-commit](https://img.shields.io/github/last-commit/zick/ZickStandardLisp.svg)](https://github.com/zick/ZickStandardLisp) [Zick Standard Lisp](https://github.com/zick/ZickStandardLisp) minimal lisp with 42 implementations

### Common Lisp
- [![last-commit](https://img.shields.io/github/last-commit/sbcl/sbcl.svg)](https://github.com/sbcl/sbcl) [SBCL](http://www.sbcl.org) [Type-L] high performance native code compiler, native threading support, type inference engine
- [![last-commit](https://img.shields.io/github/last-commit/roswell/clisp.svg)](https://github.com/roswell/clisp) [CLISP](https://clisp.sourceforge.io/) [Type-L] uses bytecode compiler, easily portable
- [Clozure CL](https://ccl.clozure.com/) [Type-L] fast compilation speed, native threads, precise generational compacting garbage collector, convenient foreign-function interface
- [![last-commit](https://img.shields.io/github/last-commit/clasp-developers/clasp.svg)](https://github.com/clasp-developers/clasp) [Clasp](https://github.com/clasp-developers/clasp) [Type-L] compiled using LLVM, seamless integration with existing libraries
- [![last-commit](https://badgen.net/gitlab/last-commit/embeddable-common-lisp/ecl?.svg)](https://gitlab.common-lisp.net/ecl/ecl) [ECL](https://common-lisp.net/project/ecl/) [Type-L] embeddable and portable, can build standalone executables
- See list of [additional implementations](https://www.cliki.net/Common+Lisp+implementation).

### Scheme
- [![last-commit](https://img.shields.io/github/last-commit/cisco/ChezScheme.svg)](https://github.com/cisco/ChezScheme) [Chez Scheme](https://www.scheme.com/) [Type-S] compiles to native binaries, among the fastest available Scheme implementations, R6RS
- [Chicken Scheme](https://www.call-cc.org/) [Type-S] produces portable and efficient C, supports R5RS and R7RS (work in progress)
- [![last-commit](https://badgen.net/gitlab/last-commit/guile-git/guile-git?.svg)](https://gitlab.com/guile-git/guile-git) [Guile](https://www.gnu.org/software/guile/) [Type-S] embedable, useful for extending programs with scripting
- [![last-commit](https://img.shields.io/github/last-commit/racket/racket.svg)](https://github.com/racket/racket) [Racket](https://racket-lang.org/) [Type-S] large standard library, powerful macro system, includes DrRacket IDE
- [![last-commit](https://img.shields.io/github/last-commit/justinethier/cyclone.svg)](https://github.com/justinethier/cyclone) [Cyclone](https://justinethier.github.io/cyclone/) [Type-S] Scheme-to-C compiler, R7RS, native threading support, generates fast native binaries
- [![last-commit](https://img.shields.io/github/last-commit/ryansuchocki/microscheme.svg)](https://github.com/ryansuchocki/microscheme) [Microscheme](https://ryansuchocki.github.io/microscheme/) [Type-S] Scheme subset for microcontrollers (like Arduino boards)
- [![last-commit](https://badgen.net/gitlab/last-commit/weinholt/loko?.svg)](https://gitlab.com/weinholt/loko) [Loko Scheme](https://gitlab.com/weinholt/loko) [Type-S] runs on bare hardware
- See list of [additional implementations](http://community.schemewiki.org/?scheme-faq-standards#implementations) and [benchmarks](https://ecraven.github.io/r7rs-benchmarks/).

### C/C++

- [![last-commit](https://img.shields.io/github/last-commit/kiselgra/c-mera.svg)](https://github.com/kiselgra/c-mera) [C-Mera](https://github.com/kiselgra/c-mera) [Type-A] also includes extensions to generate code to run on CUDA, GLSL
- [![last-commit](https://img.shields.io/github/last-commit/makuto/cakelisp.svg)](https://github.com/makuto/cakelisp) [Cakelisp](https://github.com/makuto/cakelisp) [Type-A] performance-oriented, good for game development, compiles down to C/C++, macros and compile-time code modification
- [![last-commit](https://img.shields.io/github/last-commit/carp-lang/Carp.svg)](https://github.com/carp-lang/Carp) [Carp](https://github.com/carp-lang/Carp) [Type-B] statically typed, no GC (Rust-like borrow checking)
- [![last-commit](https://img.shields.io/github/last-commit/tomhrr/dale.svg)](https://github.com/tomhrr/dale) [Dale](https://github.com/tomhrr/dale) [Type-B] Lisp-flavoured C with additional features, no GC, LLVM backend
- [![last-commit](https://img.shields.io/github/last-commit/digego/extempore.svg)](https://github.com/digego/extempore) [Extempore](https://github.com/digego/extempore) [Type-S] designed for live coding and music performances, temporal scheduling based on audio card sample rate
- [![last-commit](https://img.shields.io/github/last-commit/JeffBezanson/femtolisp.svg)](https://github.com/JeffBezanson/femtolisp) [FemtoLisp](https://github.com/JeffBezanson/femtolisp) [Type-S] scheme-like lisp, powers the compiler of the Julia language
- [![last-commit](https://img.shields.io/github/last-commit/nakkaya/ferret.svg)](https://github.com/nakkaya/ferret) [Ferret](https://ferret-lang.org/) [Type-C] aimed towards embedded systems
- [![last-commit](https://img.shields.io/github/last-commit/janet-lang/janet.svg)](https://github.com/janet-lang/janet) [Janet](https://janet-lang.org/) [Type-B] embedable, large standard library, GC
- [![last-commit](https://img.shields.io/github/last-commit/saman-pasha/lcc.svg)](https://github.com/saman-pasha/lcc) [Lcc](https://github.com/saman-pasha/lcc) [Type-A] Lisp-like syntax for writing C
- [![last-commit](https://img.shields.io/github/last-commit/dundalek/liz.svg)](https://github.com/dundalek/liz) [Liz](https://github.com/dundalek/liz) [Type-A] written as EDN, compiles to Zig, customizable memory allocators, native binaries for many architectures
- [![last-commit](https://img.shields.io/github/last-commit/attila-lendvai/maru.svg)](https://github.com/attila-lendvai/maru) [Maru](https://www.piumarta.com/software/maru/) [Type-B] minimal self-hosting lisp, multimethods, user-defined types and structures, GC
- [![last-commit](https://img.shields.io/github/last-commit/picolisp/picolisp.svg)](https://github.com/picolisp/picolisp) [PicoLisp](https://picolisp.com) [Type-B] compiled to bytecode and interpreted, C and Java interop, built-in  database and GUI
- [![last-commit](https://badgen.net/gitlab/last-commit/owl-lisp/owl?.svg)](https://gitlab.com/owl-lisp/owl) [Owl Lisp](https://gitlab.com/owl-lisp/owl) [Type-S] dialect of the Scheme, code can be interpreted or compiled into C files
- [![last-commit](https://img.shields.io/github/last-commit/Toccata-Lang/toccata.svg)](https://github.com/Toccata-Lang/toccata) [Toccata](https://github.com/Toccata-Lang/toccata) [Type-C] Clojure-inspired, gradually typed, no nil values, reference counting, compiles into native binaries

### C#

- [![last-commit](https://img.shields.io/github/last-commit/clojure/clojure-clr.svg)](https://github.com/clojure/clojure-clr) [Clojure CLR](https://github.com/clojure/clojure-clr) [Type-C] great for game development with [Arcadia](arcadia-unity.github.io/) and unity3d


### Erlang

- [![last-commit](https://img.shields.io/github/last-commit/clojerl/clojerl.svg)](https://github.com/clojerl/clojerl) [Clojerl](https://github.com/clojerl/clojerl) [Type-C]
- [![last-commit](https://img.shields.io/github/last-commit/lfe/lfe.svg)](https://github.com/lfe/lfe) [Lisp Flavored Erlang](http://lfe.io/) [Type-A]

### Fortran

- [fscheme](https://genepi.qimr.edu.au/Staff/davidD/Scheme/SIOM.html) [Type-S] small scheme interpreter written in Fortran 95
- [![last-commit](https://badgen.net/gitlab/last-commit/codetk/schemetran?.svg)](https://gitlab.com/codetk/schemetran) [Schemetran](https://gitlab.com/codetk/schemetran) [Type-A] Expressing Fortran computations in Scheme, compiles to readable Fortran code

### Go

- [![last-commit](https://img.shields.io/github/last-commit/candid82/joker.svg)](https://github.com/candid82/joker) [Joker](https://joker-lang.org/) [Type-C] interpreter, linter, great for scripting, Go interop is very limited
- [![last-commit](https://img.shields.io/github/last-commit/glycerine/zygomys.svg)](https://github.com/glycerine/zygomys) [Zygo](https://github.com/glycerine/zygomys) [Type-B] embedable, call into native Go using reflection, optional infix syntax
- [![last-commit](https://img.shields.io/github/last-commit/zylisp/zylisp.svg)](https://github.com/zylisp/zylisp) [ZYLISP](https://github.com/zylisp/zylisp) [Type-A] simple Lisp that compiles to Go (source or bytecode)

### Java

- [![last-commit](https://img.shields.io/github/last-commit/armedbear/abcl.svg)](https://github.com/armedbear/abcl) [ABCL](https://common-lisp.net/project/armedbear/) [Type-L] CL interpreter and compiler, embedable using Java scripting API (JSR-223
- [![last-commit](https://img.shields.io/github/last-commit/lsevero/abclj.svg)](https://github.com/lsevero/abclj) [Armed Bear Clojure](https://github.com/lsevero/abclj) [Type-C+L] Common Lisp embedded in Clojure via ABCL
- [![last-commit](https://img.shields.io/github/last-commit/clojure/clojure.svg)](https://github.com/clojure/clojure) [Clojure](https://clojure.org/) [Type-C]
- [![last-commit](https://badgen.net/gitlab/last-commit/kashell/Kawa?.svg)](https://gitlab.com/kashell/Kawa) [Kawa](https://www.gnu.org/software/kawa/) [Type-S] scheme implementation (R7RS)
- [![last-commit](https://img.shields.io/github/last-commit/picolisp/picolisp.svg)](https://github.com/picolisp/picolisp) [PicoLisp](https://picolisp.com) [Type-B] compiled to bytecode and interpreted, C and Java interop, built-in  database and GUI

### JavaScript

- [![last-commit](https://img.shields.io/github/last-commit/biwascheme/biwascheme.svg)](https://github.com/biwascheme/biwascheme) [BiwaScheme](https://www.biwascheme.org/) [Type-S] compact Scheme written in JavaScript, integrates well with web browsers and Node
- [![last-commit](https://img.shields.io/github/last-commit/clojure/clojurescript.svg)](https://github.com/clojure/clojurescript) [ClojureScript](https://clojurescript.org/) [Type-C]
- [![last-commit](https://img.shields.io/github/last-commit/anko/eslisp.svg)](https://github.com/anko/eslisp) [eslisp](https://github.com/anko/eslisp) [Type-A] S-expression syntax for ECMAScript/JavaScript, Lisp-like macros
- [JACL](https://tailrecursion.com/JACL/) [Type-L]  extended subset of Common Lisp, async reader and REPL development workflow
- [![last-commit](https://img.shields.io/github/last-commit/6502/JSLisp.svg)](https://github.com/6502/JSLisp) [JSLisp](https://www.jslisp.org) ([source](https://github.com/6502/JSLisp)) [Type-L] Lisp-2, similar to Common Lisp, includes GUI library and IDE
- [![last-commit](https://img.shields.io/github/last-commit/jcubic/lips.svg)](https://github.com/jcubic/lips) [LIPS](https://lips.js.org) [Type-S] similar to BiwaScheme, has better notation to call JS functions
- [![last-commit](https://img.shields.io/github/last-commit/sctb/lumen.svg)](https://github.com/sctb/lumen) [Lumen](https://github.com/sctb/lumen) [Type-A] self-hosted Lisp for Lua and JavaScript, uses arrays as first-class datastructures
- [![last-commit](https://img.shields.io/github/last-commit/ska80/parenscript.svg)](https://gitlab.common-lisp.net/parenscript/parenscript) [Parenscript](https://common-lisp.net/project/parenscript/) [Type-L] Common Lisp to JavaScript translator, native JS types, native calling convention
- [![last-commit](https://img.shields.io/github/last-commit/racketscript/racketscript.svg)](https://github.com/racketscript/racketscript) [RacketScript](https://github.com/racketscript/racketscript) [Type-S] Racket to JavaScript compiler, interop with both Racket and JS ecosystem
- [![last-commit](https://img.shields.io/github/last-commit/cxxxr/valtan.svg)](https://github.com/cxxxr/valtan) [Valtan](https://github.com/cxxxr/valtan) [Type-L] Common Lisp to JavaScript compiler
- [![last-commit](https://img.shields.io/github/last-commit/dyoo/whalesong.svg)](https://github.com/dyoo/whalesong) [Whalesong](https://www.hashcollision.org/whalesong/) [Type-S] Racket to JavaScript compiler
- [![last-commit](https://img.shields.io/github/last-commit/Gozala/wisp.svg)](https://github.com/Gozala/wisp) [Wisp](https://github.com/Gozala/wisp) [Type-C] Clojure-like, has protocols, no persistent data structures

### Julia
- [![last-commit](https://img.shields.io/github/last-commit/swadey/LispSyntax.jl.svg)](https://github.com/swadey/LispSyntax.jl) [LispSyntax.jl](https://github.com/swadey/LispSyntax.jl) [Type-A] Clojure-like lisp syntax to Julia translator with convenience macros, uses Julia's compiler and JIT

### Lua

- [![last-commit](https://img.shields.io/github/last-commit/bakpakin/Fennel.svg)](https://github.com/bakpakin/Fennel) [Fennel](https://fennel-lang.org/) [Type-A] full Lua compatibility, embedable, compiled code with no runtime dependency
- [![last-commit](https://img.shields.io/github/last-commit/sctb/lumen.svg)](https://github.com/sctb/lumen) [Lumen](https://github.com/sctb/lumen) [Type-A] self-hosted Lisp for Lua and JavaScript, uses arrays as first-class datastructures
- [![last-commit](https://img.shields.io/github/last-commit/SquidDev/urn.svg)](https://github.com/SquidDev/urn) [Urn](https://urn-lang.com/) [?] focus on minimalism, should work with LuaJIT, influenced by Common Lisp and Clojure

### Objective-C

- [![last-commit](https://img.shields.io/github/last-commit/jsloop42/dreamlisp.svg)](https://github.com/jsloop42/dreamlisp) [DreamLisp](https://github.com/jsloop42/dreamlisp) [Type-B] Clojure-inspired, originally based on MAL, added modules, lazy collections
- [![last-commit](https://img.shields.io/github/last-commit/programming-nu/nu.svg)](https://github.com/programming-nu/nu) [nu](https://github.com/programming-nu/nu) [?] interpreted

### OCaml

- [![last-commit](https://img.shields.io/github/last-commit/jaredly/myntax.svg)](https://github.com/jaredly/myntax) [Reason-Lisp](https://github.com/jaredly/myntax) [Type-A] very incomplete

### Python

- [![last-commit](https://img.shields.io/github/last-commit/hylang/hy.svg)](https://github.com/hylang/hy) [Hy](https://github.com/hylang/hy) [Type-A] compiles to Python AST, use Python ML libraries, runs on PyPy
- [![last-commit](https://img.shields.io/github/last-commit/gilch/hissp.svg)](https://github.com/gilch/hissp) [Hissp](https://github.com/gilch/hissp) [Type-A] compiles to a functional subset of Python, macro metaprogramming with Python ecosystem
- [![last-commit](https://img.shields.io/github/last-commit/pixie-lang/pixie.svg)](https://github.com/pixie-lang/pixie) [Pixie](https://github.com/pixie-lang/pixie) [Type-B] Clojure inspired, written in RPython, custom GC and JIT

### R

- [![last-commit](https://img.shields.io/github/last-commit/dirkschumacher/llr.svg)](https://github.com/dirkschumacher/llr) [llr](https://github.com/dirkschumacher/llr) [Type-C] Clojure inspired, in R compiles and interops with R

### Rust

- [![last-commit](https://img.shields.io/github/last-commit/ytakano/blisp.svg)](https://github.com/ytakano/blisp) [BLisp](https://ytakano.github.io/blisp/) [Type-B] statically typed scripting language, type inference, algebraic data types, generics
- [![last-commit](https://img.shields.io/github/last-commit/fleabitdev/glsp.svg)](https://github.com/fleabitdev/glsp) [GameLisp](https://gamelisp.rs) [Type-B] scripting language for Rust game development, interpreted, pattern‑matching, coroutines, macros
- [![last-commit](https://img.shields.io/github/last-commit/murarth/ketos.svg)](https://github.com/murarth/ketos) [Ketos](https://github.com/murarth/ketos) [Type-B] scripting and extension language for Rust programs, compiled to bytecode
- [![last-commit](https://img.shields.io/github/last-commit/timothypratley/rustly.svg)](https://github.com/timothypratley/rustly) [Rustly](https://github.com/timothypratley/rustly) [Type-C] transpiler, only small subset of Clojure supported

### Shell

- [![last-commit](https://img.shields.io/github/last-commit/alandipert/gherkin.svg)](https://github.com/alandipert/gherkin) [Gherkin](https://github.com/alandipert/gherkin) [Type-B] (dormant) implemented in Bash, shell interop
- [![last-commit](https://img.shields.io/github/last-commit/chr15m/flk.svg)](https://github.com/chr15m/flk) [Fleck](https://github.com/chr15m/flk/) [Type-A] Clojure-like, based on [Mal](https://github.com/kanaka/mal/), packaged as single-file Bash script

### VHDL

- [![last-commit](https://img.shields.io/github/last-commit/domus123/vhdlisp.svg)](https://github.com/domus123/vhdlisp) [Vhdl Lisp](https://github.com/domus123/vhdlisp) - alternative s-expression based notation to describe programmable integrated circuits (FPGAs)

### WASM

- [![last-commit](https://img.shields.io/github/last-commit/Arboreta/arboreta-wasm.svg)](https://github.com/Arboreta/arboreta-wasm) [Arboreta WASM](https://github.com/Arboreta/arboreta-wasm) [?] Common Lisp tooling for WebAssembly
- [![last-commit](https://img.shields.io/github/last-commit/roman01la/clj-wasm.svg)](https://github.com/roman01la/clj-wasm) [clj-wasm](https://github.com/roman01la/clj-wasm) [Type-A] Clojure-flavored WASM's text format
- [![last-commit](https://img.shields.io/github/last-commit/dundalek/liz.svg)](https://github.com/dundalek/liz) [Liz](https://github.com/dundalek/liz) [Type-A] general purpose programming language, supports WASM compilation target
- [![last-commit](https://img.shields.io/github/last-commit/google/schism.svg)](https://github.com/google/schism) [Schism](https://github.com/google/schism) [Type-S] self-hosting compiler from a subset of R6RS Scheme to WebAssembly

## Misc

- [Bel](http://paulgraham.com/bel.html) - self-hosted lisp dialect, see also markdown formatted [mirror](https://github.com/alephyud/bel)
  - [Language::Bel](https://github.com/masak/bel) - implementation of Bel in Perl 5, includes extensive test suite
  - [Chime](https://github.com/jeremyschlatter/chime/) - implementation of Bel written in Haskell
  - [Babybel](https://github.com/cookrn/babybel) - Ruby implementation of Bel
  - [Bel-sml](https://github.com/niyarin/bel-sml) - implementation written in Standard ML
- [uLisp](http://www.ulisp.com/) - Lisp for microcontrollers, fits into 2 Kbytes of RAM
- [CLJSL](https://github.com/IGJoshua/cljsl) - subset of Clojure compiled to GLSL for GPU programming
- A list of more [Clojure-like languages](https://github.com/chr15m/awesome-clojure-likes).
- Additional "write C in Lisp" [projects](https://www.reddit.com/r/lisp/comments/e10spm/a_list_of_various_lispflavored_programming/f8n6qxa/) (most of them not ready for a prime time).
- [Build your own lisp](http://www.buildyourownlisp.com/) - a book describing building a Lisp dialect
- See also list of languages  [implemented in Lisp](https://github.com/vindarel/list-of-languages-implemented-in-lisp).
- [Map of Common Lisp implementations](https://twitter.com/dk_jackdaniel/status/698157022483771392/photo/1)
- [Benchmarks of Scheme implementations](https://ecraven.github.io/r7rs-benchmarks/) 

## Contribute

Anything incorrect? Is there an interested project that is missing? Open an issue or PR to request adding a project to the list.
