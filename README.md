TinyJava-Compiler-VMcodeGenerator
=================================

The TinyJ language is an extremely small subset of Java. Every valid TinyJ program is a valid Java program,
and has the same semantics whether it is regarded as a TinyJ or a Java program. This repository contain 
programs that generates the Parse Tree of TinyJ program, compile that program to generate Virtual Machine
Code and then execute that VM Code. 

About Tiny Java or Tiny J
=========================
The TinyJ language is an extremely small subset of Java. Every valid TinyJ program is a valid Java 
program, and has the same semantics whether it is regarded as a TinyJ or a Java program. The syntax of 
TinyJ is given by the EBNF rules given in file 'TinyJ-Assignment-1.pdf'. A Java program is a TinyJ program
if and only if it can be generated by these EBNF rules, except that TinyJ doesn’t support method name
overloading, program arguments, “return;” statements within the main() method, and ints that 
are ³ 231!216 = 2,147,418,112. Reserved words of TinyJ are shown in boldface. Some names used by Java 
library packages, classes, and predefined methods (e.g., java, Scanner, main, and nextInt) are reserved 
words of TinyJ. Otherwise, IDENTIFIER here means any Java identifier consisting of ASCII characters.

My Contribution to this program:
================================
There were total of 3 TinyJ assignments, Check the bottom of this file to get hint of what each assignment does.
<br>Contribution:
<br>About 30% of Code in Tiny J(Tiny Java) assignment is written by me  -- Gurpreet Singh, and 70% is 
done by Professor Kong (Phd.-Oxford University) 
<br>I wrote code for:
<br>1) <b>ParserAndTranslator.java</b>  at location  <b>TJasn\ParserAndTranslator.java</b> 
<br>2) <b>execute()</b> method of approx. 30 Instructions at folder Location: <b>TJasn\virtualmachine\</b>
<br>3) <b>Parser.java</b>     \TJ1asn\Parser.java </b>

To know more about Tiny J:
=========================
Read files: 'TinyJ-Assignment-1.pdf', 'TinyJ-Assignment-3.pdf', 'TinyJ-Assignment-3.pdf' 

Examples:
=========
In folder 'Examples', CS316ex0, CS316ex1,.... CS316ex15 are input files to a TinyJ Program, and 
.out files like 0.out, 1.out, ...15.out are output files. Each such output file contains a Parse Tree of 
java program, and virtual machine code of the program.
TinyJ Assignment 1
==================
It will not deal with compilation of TinyJ programs, nor with execution of virtual machine code, but only 
with syntax analysis of TinyJ programs. The goal of TinyJ Assignment 1 is to complete a program that will:
<br>(a) determine whether its input file is a <program> according to the above EBNF rules, and
<br>(b) output a parse tree of the input file, if the input file is a <program>.  

TinyJ Assignment 2
==================
 Your assignment is to complete a compiler which does all of the following whenever its input is a syntactically valid TinyJ source file: 
1. It checks that declarations and uses of identifiers in the source file are consistent with Java's scope rules. 
2. As long as no errors are detected in the source file, it translates the source file into a sequence of  instructions for a 
   stack-based virtual machine whose instruction set is given below. At the same time, it writes to the output file 
   an "enhanced parse tree" of the source file; this shows the static address or the stackframe offset that the compiler has 
   allocated to each int or array reference variable, the start address of the code generated for each method, and the time at which each 
   instruction is generated. 
3. If no errors are detected in the source file then a list of the instructions generated is also written to the output file.


TinyJ Assignment 3
==================
The assignment is to further develop your TJasn program so it will correctly execute the TinyJ virtual machine (VM) instructions 
that it generates. For each VM instruction, there will be a corresponding file *instr.java in your TJasn/virtualMachine directory. 
Every such file has an execute() method. In ADDTOPTRinstr.java, HEAPALLOCinstr.java, NOPorDISCARDVALUEinstr.java, READINTinstr.java, and 
STOPinstr.java, that method is written for you. In the other 29 *instr.java files, the body of the execute() method contains a comment of 
the form /* ???????? */ which you need to replace with code that executes the corresponding VM instruction: Your code must make appropriate changes 
to the expression evaluation stack [CodeInterpreter.EXPRSTACK[]], data memory [TJ.data[]], and registers [CodeInterpreter.ESP, .PC, .FP, .ASP, etc.], 
and must produce correct output (if any). See the example at the beginning of the "How to Do the Assignment" section below.  
