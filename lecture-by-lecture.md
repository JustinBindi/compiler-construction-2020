# Lecture by Lecture

- [Lecture 1.1](lecture-1.1.md): Overview, Assessment, Syllabus.

### Part 1: Finite Automata

- [Lecture 1.2](lecture-1.2.md): Deterministic Finite Automata (DFA).
- [Lecture 2.1](lecture-2.1.md): 
  - Problem Class on Finite Automata. 
  - [*Why do Java and Python not have goto statements?*](https://hackmd.io/@alexhkurz/rJ5wS-0f8).
- [Lecture 2.2](https://hackmd.io/@alexhkurz/B11YSGCz8): Non-deterministic Finite Automata (NFA).  
- Lecture 3.1: 
  - For a review of NFA, we did [Exercise 2.3.2 on page 66](https://mcdtu.files.wordpress.com/2017/03/introduction-to-automata-theory.pdf) together. 
  - Then we studied different ways of [Composing Automata](https://hackmd.io/@alexhkurz/ryV_FU7XI).
- [Lecture 3.2](https://hackmd.io/@alexhkurz/HkoNj8mmU): Eliminating epsilon transitions, translating regular expressions into DFAs.

### Part 2: Parsing

- **Lecture 4.1**: **How to build an interpreter in one lecture**. Chapter 2.1 - 2.6 of [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf). For installation  introductions see the [BNFC homepage](http://bnfc.digitalgrammars.com) or our own [BNFC installation instructions](https://github.com/alexhkurz/compiler-construction-2020/blob/master/BNFC-installation.md). *Homework* (mandatory): 
  - Install Haskell and BNFC following the [BNFC installation instructions](https://github.com/alexhkurz/compiler-construction-2020/blob/master/BNFC-installation.md) and get the calculator running. *Deadline: Monday, March 2* (we need this Tuesday in class). 
  - Read the [BNFC tutorial](http://bnfc.digitalgrammars.com/tutorial/bnfc-tutorial.html) or the [short version](bnfc-tutorial-short.md) which contains what we covered in the lecture.
  - Convince yourself that the grammar in `Calc.cf` has only one parse tree for `1+2*3`.

- **Lecture 4.2**: **How to use a grammar for debugging a program**. Exercise 2 in  [BNFC self check](https://github.com/alexhkurz/compiler-construction-2020/blob/master/BNFC-example.md). *Homework* (mandatory): Find the bug in the program of [Exercise 2](https://github.com/alexhkurz/compiler-construction-2020/blob/master/BNFC-example.md). *Homework* (optional): Study the grammar of a language you know, for example [C](https://cs.wmich.edu/~gupta/teaching/cs4850/sumII06/The%20syntax%20of%20C%20in%20Backus-Naur%20form.htm) or [Java](https://docs.oracle.com/javase/specs/jls/se11/html/jls-19.html).


- **Lecture 5.1**:  **How to build a grammar**. We explain how one can come up with the grammar of C-- of the [BNFC tutorial](http://bnfc.digitalgrammars.com/tutorial/bnfc-tutorial.html), see [here](bnfc-tutorial-C--.md) for a short version of the tutorial. *Homework* (mandatory): Play around with changing the grammar of C-- (and possibly the program). Post your findings on the discussion group.

- **[Lecture 5.2](https://hackmd.io/@alexhkurz/rk5PsF2EI)**: **How does shift-reduce parsing work?**  How to use a `.info`-file? 
  - *Homework* (mandatory): Do the exercises from the lecture notes. These exercises are relevant for tests and final.
  - *Homework* (optional): Study ParCalc.info and understand how it describes a determinstic algorithm.

- **6.1:** Test 1. 

- **Assignment 2**: [Grammar and Parser for C++](http://www.grammaticalframework.org/ipl-book/assignments/assignment1/assignment1.html). You can start from `bnfc/examples/cpp/cpp.cf`, see also [here](https://github.com/alexhkurz/compiler-construction-2020/blob/master/Sources/Cpp/cpp.cf).  Deadline for the first test file is Wed, March 11, (11:59 pm PST), for the rest of the assignment Wed, March 18, (11:59 pm PST). I would prefer if you used the same repo as for Assignment 1.

- [Lecture 6.2](https://hackmd.io/@alexhkurz/SJx6T5R48): Shift/reduce and reduce/reduce conflicts. **Homework:** Do the exercise from the lecture notes. These exercises are relevant for Assignment 2.

- [Lecture 7.1](https://hackmd.io/@alexhkurz/SkXrrBuSI): How to debug a grammar? In the 8:30 lecture, we spent most of the time discussing the [dangling else](https://en.wikipedia.org/wiki/Dangling_else) (good Wikepedia article). We wrote out some (improvised) grammar rules such as

      Exp ::= ExpIf | ExpIfElse | C | D | ...
      ExpBool ::= A | B | ...
      ExpIf ::= "if" ExpBool "then" Exp 
      ExpIfElse ::= "if" ExpBool "then" Exp "else" Exp 

  and analysed how a shift-reduce parser would parse
  
      if A then if B then C else D

---

... the material below is in draft form ...



- [Lecture ??](https://hackmd.io/@alexhkurz/SJ4sbGyrU): How does the LALR(1) parser generated by BNFC and Happy work?

...

##### Part 3: Type Checking
...

##### Part 4: Interpretation
...

##### Part 5: Code Generation
...
