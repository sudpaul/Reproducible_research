**Workflow Management**

Workflow management systems help distribute and orchestrate the work that needs to be done on 
the computational resources that are available, but also helps in tracking provenance of the 
results, by storing details of the data, the process, and the executions that take place during the analysis.

**Code Construction Workflow**

Creating and executing your code follows two different workflow patterns.

- Create code in a text file and execute it with favorite IDE
- Create code in a text file and import it as a library/packages

Generally speaking, developers do both. The difference between importing and execution is subtle.

With either of these workflows, you create your code in as modular a fashion as possible and, during the creation process, 
you execute it in one of the methods described above to check it’s working. 
Most Software developers are back and forth between their terminal and the editor, and can do fine grained testing of every 
single line of code as they’re writing it.

**Utility**

- make
- snakemake
- cmake

**Make for Reproducible Data Analysis**

 Often data analysis projects are quite complicated. You might, for example, scrape some data from the web, clean it, do some analysis on it, 
 produce some plots, and then create a presentation and/or paper. Make allows you to provide a "recipe" that describes in what order files need
 to executed in order to produce a result (a cleaned data file, some figures, a log file, etc.). Each of these build procedures is executed in 
 a seperate instance of your default shell. Makefiles are executed by simply calling make from the command line, or, less commonly, 
 by referring to a specific makefile.

 **Build workflows independent of any language**

 Make is language agnostic. This is advantageous because, despite what some language zealots seem to believe, there is not usually one best tool for 
 an entire project. Data analysis often involves shell scripting, a bit of R, Python, and who knows what else. STATA is still quite dominant in many of 
 the social sciences. Make can handle anything that can be executed from the command line (actually anything, if you use automator or something like it).

Make has encouraged me to modularize my code. Rather than having one file analysis.R/data_analysis.py that cleans your data, estimates your model(s),
and produces your plots, you can have them split up by task. This makes it easier for others to understand your code and for you to debug it. When you 
are using R in batch-mode .Rout files are automatically produced, which is the output from the interpreter, making it easier to see what, if anything,
went wrong. Modularizing your code in this manner usually necessitates writing intermediate results to file. For complex objects this can sometimes be a 
pain (though R makes it easy with .RData files, which are automatically produced when R is run in batch-mode).

With Make you can seperate your data analysis from the document which presents your analysis while retaining the automated integration between the two.