__Name: Xavier Navarro__

__CSE 15L Lab Report 4__

In this lab report, I will be going over the key strokes needed to complete steps 4 through 9 on the timed section.

__Steps 1 - 3: Setup__

Before starting, make sure that are using a new fork of the ```lab7``` repository. If you already have a fork, delete and re-fork the repository. Now, we are ready to walk through all the steps of the times section!

(image of forked repository)

__Step 4: Log into ieng6__

First, you must log into your account using ```ssh```.

_Key Stroke_

```<s> <s> <h> < > <ctrl-c> <ctrl-v> <enter> <ctrl-c> <ctrl-v> <enter>``` 

Starts the ```ssh``` command to log in, copy and paste both the ieng6 account, and password.

_Entire Command_

```$ ssh cs15lsp23cv@ieng6.ucsd.edu```

(provide image showing successful log in)

__Step 5: Cloning the Repository__

In order to clone the repository, we need to use the ```git clone``` command and get access to the forked repository. This will clone the directory which you can now access through bash.

_Key Stroke_

```<g> <i> <t> < > <c> <l> <o> <n> <e> < > <ctrl-c> <ctrl-v> <enter>```

Acesses the empty git clone ```git clone```, then copy and paste path the forked repository ```https://github.com/ksirx/lab7.git```.

_Entire command_

```$ git clone https://github.com/ksirx/lab7.git```

(image of 'cloning lab7')

__Step 6: Run initial tests__

We want to run the JUnit tests which will test the java files to see if the pass on the initial try.

_Key Stroke_

```<c> <d> < > <l> <tab> <enter> <ctrl-c> <ctrl-v> <enter> <ctrl-c> <ctrl-v> < > <L> <tab> <T> <tab> <.> <j> <tab> <enter>```

Goes into the ```lab7``` directory, copy and paste the javac command from the lab 7 write up, then copy and paste java command from lab 7 write up and add ```ListExamplesTests.java``` to the end run.

_Entire command_

```$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```

```$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests.java```

(image of tests failed)

__Step 7: Edit code__

We need to access the code in ```ListExamples.java``` using vim and replace ```index1``` with ```index2``` in the final loop of merge.

_Key Stroke_

```<v> <i> <m> < > <L> <tab> <.> <tab> <enter> </> <i> <n> <d> <e> <x> <1> <enter> <shift-n> <e> <x> <i> <2> <Esc> <:> <w> <q> <enter>```

Uses the ```vim``` command to open the file, ```tab``` to fill in wanted file, ```/``` to search, <shift-n> to find last instance of term, ```e``` to go to end of word, ```x``` to remove number at end, ```i``` to enter insert mode, ```Esc``` to exit insert mode, and ```:wq``` to save and quit.

