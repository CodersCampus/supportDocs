# Hey y'all! I know it can be a little confusing, at least it was for me, when you see folks kind of interchangeably using "Integer" and "int". What is the difference? How come sometimes we HAVE to use Integer? when is it appropriate to use "int" in our code? I've put together a few things that helped me, and will hopefully help you! 

This [youTube](https://youtu.be/osV3NKeTDr0?si=9vB-7Xe4E_NMX4_O) really breaks is down in a slow, easy to understand way, plus the little nugget that does it shows that sometimes it’s good to play around, see what works and what doesn’t, he didn’t edit one the little mistake he made, which is very normal for real devs, we make mistakes, it happens 🙂\
So the basics: Integer is a class, more specifically a **wrapper** class.  What is that? What does it do?  \
What do wrapper classes do?\
Object Conversion:

Wrapper classes enable the conversion of primitive data types into objects. For instance, an int primitive can be converted into an Integer object.\
Compatibility with Collections:

Many Java collections (like ArrayList or HashMap) work with objects, not primitives. Wrapper classes allow you to use these collections with primitive values.\
Nullability:

Unlike primitive types, wrapper classes can represent a null value. This is beneficial in scenarios where you need to express the absence of a value.\
Additional Functionality:

Wrapper classes offer additional methods and functionalities that are not available with primitive types. For instance, the Integer class provides methods for parsing strings into integers or converting integers to binary strings. \
\*Think of your “.”methods, for example “Integer.toBinaryString” the dot method is a method some smart person who works for Java created for us, something that is commonly used, so they made it easy for us.\
**What to use when?**Use int (Primitive Type) when:

You want things to be fast and use less computer memory.

You don't need to represent the absence of a value (like an empty box).

You're dealing with simple numbers and calculations.

Use Integer (Wrapper Class) when:

You might need an empty box to represent "nothing" (null).

You're working with fancy computer stuff that requires objects.

You're using collections (like lists) to store numbers.

In simpler terms, int is like a basic tool for regular numbers, and Integer is like a tool with extra features that can handle special cases. Choose the one that fits the job you're doing!\
[This](https://youtu.be/4MiEznM8y8Q?si=Cmvv1-ALFoVEuQG4) is a good video on wrapper classes, autoboxing, unboxing, and he uses Integer as an example.\
[Here](https://youtu.be/IM3c6eI6lO8?si=iGPQXIaQesifjRLS) is another video breaking down why we use wrapper classes. He uses “int” and “Integer” and why you use one, and why you use the other, as well as how autoboxing and unboxing works.\
[This ](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/int-vs-Integer-java-difference-comparison-primitive-object-types#:~:text=The%20Integer%20class%20allows%20conversion,int%20can't%20have%20any.)webpage also has a great breakdown on when to use one, and not the other.
