---
layout: post
title: Big O Notation
gh-repo: May30Sal/may30sal.github.io
gh-badge: [star, fork, follow]
cover-img: /assets/img/cover-2025-01-29.jpg
thumbnail-img: /assets/img/icon-2025-01-29.jpg
tags: [Big O. Programming. Algorithms.]
comments: true
author: Mayara Saldanha
---

Big O Notation gives us a numeric representation of the general **performance** of the code. In other words, it shows how the runtime of an algorithm grows, as the input grows. When we talk about **performance** what we usually mean is how much time and space will be needed to run te code. This subject can get very complex very fast, so I'll try to keep it simple.

First, let's understand more about time and space complexity:

**Time Complexity**

One thing we need to keep in mind is that *time complexity* is about the time that the algorithm takes to run, and not the time that the computer takes to process it. 
It happens because the computers time can be different depending on many factors, like the hardrive speed, the memory capacity, etc. That's not what Big O is about.

*Time complexity* in Big O Notation relates to how many operations are perfomed by an algorithm in order to get a task completed. Let's check some examples:

**O(1)** or **constant**<br>
A function that takes one argument and return its double.
```
   function getDouble(n) {
    return n * 2
    }
```
Here, there's only one operation being performed (n * 2), so it doesn't matter if **n** value is 10 or 10 milion, it will always take the same time to run. In this case the time complexity will be *O(1)* or *constant*, since the runtime is always the same, no matter the size of the input.

**O(n)** or **linear**<br>
A function that gets an array and returns all its elements double. 
```
  function getDouble(n) {
    for(i = 0; i < n.length; i++) {
            n[i] = n[i] * 2
        }
    return n;
    }
``` 
Here **n** is an array and to get the doubles we'll need to go through every element and perform one operation (n[i] = n[i] * 2), so the runtime will grow depending on the size of the array. If it has 10 elements, will be way faster than if it has 10 milion. The time complexity in this case will be *O(n)* or *linear*.

**O(log n)** or **logarithmic**<br>
Now let's imagine a situation where you need to find the word -memory- in your physical dictionary. Would it be easier to start looking from letter A to M, or just trying to open the dictionary randomly at the middle, like at letter J, and then go ahead from there? Probably, your answer is the second option! And that's more or less how the logarithmic time works.

Another way to visualize it would be If I ask you to guess the number I'm thinking of right now, that is in a list of 1 to 10, and let's say the number that I chose is 7. If you start guessing from 1 until you get to 7 it will take 7 chances. But if you guess somewhere in the middle, like a 5, and I say higher, so you try again somewhere in the middle from 5 to 10, you'll have exactly 7, the number that I chose! So, instead of 7 operations, you used 2. That's exactly what the Binary Search algorithm does, and it has a runtime of O(log n).

We also have **O(n log n)** that grows linear and logarithm depending on the input size, and one example would be the Quicksort algorithm. The **O(n²)** or **quadratic** time is easily visualized when we have nested loops, since the runtime increases proportionally to the input.

A rank of algorithm performance would be something like this:

<span style="color:orange">
    O(1) - Excellent<br>
    O(log n) - Good<br>
    O(n) - Fair<br>
    O(n log n) - Bad<br>
    O(n²) - Horrible
</span>

**Space Complexity**

We can also use Big O to analyze how much space (memory capacity) we need to allocate in order to run the code in our algorithm. The concept of *auxiliary space complexity* refers to the extra space required by the algorithm, not including the space already taken up by the inputs. For example, when we have to create extra variables to perform operations. Let's see again the function getDouble:

Here we are not taking any extra space, as we perform the operations direct in the input.
```
  function getDouble(n) {
    for(i = 0; i < n.length; i++) {
            n[i] = n[i] * 2
        }
    return n;
    }
``` 

Now here we created a new variable *arrDouble* to store the double values, so it will take an extra space that is auxiliary to the input space.
```
  function getDouble(n) {
    let arrDouble = n;
    for(i = 0; i < arrDouble.length; i++) {
            arrDouble[i] = arrDouble[i] * 2
        }
    return arrDouble;
    }
``` 

Some highlights about space complexity:
* Booleans, numbers, undefined and null are constant space O(1)
* Strings needs linear space O(n), as it depends on the string length
* arrays and objects are generally O(n), where *n* is the length of the array or the number of keys of the object.

That's all for today! I hope it could be helpful to clarify some basic concepts about Big O Notation and algorithms. Check some references below that have helped me to better understand the topic and write this post 🤩

📚 REFERENCES:<br>
[JS Algorithms and Data Structures Masterclass](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass/){:target="_blank"}<br>
[Big O Cheat Sheet Time Complexity Chart](ttps://www.freecodecamp.org/news/big-o-cheat-sheet-time-complexity-chart/){:target="_blank"}<br>
[Big O Asymptotic Complexity](https://www.baeldung.com/cs/big-oh-asymptotic-complexity){:target="_blank"}<br>

*Images by Freeimages.com and Freepik.com*