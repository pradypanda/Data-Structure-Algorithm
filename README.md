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
- we will be using the **Recursion Treee** concept to solve complex and visulaize comolex problems.



# String in JAVA

- 4 ways to define string in java:
### 1. Character Array/ArrayList
```
syntax:
char []arr = ['g','e','e','k','s'];
```

### 2. String Class
- It is Immutable class
```
syntax:
String str="geeks";

    OR
    
String str = new String("geeks");
```

### 3. StringBuffer class
- It is Mutable class
- It is thread safe
```
syntax:

StringBuffer str = new StringBuffer("geeks");
```
### 4. StringBuilder class
- It is Mutable class
- It is not thread safe
```
syntax:

StringBuilder str = new StringBuilder("geeks");
```

![image](https://user-images.githubusercontent.com/61123137/173683733-1c0d0f95-a590-472c-b837-c9f912baea9c.png)


![image](https://user-images.githubusercontent.com/61123137/173683895-062dced7-3907-4f12-b16e-a22e16d5524e.png)

- s1 == s1 --> It compare whether instance s1 & s2 belong to same memory aor not. for content comparison we have equal and compare method.
- contains()
![image](https://user-images.githubusercontent.com/61123137/173685140-fcae09b5-ee3a-45cf-8e62-57b1edbc67d7.png)

- equals()
![image](https://user-images.githubusercontent.com/61123137/173685416-8ea4b1d8-0370-4ab8-b0da-86772374a1c7.png)

- compareTo()
![image](https://user-images.githubusercontent.com/61123137/173685676-b7a8ea08-687e-4d9b-a195-d28d4970c9af.png)

- indexOf()
![image](https://user-images.githubusercontent.com/61123137/173686257-47cccebc-29fc-4a79-8d09-086169c757d7.png)






  


