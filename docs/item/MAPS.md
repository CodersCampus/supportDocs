Some of your first exposure to actually code with Maps will probably be the [Map\_Practice](https://courses.coderscampus.com/students/courses/274/sections/679/lessons/5064) exercise in Unit 9 (the third exercise in that unit). This can be frustrating at first! I know it was for me, so this doc will hopefully help demystify this type of Java collection for you! 
I’ve added a lot of information below, but here is a [YouTube\_video](https://www.youtube.com/watch?v=H62Jfv1DJlU) that explains it really well too. And this [website](https://www.designgurus.io/blog/what-is-java-map-class-and-its-uses) does a great job breaking down Maps (along with HashMap, TreeMap, and LinkedHashMap). Also dives into the benefits, when to use which, and what makes them unique.
## So what are Maps?
In Java, a Map is like a dictionary that allows you to store information in pairs. Think of it as a collection where every piece of data has a unique name, and you can quickly find and retrieve that data using its name.
Maps are like personalized, efficient data organizers. They help you quickly find, update, and manage information in a way that's easy to understand and use. Whenever you have pairs of related information, and you want fast access to that information, using a map is a smart choice.


**Why Use Maps?**

**1. Organizing Information:**

Imagine you have a list of students and their grades. A map allows you to associate each student's name with their respective grade, making it easy to look up grades by student names.

**2. Fast Data Retrieval:**

If you have a large dataset, like a phone book with names and phone numbers, using a map allows you to find a phone number much faster than searching through the entire list.

**3. Uniqueness:**

Each piece of data in a map has a unique identifier, known as a key. This ensures that each item is distinct, just like a student's name in a class or a word in a dictionary.

**4. Updating Information:**

Maps are great for updating or changing information. For instance, if a student's grade changes, you can quickly update it in the map without rearranging the entire list.

**5. Deleting Information:**

Similarly, if a student leaves the class, you can easily remove their information from the map without affecting the others.\
So essentially CRUD! (Create, Read, Update, Delete, what we do with data as devs!)

**Where to Use Maps?**

**1. Data Management:**

Maps are handy when dealing with data that has clear associations. For example, managing user preferences in an application, where each user has unique settings.

**2. Counting Occurrences:**

You can use a map to count occurrences of specific items. In a game, for instance, you might use a map to track the number of times a player achieves a certain score. Like our Poker game in the exercise!

**3. Configuration Settings:**

Storing configuration settings for a program. Each setting (like screen brightness or sound volume) can be associated with a unique key.

**4. Caching:**

Maps are useful for caching data. If you've computed a result once, you can store it in a map, and the next time you need it, you can retrieve it quickly without recalculating.

**There are helpful methods built in that we can take advantage of:**\
Sticking with our poker game as a reference, what are some methods we could use to do this exercise?\
.**getOrDefault(Object key, V defaultValue):**- Retrieves the value associated with the specified key or a default value if the key is not present. So we could use this to update the flush count to handle the case where the player’s name is not already in the map.\
**.put(K key, V value):**\
\- Adds a key-value pair to the map, you can use it to update the flush count map when a flush hand is encountered.\
\- Example:\
    flushCountMap.put(playerName, flushCountMap.getOrDefault(playerName, 0) + 1);\
**.get(Object key)**- Retrieves the value associated with the specified key, for example, if we wanted a count of all the flushes a player had we could use this method.\
\- Example:\
&#x20;          Integer flushCount = flushCountMap.get(playerName);\
.**remove(Object key):**-Removes the mapping for a key from this map if it is present. So we could use this method  to remove a player (key) from the flush count map if we need to.\
\- Example:\
    flushCountMap.remove(playerName);\
**.forEach(key, value)**

\- This is a way of iterating through the elements of a collection, like a loop, .forEach is not a traditional loop construct like “for” or “while”, it serves a similar purpose by allowing you to iterate over elements and perform actions\
\- Comparison example of a .forEach vs a “for” loop:\
For loop:\
List\<String> myList = Arrays.asList("apple", "banana", "orange");

****

for (String fruit : myList) {

    System.out.println(fruit);

}

And here is the same thing done with a .forEach\
List\<String> myList = Arrays.asList("apple", "banana", "orange");

****

myList.forEach(fruit -> System.out.println(fruit));

****

**.keySet()**Allows you to use just the keys in a set of data, for our poker example, it we just wanted the player’s names, and nothing else, if we had a Map called “flushCountMap” with the players names as a key, and the number of their flushes in the poker game as a value. We could use the following code example to get just the keys,iterate over them, and print them out:\
    Set\<String> playerNames = flushCountMap.keySet();

****

        for (String playerName : playerNames) {

            System.out.println(playerName);

        }\
**.values()**Does the same thing as the above .keySet, but this is used just to get the values.\
**.containsKey(Object key)**used to check if a specific key is present in a Map, for example, let’s say we wanted to check if a specific player exists in our map. Let’s see if we have a player named Bob:\
boolean bobIsPresent = playerScores.containsKey("Bob");\
You won’t need all of these methods in that exercise, but they are good to know! 
