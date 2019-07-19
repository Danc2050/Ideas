1) A language feature that may be beneficial to add: have a piece of code that you can write that only executes once.
  e.g., the keyword 'once' could be used.
        if once i == 2:
          print("This only happens once")

2) An application that takes a book and lets you "read" it one word at a time by flashing the words on the screen. The reason? We read faster when only needing to look at words (our eyes don't have to travel as far). There are speed reading apps and techniques for this, but no apps (to my knowledge -- must research) that actually have the ability to take the text of a book and display it in this format. You could rewind and adjust the speed at which words come on the screen etc.
Ex:   [The] -> [house] -> [was] -> [red].
UPDATE: This already exists... but they are often not free, don't have proper import (copy and paste is the primary format) and lack functionality (e.g., rewind). You could do a better job FOR SURE.

3) An AI to write a program... with some help

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

# Automating a task
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

4) This is a different implementation idea, similar to idea #3, but more centered on AI.
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