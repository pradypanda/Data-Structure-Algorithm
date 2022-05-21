# Data-Structure-Algorithm
### RECURSION
- Function calling another function
- Function are excuted in the stack memory
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
    1. While the function is not finished executing it will remain in stack
    2. When a function finishes its execution it is **removed from stack** and the **flow of program is restored to program where the function was called.**
    3. Main function is the last function that is removed from stack
        ![image](https://user-images.githubusercontent.com/61123137/169643698-1dc8b384-2d37-4e2d-a47b-16d1afe78072.png)
        
 - Same action is present in the body:
   1. Taking a number
   2. Printing a number 
   3. calling another function

- If all these function have the same body and are doing the same thing then why are we creating this function again and again?

  Solution: call the function itself

  


