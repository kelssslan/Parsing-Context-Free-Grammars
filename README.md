# Parsing-Context-Free-Grammars

Course: COMP 4750 Introduction to Natural Lanuage Processing

Topics: NLP, Parsing Text 

Professor: Dr. Harold Wareham https://www.cs.mun.ca/~harold/

A special thanks to Dr. Harold Wareham for implementing a fun and great way to learn how to clean, organize and parse context free methods. And also for giving me permission to share my experience with these assignments. Dr.Wareham spent months programming these assignments and the source codes are not available. Please sent me an email klan@mun.ca if you have any questions!


This program implements the deterministic version of the Cocke-Kasami-Younger algorithm for parsing context-tree grammars in extended Chomsky Normal Form (eCNF). 

This script will take two arguments, namely, the filenames of an eCNF grammar file and an utterance file. The output associated with these arguments is, for each utterance in the utterance file, the set of all valid parses for that utterance relative to the given grammar, where a valid parse is one whose topmost non-terminal is "S" (see below). 

In cases where an utterance does not have a valid parse, the output for that utterance will be the sentence "No valid parse".

An eCNF grammar file will consist of one or more lines, where each line describes a single rule of the form LHS -> RHS such that LHS is a non-blank string denoting a non-terminal and RHS can be either (1) one or two non-blank strings denoting non-terminals or (2) a double-quote enclosed string denoting a word. An example eCNF grammar is

![Screen Shot 2023-03-02 at 12 39 15 PM](https://user-images.githubusercontent.com/66441548/222493905-17ad7a4f-5467-4206-89d2-99b972ec6b10.png)

Non-terminal "S" is the start / utterance non-terminal in every grammar. A parse of an utterance relative to a grammar will be output as a bracketed representation of the derivation-tree associated with that parse. For example, the parses of the utterances "the man shot the elephant" and "shoot the man" relative to the example eCNF grammar above have the bracketed representations

[S [NP [Det "the"] [N "man"]] [VP [V "shot] [NP [Det "the"] [N "elephant"]]]]

and

[S [VP [V "shoot"] [NP [Det "the"] [N "man"]]]]

respectively.

**
The following ouput file shows the results when grammarFile = "g3.ecfg" and utteranceFile = "u3b.utt"
**
