---
layout: post
title: Python Modules 🗂️ 
gh-repo: May30Sal/may30sal.github.io
gh-badge: [star, fork, follow]
cover-img: /assets/img/cover-2024-05-01.jpg
thumbnail-img: /assets/img/icon-2024-05-01.jpg
share-img: /assets/img/cover-2024-05-01.jpg
tags: [Python. Code. Data.]
comments: true
author: Mayara Saldanha
---

According to the [Python Docs](https://docs.python.org/3/tutorial/modules.html#modules){:target="_blank"}, a python **Module** is a file containing python definitions and statements, that can be later imported and used when necessary. As python users, we can use existing modules or create new modules. 

Python delivers some modules and built-in functions by itself [python standard library](https://docs.python.org/3/library/index.html){:target="_blank"}, like **math** or **sys**. 

Modules have **entities** that can be: functions, variables, constants, classes, and objects. Every module has a name and we need to import it before use it.

Example: **math** is a module name and **cos()** is an entity inside the **math** module.

* Some ways to import modules and their differences:

1. ``` import math ``` <br>
   Here, you import the entire module to your code and can use all its entities. The interesting thing about it is something called *namespace*. Namespace means that you can have your own entities named the same names as the module entities, and they don't cause naming issues. That's because the module is accesible in your code, but don't enter it's namespace. Check the example below:

   ```
    import math
    x = 75
    cos = math.cos(x)
    print(cos) 
    ``` 
    In this example I have a variable called *cos* and I'm also using the **math** entity called *cos()*, and they don't affect each other.
    In order to access the entity I have to use the qualification first, followed by a dot and the entity name ```math.cos()```.
    
2. ```from math import pi ``` <br>
   In this case only the entity *pi* is being imported from **math**. I can access the entity without the qualification ```print(pi)``` and it will be the only thing accessible for me from the **math** module. If I have a variable in my code with the same name *pi*, depending on where I'm importing th module, it can be overrided by it or not. So it can cause some naming issues.

3. ``` from math import * ```<br>
   This will import all entities in the **math** module and they can be accessed without the qualification (math.). It can also cause name conflicts, as the previous example.
   
4. ```from math import pi as p```<br>
   In this case, we are using an alias for the entity, that can now be accessed by the alias ``` print(p)```. It helps avoiding the name issues, in case we have a variable in the code named *pi*. 

This is the basic about python modules. I hope it helps you the same way as it helped me 🐱

You can check some basic code examples about this subject [here](https://github.com/May30Sal/Python_For_Everybody_Course/blob/main/py_cert.py){:target="_blank"} and try it yourself.


*Images by Freeimages.com and Freepik.com*