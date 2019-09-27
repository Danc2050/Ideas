# 1) A language feature that may be beneficial to add: have a piece of code that you can write that only executes once.
  e.g., the keyword 'once' could be used.
        if once i == 2:
          print("This only happens once")

# 2) An application that takes a book and lets you "read" it one word at a time by flashing the words on the screen. 
The reason? We read faster when only needing to look at words (our eyes don't have to travel as far). There are speed reading apps and techniques for this, but no apps (to my knowledge -- must research) that actually have the ability to take the text of a book and display it in this format. You could rewind and adjust the speed at which words come on the screen etc.
Ex:   [The] -> [house] -> [was] -> [red].
UPDATE: This already exists... but they are often not free, don't have proper import (copy and paste is the primary format) and lack functionality (e.g., rewind). You could do a better job FOR SURE.

# 3) An AI to write a program... with some help

Summary: All programs may be represented as a large flow graph, if we are to enumerate all outcomes. So, if we know the outcomes that are desirable, we can teach an AI to create a program that operates off of a flow graph as seen in figure 1. This involves both human and AI components... but AI may do most of the work.

What needs to be completed may vary, and thus, each program may vary. However, what will not vary is all possible paths a user should take. If we have the graph we have two things:

1) A "happy paths" of what a program should/could take.
2) A restriction on what paths the program should take.

Thus, as the machine learns, it may find paths that are possible in its programming logic that do not conform to the graph. Hopefully, it may learn to not take these paths by changing its logic. 

Another necessity is defining variables. It must be specified by the programmer (e.g., x is specified as what it should be (e.g., a regex value, a data type with range, etc.)). Starting out, variable x is not known. However, as the machine realizes it needs variable x, it may add variable x (type, etc.) into its program to satisfy the flow graph. 

This would minimize debugging significantly.

Furthermore, at a high level, all programs have four operations:
1) flow-control
2) input
3) output
4) computations

The first is handled, in-part (what is acceptable), by the flow-control designer. The remainder may be handled by the AI/Computer (including the part of checking for errant paths and preventing a user from taking them (e.g., error control).

## Automating a task
This program, and many "automated tasks", can be realized by realizing that every operation is a subset of a group of operations as demonstrated above in listing items 1-4. For example, item 4 includes many mathematical operations (add, subtract, divide, multiply, etc.).

The remainder of "automating a task" involves matching an operation with a implementation that covers all cases. For example, the flow graph is one in which a set (automating a program) is attempting to cover all cases inside that set (all implementation details of writing a program). For example, a program may read the flow graph and then write to a text file (crude implementation), specifying a line number. 

It may also create classes to align with individual flow control "elements". The classes may have the elements needed (e.g., 'x' in figure 1') and the subclass (sub flow control element) may check if it's parent (or sibling if it is an operation concurrently?) has that element (or just check if the line number has it...). All variables may be public or all classes members public... who knows at this point. Additionally, each flow control element may receive an index... so each class which represents an index may be hashed for quick access and retrieved and then accessed (member elements) quickly... There are many implementation details perhaps.

But...

Further questions need to be asked:
1) Does this essentially create an inefficient one function program? 
  1a) can this program be modularized through AI later?
2) How does maintanence work? (I propose that the flow graph be re-written and the AI ran again).
3) ....?

Figure 1:
    ----------
    \  if x  / 
      \    /
        ---
        |
        |
       *do*

# 4) This is a different implementation idea, similar to idea #3, but more centered on AI.
Summary: There are little implementations that I know of that converge AI/ML with programming languages. However, if a project could be linked together, the load on programmers would be severely minimized and companies would not have to pay them as much or as often. I believe that AI/ML could be used to predict what a programmer wants, without him needing to learn or know syntax or semantics.

For example, I have been working with Java date objects lately. The system is entirely convoluted. If I want a date, there are multiple ways to do it and it can be confusing which way to use and what you can return to what date object, etc.

If AI/ML could aid in this process of using libraries to get what a programmer wants, without them needing to know said libraries, this would expedite the process of programming.

My idea would be this:
- Have some sign to the compiler that this is going to be an ML/AI command (e.g., ``This is my command``).
- Let the body of that command resemble what the AI/ML will parse and search the libraries for.
  -E.g., ``Create a date object of the form 'mm/dd/yyy'`` would return a Date object (or perhaps write the code on that line) as a result.
- The AI/ML model would learn by programmer input. Was it what they were looking for? No? A series of key combinations could do the following:
  - Iterate through options *Note: I like this option the best because by choosing and sticking with this option, the programmer is signaling that it was a good option*.
  - Vote options (good or bad?).
  

#Final thoughts
I believe that this idea could bear fruit. If anything, it could be a partial implementation. A tool that a programmer could use who is just learning the language or who may not want to look up library code and take a chance on AI/ML model to find the correct library/syntax/semantics.


# AI That Uses Logic AND Math to Train A Model
From the little I know, it seems like AI/ML models use math primarily as their force to train models and logic to program the models.

But logic doesn't seem to be used as a criteria to influence the model to train. What do I mean? I'll explain.

