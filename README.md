Download Link : https://programming.engineering/product/the-if-statement-comparing-strings-and-flags/

# The-if-Statement-Comparing-Strings-and-Flags
The if Statement, Comparing Strings, and Flags
Lab Objectives

    Be able to construct boolean expressions to evaluate a given condition

    Be able to compare String objects

    Be able to use a flag

    Be able to construct if and if–else–if statements to perform a specific task

    Be able to construct a switch statement

    Be able to format output

Introduction

Up to this point, all the programs you have written had a sequence structure. This means that all statements are executed in sequence, one after another. Sometimes we need to let the computer make decisions, based on the data. A decision structure allows the computer to decide which statement to execute.

In order to have the computer make a decision, it needs to do a comparison. So we will work with writing boolean expressions. boolean expressions use relational operators and logical operators to create a condition that can be evaluated as true or false.

Once we have a condition, we can conditionally execute statements. This means that there are statements in the program that may or may not be executed, depending on the condition.

We can also chain conditional statements together to allow the computer to choose from several courses of action. We will explore this using nested if–else statements as well as a switch statement.

In this lab, we will be editing a pizza ordering program. It creates a pizza ordered to the specifications that the user desires. It walks the user through ordering, giving the user choices, which the program then uses to decide how to make the pizza and how much the cost of the pizza will be. The user will also receive a $2.00 discount if his or her name is Mike or Diane.

Task #1 The if Statement, Comparing Strings, and Flags

    Copy the file PizzaOrder.java (see Code Listing 3.1) from the Student CD or as directed by your instructor.

    Compile and run PizzaOrder.java. You will be able to make selections, but at this point, you will always get a Hand-tossed pizza at a base cost of $12.99 no matter what you select, but you will be able to choose toppings, and they should

Copyright © 2016 Pearson Education, Inc., Hoboken NJ

add into the price correctly. You will also notice that the output does not look like money. So we need to edit PizzaOrder.java to complete the program so that it works correctly.

    Construct a simple if statement. The condition will compare the String input by the user as his or her first name with the first names of the owners, Mike and Diane. Be sure that the comparison is not case sensitive.

    If the user has either first name, set the discount flag to true. This will not affect the price at this point yet.

Task #2 The if–else–if Statement

    Write an if–else–if statement that lets the computer choose which statements to execute by the user input size (10, 12, 14, or 16). For each option, the cost needs to be set to the appropriate amount.

    The default else of the above if–else–if statement should print a statement that the user input was not one of the choices, so a 12 inch pizza will be made. It should also set the pizza size to 12 and the cost to 12.99.

    Compile, debug, and run. You should now be able to get correct output for the pizza size and price (it will still have Hand-tossed crust, the output won’t look like money, and no discount will be applied yet). Run your program multiple times ordering a 10, 12, 14, 16, and 17 inch pizza.

Task #3 The switch Statement

    Write a switch statement that compares the user’s choice with the appropriate characters (make sure that both capital letters and small letters will work).

    Each case will assign the appropriate string indicating crust type to the crust variable.

    The default case will print a statement that the user input was not one of the choices, so a Hand-tossed crust will be made.

    Compile, debug, and run. You should now be able to get crust types other than Hand-tossed. Run your program multiple times to make sure all cases of the switch statement operate correctly.

Task #4 Using a Flag as a Condition

    Write an if statement that uses the flag as the condition. Remember that the flag is a boolean variable, therefore is true or false. It does not have to be compared to anything.

    The body of the if statement should contain two statements:

        A statement that prints a message indicating that the user is eligible for a $2.00 discount.

        A statement that reduces the variable cost by 2.

Copyright © 2016 Pearson Education, Inc., Hoboken NJ

    Compile, debug, and run. Test your program using the owners’ names (both capitalized and not) as well as a different name. The discount should be displayed correctly at this time.

Task #5 Formatting Output

    Edit the appropriate lines in the main method so that any monetary output has 2 decimal places.

    Compile, debug, and run. Your output should be completely correct at this time, and numeric output should look like money.

Code Listing 3.1 (PizzaOrder.java)

import java.util.Scanner; // Needed for the Scanner class

/**

This program allows the user to order a pizza.

*/

public class PizzaOrder

