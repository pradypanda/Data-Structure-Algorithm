# Data-Structure-Algorithm
### RECURSION
- Function calling another function
- Function are excuted in the **STACK** memory
```
public class NumberExample {
    public static void main(String args[])
    {
        print1(1);

    }

    static void print1(int n)
    {
        System.out.println(n);
        print2(2);
    }

    static void print2(int n)
    {
        System.out.println(n);
        print3(3);
    }

    static void print3(int n)
    {
        System.out.println(n);
        print4(4);
    }

    static void print4(int n)
    {
        System.out.println(n);
        print5(5);
    }
    
    static void print5(int n)
    {
        System.out.println(n);
    }
}

```
- How function call works internally?
- NOTE:
    1. While the function is not finished executing it will remain in **STACK**
    2. When a function finishes its execution it is **removed from stack** and the **flow of program is restored to program where the function was called.**
    3. Main function is the last function that is removed from **STACK** and the first one to enter into **STACK** memory
        ![image](https://user-images.githubusercontent.com/61123137/169643698-1dc8b384-2d37-4e2d-a47b-16d1afe78072.png)
        
 - Same action is present in the body:
   1. Taking a number
   2. Printing a number 
   3. calling another function

- If all these function have the same body and are doing the same thing then why are we creating this function again and again?

  Solution: call the function itself
  
- Parmameter is calling **n+1** and when the value of n is 5 it is not calling anything
- Recurssion is a function that call itself

```
public class NumberExample {
    public static void main(String args[])
    {
        // write a function that takes in a number and print it
        // print first  5 numbers: 1 2 3 4 5
        print(1);

    }

    static void print(int n)
    {
        if(n ==5)
        {
            System.out.println(5);
            return;
        }
        System.out.println(n);
        print(n+1);
    }
}
```

- Base Condition in Recursion:
   It is a Condition where our recurssion will stop making new calls. 
   
### Recursive call
- If you are calling a function again and again, you can treat it as a seperate call in the stack
- If there are no Base Condition --> Function calls will keep happening --> stack will be filled again and again --> We know that every function call consumes memory
  --> at a given moment **Memory of computer will exceed the limit**, resulting into stackoverflow error
  
### Why do we need Recursion?
- It helps us in soving bigger/complex problem in a simple way.
- you can convert recursion solution into iteration & vice versa
    eg: First solve the problem statement using recursion and then convert it into iteration to get an optimized solution
- Space complexity is not constant because of recursive call
- It helps us in breaking down bigger problems into smaller problems

### Visualizing Recursion   VVVVI
![image](https://user-images.githubusercontent.com/61123137/169655835-0d6a6a77-7477-4deb-bc46-5f572f8dc933.png)

- This is called as **Recursion Treee**





  


