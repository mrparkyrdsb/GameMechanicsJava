# How to create named code blocks with Methods

_Current Problem:_ It is too messy to have a large set of code, I want to divide up my code into their own components.

__SOLUTION:__ We can create method. Methods will be formally defined in a future grade.

## Creating a Method

__Code Example:__

```java
class Main {
    static void otherMethod() {
        System.out.println("I exist too, but you don't see me because you did not call my name.");
    }
    
    static void myMethod() {
        System.out.println("I am my own independent code!");
    }

    public static void main(String[] args) {
        myMethod();
    }
}
```

__NOTES:__
- The ```main()``` is usually where we always store our code.
- We can now create code outside of it as long as we follow the rules of methods
- Our custom code called ```myMethod()``` currently outputs: ```I am my own independent code!``` only if its name is called within the ```main()```

### What is ```static void```?

This will be explained in Grade 11! _We will change up void to other keywords soon!_

## Why do we need this?

If you were to create a story-based choose your own adventure game ... it will be very beneficial to have different part of the stories within its own methods rather than all within the main.

__Code Example:__
```java
import java.util.Scanner;
class Main {
    static void beach() {
        System.out.println("You are exploring the beach.");
    }
    
    static void forest() {
        System.out.println("You are exploring the forest.");
    }

    public static void main(String[] args) {
        Scanner reader = new Scanner(System.in);

        System.out.println("Hello, you washed up on shore on a random beach...");
        System.out.println("After orienting yourself, you notice there is also a forest.");
        System.out.println("Which will you explore? (Forest/Beach)");
        String choice1 = reader.nextLine();

        if (choice1.equals("Forest")) {
            forest();
        } else if (choice1.equals("Beach")) {
            beach();
        } else {
            System.out.println("Hmm... that is not an option.");
        }
    }
}
```

__NOTES:__
- In the code above, the main game is coded in our ```main()```
- However, anytime we make a decision, we can jump into a method to complete story line there
- This allows us to have a cleaner conditional statements in our code