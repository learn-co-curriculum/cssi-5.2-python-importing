# cssi-5.2-python-importing
Importing Libraries and Modules

We can think about our classes as little factories we have set up to chug along and churn out objects when we need them. It is best practice to keep these factories separate from the rest of our python code. Classes should exist on their own, in their own .py file. By keeping them separate from the rest of our code, we can include a class we have made in any python app we are creating, as long as they are in the same directory. All we have to do is import the class!

## Import A Class:
I’ve saved our Musician class to a file called `musician.py`.

Let’s imagine I’m creating an app in a new file that is going to be used to organize a music festival. I’m writing that app in a new python script doc that I’ll call festival.py. My Musician class could definitely come in handy for this app! So I am going to import my Musician class at the top of my new app file like this:
```python
import musician.py
from musician.py import *
```
The first line imports the musician.py file itself. The second line imports all the classes and functions contained in that musician.py file.

When we create a new instance of Musician within our music festival script file, the Musician class will be able to process that information and the factory can churn out some musician objects for us. So if we try to create a new instance of musician on our festival.py script, it will work!
```python
import musician.py
from musician.py import *
taylor = Musicians("Taylor Swift", "Pop" , "1989" , False)
print taylor.name
```
## Import Libraries/Modules:
We can similarly import different python libraries to use and reference within our scripts. Remember when we linked to the JQuery library for Javascript? There are tons of python libraries that we can import into our scripts. [Here’s a list!](http://pythontips.com/2013/07/30/20-python-libraries-you-cant-live-without/) Libraries are often called modules in python - a module is a file containing Python definitions and statements. Our file containing our Musician class, musician.py, could also be referred to as a module.

Let’s experiment with a basic python library. There is no built in function to randomize selection in python, but there is a randomizer library, contained in a file called `random.py`. [See the documentation](https://docs.python.org/2/library/random.html) to learn about all the different functions you can call from it. You can see the actual library and all the python code it contains here.
Sample use:
```python
import random

print random.randint(1,3)
```
##Conclusion:

There are many libraries out there we can import to add to our python coding power. Just take a look at the documentation to find out what cool functionality one will add to your script! We will be using import a lot when we talk about Google App Engine next week.