The models that are trained are not given a list of if/else conditions, I think. Parameters are set explicitly, and only then an agent does some sort of thing based on it (logic) or an output is accepted IF (logic) confidence level is above some range. However, what if the ML/AI model sensed something and, based on it, trained itself in some way?

For example, let's assume an AI/ML model knew to perfectly visualize a panda. If a panda existed, it could then proceed to identify something else about the panda -- maybe xray the panda -- which it is not so good at in the current SOTA. Based on the initial absolute, it can begin to xray the panda and identify certain bones (fibula, etc.) and build its x-ray model.

The way we currently have it (or so I think) is that we do not identify the panda before we train the model. We train the model (randomly, even, sometimes) and use math as the primary force. But logic should be considered as a force. How can we use it?

# Program that re-inputs the same inputs you put into your program so as to enable you to debug at the exact point the problem occurred.

It is annoying, and often unnecessary, to start from point zero of a program/applicataion to get back to the point where the program failed. This project would allow one to be at the step before the program fails by saving the input the user gives to the program and giving it back to the program. Note: This will only work for some program (e.g., static rather than dynamic data-driven programs) and languages (Java or Python would be a good candidate). Android Studio would need a way to mimick the clicks a user does... which wouldn't be impossible.

# Program that turns a drawing of a tree into a programmed AST. Or...

This program would be useful for those who don't want to code an AST or lack the skills or knowledge. 

An AST has many uses (?). Particulary, in compilers.

In addition, this program could implement methods. Ideally, the program would actaully have a set of pre-programmed methods and just replicate the data (i.e., the tree). This, in theory, would reduce the need for coders to code an AST.

# A program that memorizes (or memoizes..?) previous input to a program
This is a good tool for those that do user testing.

When a user tester is testing a program they follow a linear path, starting at point 0 and moving to point x.

There are a few problems with this:
1) When they have tested paths and received a segfault at path x, they have no way to return to the previous invocation/safe place before the segfault occurred and proceed to test further. They must start at point 0.
2) When a user is testing paths, they have no ability to determine if they have traversed all paths (and what values they have inputted) unless they manually write/type this.

A few possible solutions:
1) A program that memorizes (or memoizes) the input to a given program so it can be fed back in at a later date (e.g., by ./a.out > memorizedResults).
2) A GUI that draws a tree of possible paths and includes tested solutions the user has completed.
  - Additionally, a symbolic execution engine could be run on the program pre-emptively and update the tree/picture to reduce user testing from needing to occur.


Check-out [this link][1] for symbolic execution engines

[1]: https://github.com/ksluckow/awesome-symbolic-execution#tools

# A website that lets the general population refinance student loans
Student loan repayments have interest rates of ~3-7 interest rate or more. General citizens would like to earn money back on savings, but don't always have options that yield above 1.5% (even "high" interest yield accounts). This is an option for the student to get a lower interest rate on his/her loans and the average citizen to increase the amount gained back while investing.

There are some important details:
* This should be marketed as a "crowd sourcing" type of thing... like Uber, but the vehicle is loans that you share and users get the benefit of the additional income on investment.
* A student must verify a steady source of income and documents to prove these and other important details (e.g., loan documents).
* A citizen can opt to "invest" in any part of the loan.
* A student and citizen must commit to a period of repayment and investment respectively. Thus, a student may not pay off a loan early. This ensures that the investment by the citizen is kept.

# A script to remove compiler errors from files -- WarningsBeGone

If a person compiles from the `src` directory, this program will remove (on a second compilation) the code that causes the warnings to be produced.

For example, if a long standing tool such as [this one](https://www.mersenneforum.org/mayer/README.html#download) produces [many compilation warnings](https://travis-ci.org/tdulcet/Distributed-Computing-Scripts/jobs/559866710), then the majority of these can be removed, without harming the program. Some examples:

- Easy one liners are simple...just remove the line (e.g., unused variable)
- Lines where an unused variable(s) share a line can be removed by writing the file out again, but without the same item on that line.
- set but not used

## Other ideas
- use a folder (like "build"), perhaps named "WarningsBeGone" to include the new files (without warnings)

# IsItReadyYet? -- A program to tell you when your program has finished
I check long running processes too often. A solution? Email or text me when it is done.

## Possible features
- Send hostname, $USER, etc. of machine (hint: use Teal Dulcet's script), so I know what machine finished and possibly use details about the process (e.g., name of program, PID, etc.) so I know what process finished and even could maybe grab exitcode to see if it exited succesfully and forward these details to me.

- Could be a simple pipe where the program can be started through a BASH command that is globally recognized in the `.bashrc` file.

# GraphQL -- Keep it on the server side
Is the GraphQL only on client side? It makes more sense to have it on the server side because this reduces network traffic and bits over the wire. It is the same computation time on the server side.

# OCR Screen Grab Tool
*Steps*
1) get/create a free Open Source OCR tool
2) get/create/utilize a screenshot tool
3) have the screenshot be sent through the ocr as soon as it is taken and the OCR results outputted to some file (word, doc) that the user chooses.
4) have a donate tab.
Here is a good one: http://www-e.uni-magdeburg.de/jschulen/ocr/download.html
