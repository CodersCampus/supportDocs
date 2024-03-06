**Streams! What the heck is that?**  

****

Think of Java Streams as a convenient way to work with collections (like lists or arrays) by allowing you to perform operations on the elements easily. It's like a set of tools that helps you filter, transform, and manipulate data in a more readable and concise manner.\
Resources I found helpful:\
[This](https://youtu.be/Q93JsQ8vcwY?si=QOFlw4HA7_6UuABA) Amigo’s Code youtube is great at showing all the built in methods/functionality of Streams.\
[Another](https://youtu.be/t1-YZ6bF-g0?si=Lwk4BbJCb8o1u9o8) youtube from Joe James he does an AMAZING job explaining Streams.\
If you’d rather read about them, other than what I have below, [This](https://stackify.com/streams-guide-java-8/) website has wonderful explanations and examples.

****

Here's a super simple analogy:

****

Imagine you have a bucket of numbers, and you want to pick out only the even ones and write them down. Using Java Streams is like having a magic wand that lets you do this in a few lines of code without creating a mess.

****

import java.util.Arrays;

import java.util.List;

****

public class StreamExample {

    public static void main(String\[] args) {

        List\<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

****

        // Magic wand (Java Stream) to pick out even numbers and write them down

        numbers.stream()\
//the line just below this is saying: if the result of that number can be divided by two without a remainder, it’s an even number so filter it.

               .filter(n -> n % 2 == 0)

               .forEach(System.out::println);

    }

}

In this analogy, the filter part is like selecting only the even numbers, and the forEach part is like writing them down one by one. Java Streams make this process more readable and neat.\
**Why use Streams?**

****

Concise Code: Streams allow you to write more readable and concise code by utilizing lambda expressions and method chaining.

Parallel Processing: Streams can automatically parallelize certain operations, making it easier to take advantage of multi-core processors.

Immutability: Streams are immutable, meaning that they don't modify the original data source. This makes them safer and easier to reason about.

****

What kinds of things can streams do??

Here are some common operations you can perform with streams:

****

**1. Creating a Stream**

You can create a stream from various data sources like collections, arrays, or even individual elements:

****

// From a collection

List\<String> names = Arrays.asList("Alice", "Bob", "Charlie");

Stream\<String> namesStream = names.stream();

****

// From an array

String\[] languages = {"Java", "Python", "C++"};

Stream\<String> languagesStream = Arrays.stream(languages);

****

// From individual elements

Stream\<Integer> numbersStream = Stream.of(1, 2, 3, 4, 5);

****

**2. Filtering**

You can use the filter operation to keep only the elements that match a certain condition:

****

Stream\<String> longNames = namesStream.filter(name -> name.length() > 5);

****

**3. Mapping**

The map operation allows you to transform each element of the stream into something else:

****

Stream\<Integer> nameLengths = namesStream.map(String::length);

****

**4. Sorting**

You can sort the elements of a stream using the sorted operation:

****

Stream\<String> sortedNames = namesStream.sorted();

****

**5. Reducing**

The reduce operation combines all the elements of a stream into a single value:

****

int sum = numbersStream.reduce(0, Integer::sum);

****

**6. Collecting**

Finally, you can collect the elements of a stream into a new collection using the collect operation:

****

List\<String> uppercaseNames = namesStream.map(String::toUpperCase)

                                         .collect(Collectors.toList());
