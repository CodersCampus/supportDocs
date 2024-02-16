After learning about variable creation, primitives, classes, etc. you will start learning about methods in Java, it might not be clear right away why we even need methods, what is their purpose? How do you create one that does what you were hoping for? Let’s break it down to the basics.\
-If you are more of a video person, [here](https://youtu.be/cCgOESMQe44?si=-hNQRr6akWa2a1ep) is a video from Alex Lee (he does great tutorials) on methods.\
-And [here](https://youtu.be/-Y67pdWHr9Y?si=jxR-UNLuBYDMxped) is video from Coding With John, another great teacher, on static vs. non-static, If you ask Pete, he doesn't love using static but it’s good to learn either way right?\
-And [this](https://youtu.be/tOHJmm_SsAM?si=8OD3c4_8SH0Sgged) is a good tutorial on return statements.\
-The [Oracle\_Website](https://docs.oracle.com/javase/tutorial/java/javaOO/methods.html) (the holy site for everything Java) has some good info as well.

**What are Methods in Java?**

In Java, a method is a block of code that performs a specific task. Methods are like little programs within a larger program. They allow you to organize code, make it reusable, and break down complex tasks into smaller, more manageable pieces.

**Key Concepts:**

1\. Method Declaration: A method is defined with a signature that includes its name, return type, and parameters. Example:

&#x20;public int add(int a, int b) {

        return a + b;

    }

In this method:

-The return type is specified as int, indicating that the method will return an integer value.

-The expression a + b calculates the sum of the two integer parameters a and b.

-The result of the addition is then returned as the output of the method.\
So let’s say we created the above method called “add” in a class called MathOperations. But we want to use this method in another class? How would we do that? All we would have to do is simply create an “instance” of the class MathOperations, in the class we would like to use our “add” method in.  Let’s say we want to call our “add” method, in our _public static void main(String\[] args)_ class, We would just code it out like this:\
&#x20;  public static void main(String\[] args) {

        _// Create an instance of our MathOperations class:_

        MathOperations mathOperations = new MathOperations();

        _// Then we just call (actually type the method) the “add” method within the class_

        int result = mathOperations.add(5, 3);\
_//and to make sure everything is working the way we thought, we can use a “print line”:\
//so we can actually visualize what we are getting._

        System.out.println("Result of addition: " + result);

    }

}

But what do I mean when I say “return type”? 

In Java, the "return type" of a method specifies the type of value that the method will return when it is called and its execution is completed. The return type is declared in the method signature, indicating the type of data that the method will provide as output. It comes after the access modifier (if any) and before the method name.

In the below code block, I lay out the blueprint for a method.

\[accessModifier] returnType methodName(parameters) {

    // logic for the method would be here

}

So basically, the return type is what I want the method to give me when it’s executed, this could be a String, int, etc.\
But some methods do not have return types, when you see the word “void” in a method, this is a method with no specified return type. An example:\
public void printMessage(String message) {

    System.out.println(message);

}

The return type can be any valid data type in Java, including primitive types, objects, or even user-defined types. Like the method below:\
public String greet(String name) {

    return "Hello, " + name + "!";

}

In summary, the return type of a Java method specifies the type of value that the method will produce and return to the caller. If a method has a return type other than void, it must include a return statement in its body to provide the expected value.\
In the last example after the method name of “greet” I put (String name) as a parameter, but what is a parameter?\
&#x20;Think of parameters in a method as inputs that the method can use to perform its task. Here's a straightforward explanation. Parameters are like information or data that you provide to a method when you call it. They act as placeholders for values that the method needs to do its job. It’s kind of like a contract for the method, it’s something that, if you want to run that method it absolutely has to have the parameters to run. 

And a method can have multiple parameters, which will be separated by commas, like this:

public int add(int a, int b) {

    return a + b;

}

In the above we have two parameters, “int a” and “int b”.

In short, parameters are like pieces of information that you give to a method, enabling it to perform a specific action or calculation. They make methods flexible and reusable because you can provide different values each time you call the method.\
One thing you’ve probably also heard is the word “scope”, or you’ve wondered what all the “{“ and “}” (curly brackets) do. These curly brackets provide the “scope” of the method. Scope in a method is like a bubble where variables inside the method live. They can only be used and seen inside that bubble, not outside. It keeps things separate and organized. Method scope helps isolate variables, preventing unintended interference with other parts of the program.\
Things get a little trickier with loops and return statements, closing scanners etc, so you have to be very careful where you place things like system out print lines, and scanner.close, etc. But with practice this will come easier, so if things are not compiling that you thought perhaps they might, try moving that specific line to a different area of the code.
