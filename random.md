# How to generate Random Numbers in Java

Randomness is a fun way to unique interactions in  your code.

## Step 1: ```import java.util.Random```

There is a [class](https://www.w3schools.com/java/java_classes.asp) that we can import that allows us to access java's way of generating randomness.

__Code Example:__

```java
import java.util.Random; // Random Class Imported

class Main {
    public static void main(String[] args) {
        System.out.println("Hello world!");
    }
}
```

## Step 2: Create a random instance (object variable) --> ```Random rand = new Random()```

Much similar to how __[Scanners](https://www.w3schools.com/java/java_user_input.asp)__ are used, we must create a random variable. You don't have to call it ```rand```; feel free to  call it whatever. This random variable is going to help us use __[methods](https://www.w3schools.com/java/java_methods.asp)__ belonging to the _random class_.

__Code Example__:

```java
import java.util.Random; // Random Class Imported

class Main {
    public static void main(String[] args) {
        //System.out.println("Hello world!");
        Random rand = new Random();
    }
}
```

## Step 3: Generating Random Integers

There are ways to generate random decimals from 0.0 to 1.0, but I personally find that working with integers much easier.

__The method:__ ```rand.nextInt(upperbound)```
- ```rand``` is the random object instance we created prior
- ```.nextInt()``` generates a random number from 0 (inclusively) up towards an upperbound (exclusively).
- ```upperbound``` should be a positive integer, it helps to generate an integer from ```[0, upperbound)```

__Code Example:__

```java
import java.util.Random; // Random Class Imported

class Main {
    public static void main(String[] args) {
        //System.out.println("Hello world!");
        Random rand = new Random();

        int rand_number = rand.nextInt(100) // Generates a random number from 0 to 99 inclusively both ends.
    }
}
```