---
tags: cssi, python, importing
level: 1
languages: python
---

#Python - Importing Libraries and Modules

#Objectives:

+ Know how to Import a python class/library/module into another file


#Motivation:
We can think about our classes as little factories we have set up to chug along and churn out objects when we need them. It is best practice to keep these factories separate from the rest of our python code. Classes should exist on their own, in their own .py file. By keeping them separate from the rest of our code, we can include a class we have made in any python app we are creating, as long as they are in the same directory. All we have to do is import the class!

#Lesson: Import a Class
+ Open up the file that you saved the class you made into - our in class example is called musician.py

In order to access the class contained in musician.py from another python script, we need to import it. If we are creating a new script for a music festival app on a file called festival.py, we can import our Musician class by including this code at the top of the file:

```python
import musician.py
from musician.py import *
```
The first line imports the musician.py file itself. The second line imports all the classes and functions contained in that musician.py file.

Now, when we create a new instance of Musician within our music festival script file, the Musician class will be able to process that information and the factory can churn out some musician objects for us. So if we try to create a new instance of musician on our festival.py script, it will work!

#Lesson: Import a Library/Module
We can similarly import different python libraries to use and reference within our scripts. Remember when we linked to the JQuery library for Javascript? There are tons of python libraries out there that we can import into our scripts. <a href="http://pythontips.com/2013/07/30/20-python-libraries-you-cant-live-without/">Here’s a great list of possibilities!</a> Libraries are often called modules in python - a module is a file containing Python definitions and statements, our file containing our Musician class, musician.py, could also be referred to as a module.

Let’s experiment with a basic python library. Say you want your python script to be able to select a random number, what should we do? There is no built in function to randomize the selection in python, but there is a randomizer library, contained in a file called random.py . You can find documentation on this library <a href="https://docs.python.org/2/library/random.html">here</a> to learn about all the different function you can call from it.

**CODE ALONG**:
+ Create a new script file called random-numbers.py
+ Import the random library and write this code:

```python
import random

print random.randint(1,3)

```

Save and run your script in the command line at least 5 times. What is happening? What does the function randint do?

**PARTNER PROGRAMMING**:

<a href="https://github.com/learn-co-curriculum/cssi-5.2-monopoly-dice-mini-app">Basic Random Lab: Monopoly Auto Dice Roll Mini App</a>

Let's use the random library to create an automatic dice roller for a game of Monopoly!
In Monopoly, at the beginning of each turn a player rolls two six sided dice. The numbers rolled on each die are added together to tell the player how many spaces to move. If the player rolls doubles, if they roll the same value on each die, then they get to roll again. If they don’t roll doubles, its the next player’s turn.
 Every time we run our dice roller app, it will tell us how many spaces we should move, and if we have rolled doubles and get to go again, or it it is the next player’s turn.

#Conclusion:
There are many libraries out there we can import to add to our python coding power. Just take a look at the documentation to find out what cool functionality one will add to your script! We will be using import a lot when we talk about Google App Engine next week.

#Labs:

<a href="https://github.com/learn-co-curriculum/cssi-5.4-python-dice-roll">Random Library Lab: Dice Rolling Game App</a>