{

public static void main (String[] args)

{

    Create a Scanner object to read input. Scanner keyboard = new Scanner (System.in);

String firstName; // User’s first name boolean discount = false; // Flag for discount int inches; // Size of the pizza char crustType; // For type of crust String crust = “Hand-tossed”; // Name of crust double cost = 12.99; // Cost of the pizza final double TAX_RATE = .08; // Sales tax rate double tax; // Amount of tax char choice; // User’s choice String input; // User input String toppings = “Cheese “; // List of toppings int numberOfToppings = 0; // Number of toppings

    Prompt user and get first name. System.out.println(“Welcome to Mike and ” +

“Diane’s Pizza”);

System.out.print(“Enter your first name: “);

firstName = keyboard.nextLine();

Copyright © 2016 Pearson Education, Inc., Hoboken NJ

    Determine if user is eligible for discount by

    having the same first name as one of the owners.

    ADD LINES HERE FOR TASK #1

    Prompt user and get pizza size choice.

            System.out.println(“Pizza Size (inches)
            	

            Cost”);

            System.out.println(“
            	

            10
            	

            $10.99″);

            System.out.println(“
            	

            12
            	

            $12.99″);

            System.out.println(“
            	

            14
            	

            $14.99″);

            System.out.println(“
            	

            16
            	

            $16.99″);

            System.out.println(“What size pizza ” +
            	

            “would you like?”);
            	

System.out.print(“10, 12, 14, or 16 ” + “(enter the number only): “);

inches = keyboard.nextInt();

    Set price and size of pizza ordered.

    ADD LINES HERE FOR TASK #2

    Consume the remaining newline character. keyboard.nextLine();

    Prompt user and get crust choice. System.out.println(“What type of crust ” +

“do you want? “);

System.out.print(“(H)Hand-tossed, ” +

“(T) Thin-crust, or ” +

“(D) Deep-dish ” +

“(enter H, T, or D): “);

input = keyboard.nextLine();

crustType = input.charAt(0);

    Set user’s crust choice on pizza ordered.

    ADD LINES FOR TASK #3

    Prompt user and get topping choices one at a time. System.out.println(“All pizzas come with cheese.”); System.out.println(“Additional toppings are ” +

“$1.25 each, choose from:”);

System.out.println(“Pepperoni, Sausage, ” + “Onion, Mushroom”);

Copyright © 2016 Pearson Education, Inc., Hoboken NJ

    If topping is desired,

    add to topping list and number of toppings System.out.print(“Do you want Pepperoni? (Y/N): “); input = keyboard.nextLine();

choice = input.charAt(0);

if (choice == ‘Y’ || choice == ‘y’)

{

numberOfToppings += 1;

toppings = toppings + “Pepperoni “;

}

System.out.print(“Do you want Sausage? (Y/N): “); input = keyboard.nextLine();

choice = input.charAt(0);

if (choice == ‘Y’ || choice == ‘y’)

{

numberOfToppings += 1;

toppings = toppings + “Sausage “;

}

System.out.print(“Do you want Onion? (Y/N): “); input = keyboard.nextLine();

choice = input.charAt(0);

if (choice == ‘Y’ || choice == ‘y’)

{

numberOfToppings += 1; toppings = toppings + “Onion “;

}

System.out.print(“Do you want Mushroom? (Y/N): “); input = keyboard.nextLine();

choice = input.charAt(0);

if (choice == ‘Y’ || choice == ‘y’)

{

numberOfToppings += 1;

toppings = toppings + “Mushroom “;

}

    Add additional toppings cost to cost of pizza. cost = cost + (1.25 * numberOfToppings);

    Display order confirmation. System.out.println(); System.out.println(“Your order is as follows: “); System.out.println(inches + ” inch pizza”); System.out.println(crust + ” crust”); System.out.println(toppings);

Copyright © 2016 Pearson Education, Inc., Hoboken NJ

    Apply discount if user is eligible.

    ADD LINES FOR TASK #4 HERE

    EDIT PROGRAM FOR TASK #5

    SO ALL MONEY OUTPUT APPEARS WITH 2 DECIMAL PLACES System.out.printf(“The cost of your order ” +

“is: $%f\n”, cost);

    Calculate and display tax and total cost. tax = cost * TAX_RATE; System.out.printf(“The tax is: $%f\n”, tax); System.out.printf(“The total due is: $%f\n”,

(tax + cost));

System.out.println(“Your order will be ready ” + “for pickup in 30 minutes.”);

}

}

Copyright © 2016 Pearson Education, Inc., Hoboken NJ
