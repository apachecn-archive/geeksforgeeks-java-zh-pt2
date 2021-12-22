# Java 中的 Reader read(CharBuffer)方法，示例

> 原文:[https://www . geeksforgeeks . org/reader-readcharbuffer-method-in-Java-with-examples/](https://www.geeksforgeeks.org/reader-readcharbuffer-method-in-java-with-examples/)

Java 中 **[Reader](https://www.geeksforgeeks.org/java-io-reader-class-java/)** 类的 **read(CharBuffer)** 方法用于将指定的字符读入 CharBuffer 实例。这个方法阻塞流直到:

*   It takes some input from the stream.
*   Some IOException occurred.
*   It has reached the end of the stream when reading.

**语法:**

```java
public int read(CharBuffer charBuffer)
```

**参数:**这个方法接受一个强制参数 **charBuffer** ，它是要写入流中的 charBuffer 实例。

**返回值:**该方法返回一个**整数值**，即从流中读取的字符数。如果未读取任何字符，则返回-1。

**异常:**如果输入输出时出现错误，该方法抛出以下异常:

*   **Exception:** .
*   **空指针异常:**你好载入缓冲区是陈列夫吗
*   **readonlybufferexception:** If the CharBuffer instance to be filled is a read-only buffer

下面的方法说明了 read(CharBuffer)方法的工作原理:

**程序 1:**

```java
// Java program to demonstrate
// Reader read(CharBuffer) method

import java.io.*;
import java.util.*;
import java.nio.CharBuffer;

class GFG {
    public static void main(String[] args)
    {

        try {

            String str = "GeeksForGeeks";

            // Create a Reader instance
            Reader reader
                = new StringReader(str);

            // Get the CharBuffer instance
            // to be read from the stream
            CharBuffer charBuffer
                = CharBuffer.allocate(5);

            // Read the charBuffer
            // to this reader using read() method
            // This will put the str in the stream
            // till it is read by the reader
            reader.read(charBuffer);

            // Print the read charBuffer
            System.out.println(charBuffer
                                   .flip()
                                   .toString());

            reader.close();
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

**输出:**

```java
Geeks

```

**程序二:**

```java
// Java program to demonstrate
// Reader read(CharBuffer) method

import java.io.*;
import java.util.*;
import java.nio.CharBuffer;

class GFG {
    public static void main(String[] args)
    {

        try {

            String str = "GeeksForGeeks";

            // Create a Reader instance
            Reader reader
                = new StringReader(str);

            // Get the CharBuffer instance
            // to be read from the stream
            CharBuffer charBuffer
                = CharBuffer
                      .allocate(
                          str.length());

            // Read the charBuffer
            // to this reader using read() method
            // This will put the str in the stream
            // till it is read by the reader
            reader.read(charBuffer);

            // Print the read charBuffer
            System.out.println(charBuffer
                                   .flip()
                                   .toString());

            reader.close();
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

**输出:**

```java
GeeksForGeeks

```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/io/reader . html # read-Java . nio . charbuffer-](https://docs.oracle.com/javase/9/docs/api/java/io/Reader.html#read-java.nio.CharBuffer-)