## Here's a step-by-step explanation of the provided Java code:

### Overview
The code calculates the total cost of a meal including a tip and tax based on provided percentages, then rounds the total cost to the nearest integer and prints it out.

### Step-by-Step Breakdown

1. **Imports and Class Declarations:**
   ```java
   import java.io.*;
   import java.math.*;
   import java.security.*;
   import java.text.*;
   import java.util.*;
   import java.util.concurrent.*;
   import java.util.function.*;
   import java.util.regex.*;
   import java.util.stream.*;
   import static java.util.stream.Collectors.joining;
   import static java.util.stream.Collectors.toList;
   ```
   These are import statements that bring various Java standard libraries into scope, though not all of them are used in this code snippet.

2. **Result Class and Solve Method:**
   ```java
   class Result {
       public static void solve(double meal_cost, int tip_percent, int tax_percent) {
           double tip = meal_cost * (tip_percent / 100.0);
           double tax = meal_cost * (tax_percent / 100.0);
           double total = meal_cost + tip + tax;
           System.out.println(Math.round(total));
       }
   }
   ```
   - **solve Method Signature:**
     `public static void solve(double meal_cost, int tip_percent, int tax_percent)`:
     This method takes three parameters: the base meal cost (`meal_cost`), the percentage for the tip (`tip_percent`), and the percentage for the tax (`tax_percent`).

   - **Calculate Tip:**
     `double tip = meal_cost * (tip_percent / 100.0);`
     Calculates the tip by multiplying the meal cost by the tip percentage divided by 100.

   - **Calculate Tax:**
     `double tax = meal_cost * (tax_percent / 100.0);`
     Calculates the tax in the same way as the tip.

   - **Calculate Total Cost:**
     `double total = meal_cost + tip + tax;`
     Adds the base meal cost, the tip, and the tax to get the total cost.

   - **Print Rounded Total:**
     `System.out.println(Math.round(total));`
     Rounds the total cost to the nearest integer and prints it.

3. **Main Method in Solution Class:**
   ```java
   public class Solution {
       public static void main(String[] args) throws IOException {
           BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

           double meal_cost = Double.parseDouble(bufferedReader.readLine().trim());
           int tip_percent = Integer.parseInt(bufferedReader.readLine().trim());
           int tax_percent = Integer.parseInt(bufferedReader.readLine().trim());

           Result.solve(meal_cost, tip_percent, tax_percent);

           bufferedReader.close();
       }
   }
   ```
   - **BufferedReader for Input:**
     `BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));`
     Creates a `BufferedReader` to read input from the console.

   - **Read Meal Cost:**
     `double meal_cost = Double.parseDouble(bufferedReader.readLine().trim());`
     Reads a line from the console, trims any whitespace, and converts it to a `double` representing the meal cost.

   - **Read Tip Percent:**
     `int tip_percent = Integer.parseInt(bufferedReader.readLine().trim());`
     Reads another line, trims it, and converts it to an `int` representing the tip percentage.

   - **Read Tax Percent:**
     `int tax_percent = Integer.parseInt(bufferedReader.readLine().trim());`
     Similarly, reads another line, trims it, and converts it to an `int` representing the tax percentage.

   - **Call Solve Method:**
     `Result.solve(meal_cost, tip_percent, tax_percent);`
     Calls the `solve` method from the `Result` class with the read values to calculate and print the total cost.

   - **Close BufferedReader:**
     `bufferedReader.close();`
     Closes the `BufferedReader` to free up resources.

### Summary
This program reads three inputs (meal cost, tip percent, and tax percent), calculates the total cost including the tip and tax, 
rounds the total to the nearest whole number, and prints it. The main logic resides in the `solve` method of the `Result` class, 
which performs the calculations and rounding. The `main` method handles input reading and invokes the `solve` method.
