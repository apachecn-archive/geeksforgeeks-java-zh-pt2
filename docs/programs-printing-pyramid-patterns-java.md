# 用 Java 打印金字塔图案的程序

> 原文:[https://www . geesforgeks . org/programs-printing-金字塔-patterns-java/](https://www.geeksforgeeks.org/programs-printing-pyramid-patterns-java/)

本文旨在给出一个模式打印的 Java 实现。

*   **Simple pyramid pattern**

## Java

```
import java.io.*;

// Java code to demonstrate star patterns
public class GeeksForGeeks
{
    // Function to demonstrate printing pattern
    public static void printStars(int n)
    {
        int i, j;

        // outer loop to handle number of rows
        //  n in this case
        for(i=0; i<n; i++)
        {

            //  inner loop to handle number of columns
            //  values changing acc. to outer loop   
            for(j=0; j<=i; j++)
            {
                // printing stars
                System.out.print("* ");
            }

            // ending line after each row
            System.out.println();
        }
   }

    // Driver Function
    public static void main(String args[])
    {
        int n = 5;
        printStars(n);
    }
}
```

**输出**

```
* 
* * 
* * * 
* * * * 
* * * * * 

```

*   **After 180-degree rotation**

## Java

```
import java.io.*;

// Java code to demonstrate star pattern
public class GeeksForGeeks
{
    // Function to demonstrate printing pattern
    public static void printStars(int n)
    {
        int i, j;

        // outer loop to handle number of rows
        //  n in this case
        for(i=0; i<n; i++)
        {

            // inner loop to handle number spaces
            // values changing acc. to requirement
            for(j=2*(n-i); j>=0; j--)
            {
                // printing spaces
                System.out.print(" ");
            }

            //  inner loop to handle number of columns
            //  values changing acc. to outer loop
            for(j=0; j<=i; j++)
            {
                // printing stars
                System.out.print("* ");
            }

            // ending line after each row
            System.out.println();
        }
    }

    // Driver Function
    public static void main(String args[])
    {
        int n = 5;
        printStars(n);
    }
}
```

**输出**

```
           * 
         * * 
       * * * 
     * * * * 
   * * * * * 

```

*   ```
        * 
       * * 
      * * * 
     * * * * 
    * * * * * 

    ```