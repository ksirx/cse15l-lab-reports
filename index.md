__Name: Xavier Navarro__

__CSE 15L Lab Report 4__

In this lab report, I will be going over the key strokes needed to complete steps 4 through 9 on the timed section.

__Steps 1 - 3: Setup__

Before starting, make sure that are using a new fork of the ```lab7``` repository. If you already have a fork, delete and re-fork the repository. Now, we are ready to walk through all the steps of the times section!

NOTE: Make sure that you have set up generating ssh keys for both ieng6 and github! This will mkae your life easier and is required to push any changes made to github.

(image of forked repository)

![Image](images/2023-05-20 (11).png)

__Step 4: Log into ieng6__

First, you must log into your account using ```ssh```.

_Key Stroke_

```<s> <s> <h> <space> <ctrl-c> <ctrl-v> <enter> <ctrl-c> <ctrl-v> <enter>``` 

Starts the ```ssh``` command to log in, copy and paste both the ieng6 account, and password.

_Entire Command_

```$ ssh cs15lsp23cv@ieng6.ucsd.edu```

(provide image showing successful log in)

![Image](images/2023-05-20 (12).png)

__Step 5: Cloning the Repository__

In order to clone the repository, we need to use the ```git clone``` command and get access to the forked repository. This will clone the directory which you can now access through bash.

_Key Stroke_

```<g> <i> <t> <space> <c> <l> <o> <n> <e> <space> <ctrl-c> <ctrl-v> <enter>```

Acesses the empty git clone ```git clone```, then copy and paste path the forked repository with ssh```git@github.com:ksirx/lab7.git```.

_Entire command_

```$ git clone git@github.com:ksirx/lab7.git```

(image of 'cloning lab7')

![Image](images/2023-05-20 (13).png)

__Step 6: Run initial tests__

We want to run the JUnit tests which will test the java files to see if the pass on the initial try.

_Key Stroke_

```<c> <d> <space> <l> <tab> <enter> <ctrl-c> <ctrl-v> <enter> <ctrl-c> <ctrl-v> <space> <L> <tab> <T> <tab> <tab> <enter>```

Goes into the ```lab7``` directory, copy and paste the javac command from the lab 7 write up, then copy and paste java command from lab 7 write up and add ```ListExamplesTests``` to the end run.

_Entire command_

```$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```

```$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```

(image of tests failed)

__Step 7: Edit code__

We need to access the code in ```ListExamples.java``` using vim and replace ```index1``` with ```index2``` in the final loop of merge.

_Key Stroke_

```<v> <i> <m> <space> <L> <tab> <.> <tab> <enter> </> <i> <n> <d> <e> <x> <1> <enter> <shift-n> <e> <x> <i> <2> <Esc> <:> <w> <q> <enter>```

Uses the ```vim``` command to open the file, ```tab``` to fill in wanted file, ```/``` to search, ```<shift-n>``` to find last instance of term, ```e``` to go to end of word, ```x``` to remove number at end, ```i``` to enter insert mode, ```Esc``` to exit insert mode, and ```:wq``` to save and quit.

_Entire Command_

```vim ListExamples.java```
  
(image of file opened inside vim)
![Image](images/2023-05-20 (6).png)
  
__Step 8: Run tests again__
  
We need to run the tests again to see if the change we made will make the test pass this time around.
  
_Key Stroke_
  
```<ctrl-c> <ctrl-v> <enter> <ctrl-c> <ctrl-v> <space> <L> <tab> <T> <tab> <enter>```
  
Run the same tests as step 6.
  
_Entire Command_
  
```$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```

```$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```
  
(insert image of test passing)
  
__Step 9: Commit and push to github account__
  
We now need to run some commands in order to save the changes that we have made to our github account.

_Key Stroke_
  
```<g> <i> <t> <space> <a> <d> <tab> <L> <tab> <.> <j> <tab> <enter> <g> <i> <t> <space> <c> <o> <m> <tab> <-> <m> <"> <n> <e> <w> <"> <enter> <g> <i> <t> <space> <p> <u> <s> <tab> <enter> ``` 
  
Using a combination of 3 commands. ```git add``` indicates which files have been changed.```git commit``` creates a snapshot of all the changes within the repository. ```git push``` pushes the changes to github.

_Entire Command_
  
```$ git add ListExamples.java```
  
```$ git commit -m "new"```
  
```$ git push```
  
(insert image of three commands)
