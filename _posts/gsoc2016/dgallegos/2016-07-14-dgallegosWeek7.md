---
layout: post
title: Cog and PyParsing
---

Let's go to know how RoboCompDSL works.

## PyParsing
One of the most important modules used in RoboCompDSL is pyparsing. It is a Python module whose latest version to date is 2.0.4, which lets you create grammars in a simple way. Thanks to this, we can create Parsers that are in charge of a grammatical analysis of files that follow a grammatical structure. This module is vital in generating the code as it is used to interpret the DSLs defined in RoboComp.
**A simple example of it would be:**

from pyparsing import Word, alphas
greet = Word( alphas ) + "," + Word( alphas ) + "!"
hello = "Hello, World!"
print (hello, "->", greet.parseString( hello ))

**Output:**

$ Hello, World! -> ['Hello', ',', 'World', '!']

This module is used in scripts *parseIDSL.py* and *parseCDSL.py* to extract the files CDSL and IDSL necessary information that will be used to generate code routine.

## Cog
Cog is a code generator written in Python that allows you to inject Python code within a file so that, after using the generator, we get a result that depends on the injected code.
It can be used with any type of file so it does not limit its use to code generation. The RoboCompDSL tool uses this code generator for creating and modifying components of a quick and easy basis of information obtained from CDSL and IDSL files. This tool is able to generate code routine that hindered the creation of complex systems components.

**An example of use is shown in a file either:**

Static part of our file
[[[cog
import cog
fnames = ['DoSomething', 'DoAnotherThing', 'DoLastThing']
for fn in fnames:
    cog.outl("void %s();" % fn)
]]]
[[[end]]]
Another fragment of our file

**Running Cog:**

static part of the file
void DoSomething();
void DoAnotherThing();
void DoLastThing();
Another fragment of our file