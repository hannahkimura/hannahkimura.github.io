---
layout: default
title: Decaf Compiler 
parent: RESEARCH/PROJECTS
nav_order: 1
---

# Designing and Implementing a compiler!
In this project, I worked in a team of four to build a compiler fully developed in rust that takes Decaf programs, a subset of C, as input and generates executable x86 code as output. 

Click the link below to see the design doc for our compiler, which includes a high-level description of how our compiler works! In the design doc we discuss our strategies for scanning, parsing, semantic checking, low-level IR generation, codegen, and dataflow optimizations, and conclude with a deep dive into our register allocation and further
optimizations implemented in our final implementation.
* [Design Document](compiler.pdf){: .btn .btn-outline }


<!-- 
### Worked in a team of four to build a compiler fully developed in rust that takes Decaf programs, a subset of C, as input and generates executable x86 code as output.

NOTE: Because this project was done in a class, I cannot make the code public. If grad schools would like access for admissions, please email me to let me know.

## STAGE 1: Scanner and Parser

Before forming a team, we all coded our own scanner and parser. I used ANTLR and scala to generate my scanner and parser. 

After stage 1, I joined three others to finish coding our compiler. We decided to use Rust to do the rest of our project.

## STAGE 2: Intermediate Representation  
Our IR has two phases: The build phase and the checking phase. The build phase constructs the actual IR tree. Our IR is very similar to our parse tree, but we define scope the program, method, and blocks. The scope contains the symbol table for those respective program segments (the global table is in the program scope).  The symbol table is a list of table entries which contain relevant information about identifiers, types, their constant status, and their source info. Each scope also has a reference to its parent scope. 

During the construction of these symbol tables, we also pull relevant IR semantic errors which are purely to do with scoping (i.e. declaring multiple variables with the same name in the same scope). This was simply due to the increased simplicity of doing these checks here with a half-constructed scope rather than in the IR checker. 

Our second phase was the semantic checker. Here, we visit each node, first visiting its children and then with the data brought from its children (i.e. their types in an binary expression) we then semantic check the entire node. We did this with a visitor pattern which passed down the target node as well as the scope to evaluate it in. This made asynchronously working through checks easier since checks could be constructed per node and largely independently. Aside from the visitor pattern, we also created a robust helper function for determining the relevant type of complex expressions, which was used in nearly all locations where expression type was relevant.  -->

