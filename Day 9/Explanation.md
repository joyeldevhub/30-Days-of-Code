Sure, let's go through the code step by step:

1. **Importing Required Libraries**:
   ```java
   import java.util.*;
   ```
   This line imports all classes from the `java.util` package, including the `Scanner` class and the `Map` interface, which are used in the code.

2. **Main Class Definition**:
   ```java
   class Solution {
   ```
   This defines a class named `Solution`. In Java, the name of the main class should match the filename.

3. **Main Method Declaration**:
   ```java
   public static void main(String[] argh) {
   ```
   This declares the main method. The `main` method is the entry point of any Java program. It accepts an array of strings as arguments (`String[] argh`), which are commonly named `args`. These arguments can be passed from the command line when running the program.

4. **Creating Scanner Object**:
   ```java
   Scanner in = new Scanner(System.in);
   ```
   This line creates a new `Scanner` object named `in` to read input from the standard input stream (usually the keyboard).

5. **Reading Number of Entries**:
   ```java
   int n = in.nextInt();
   ```
   This line reads an integer value from the input, which represents the number of entries (names and phone numbers) that will be provided.

6. **Initializing Phone Book**:
   ```java
   Map<String, Integer> phoneBook = new HashMap<>();
   ```
   This line initializes a `HashMap` named `phoneBook` with keys of type `String` (names) and values of type `Integer` (phone numbers). This map will store the phone book entries.

7. **Reading and Storing Entries**:
   ```java
   for (int i = 0; i < n; i++) {
       String name = in.next();
       int phone = in.nextInt();
       phoneBook.put(name, phone);
   }
   ```
   This loop iterates `n` times, where `n` is the number of entries provided earlier. Inside the loop, it reads a name and a corresponding phone number from the input and stores them in the `phoneBook` map.

8. **Querying the Phone Book**:
   ```java
   while (in.hasNext()) {
       String query = in.next();
       if (phoneBook.containsKey(query)) {
           System.out.println(query + "=" + phoneBook.get(query));
       } else {
           System.out.println("Not found");
       }
   }
   ```
   This loop continues to execute as long as there is more input available. Inside the loop, it reads a query (a name) from the input. Then, it checks if the `phoneBook` map contains the queried name using `phoneBook.containsKey(query)`. If the name is found in the phone book, it prints the name and its associated phone number. Otherwise, it prints "Not found".

9. **Closing the Scanner**:
   ```java
   in.close();
   ```
   This line closes the `Scanner` object `in` to release system resources associated with it. It's good practice to close the scanner when it's no longer needed to prevent memory leaks.
