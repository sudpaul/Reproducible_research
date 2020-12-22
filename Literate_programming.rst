****************************************
Literate programming (dynamic reporting)
****************************************

Literate programming encourages meaningful documentation and inclusion of details that are usually omitted in source code such as 
the description of algorithms, design decisions, and implementation strategy. In a research context, computer programs are embedded 
within documents, such as scientific papers. This practice is also described as 'literate computing', 'literate statistical programming', 
'literate data analysis', and 'literate statistical practice', in recognition of the adoption of literate programming methods from a 
software development context into a data analysis context. Several systems, such as knitr and Jupyter allow the writing of documents, 
including papers, with the code embedded or interleaved with the text.


This programming paradigm allows developers to focus on documenting their code in a more natural way. This has the double advantage of 
aiding a new user in understanding what the code does and helping the author of the code to develop the code following a logic that can
be different from the logic of the code’s programming language.

In general, from a literate source file (a file containing both natural language and programming code) it is possible to obtain a 
documentation file (by the process called weaving) and a script file (by the process called tangling) which is interpretable by 
the target programming language.

Markdown, a simple but effective mark-up language, allows mixing natural language (with rich formatting) and code in a single document
