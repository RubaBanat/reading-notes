# FUNCTIONAL PROGRAMMING

![f](imgs/f.png)

---

**What is functional programming?**

*Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. The first fundamental concept we learn when we want to understand functional programming is pure functions. But what does that really mean? What makes a function pure? So how do we know if a function is pure or not? Here is a very strict definition of purity:*

- It returns the same result if given the same arguments (it is also referred as deterministic)

- It does not cause any observable side effects It returns the same result if given the same arguments Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:


       const calculateArea = (radius) => radius * radius * PI;

       calculateArea(10); // returns 314.0 ```

       Why is this an impure function? Simply because it uses a global object that was not passed as a parameter to the function.
       Now imagine some mathematicians argue that the PI value is actually 42and change the value of the global object.
       Our impure function will now result in 10 * 10 * 42 = 4200. For the same parameter (radius = 10), we have a different result. Let's fix it!
       ``` let PI = 3.14;

       const calculateArea = (radius, pi) => radius * radius * pi;

       calculateArea(10, PI); // returns 314.0 



*Now we’ll always pass thePI value as a parameter to the function. So now we are just accessing parameters passed to the function. No external object.Now we will have the answer regardless what is the convinces on the pi value of the era even though i doubt it will change anytime soon.*


---

# Strategies

- `Here are some straightforward to implement methods that can lead to easier to read code. There are no absolutes when it comes to clean code — there's always an edge case!`

- `Return early from functions
Cache variables so functions can be read like sentences.`

- `Check for Web APIs before implementing your own functionality`

---

# THE END