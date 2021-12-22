# Java 中的 Reader markSupported()方法，示例

> 原文:[https://www . geesforgeks . org/reader-marksupported-method-in-Java-with-examples/](https://www.geeksforgeeks.org/reader-marksupported-method-in-java-with-examples/)

Java 中 **[Reader](https://www.geeksforgeeks.org/java-io-reader-class-java/)** 类的 **markSupported()** 方法用来检查这个 Reader 是否支持 mark()操作。它返回一个布尔值，该值表示读取器是否被标记为受支持。

**语法:**

```
public boolean markSupported()
```

**参数:**该方法不接受任何参数

**返回值:**这个方法返回一个**布尔值**，这个值告诉这个阅读器是否支持 mark()操作。如果它是 markSupported，则返回 true。否则返回假。

下面的方法说明了 markSupported()方法的工作原理:

**程序 1:**

```
// Java program to demonstrate
// Reader markSupported() method

import java.io.*;
import java.util.*;

class GFG {
    public static void main(String[] args)
    {

        try {

            String str = "GeeksForGeeks";

            // Create a Reader instance
            Reader reader
                = new StringReader(str);

            // Check if the Reader is
            // markSupported using markSupported()
            System.out.println("Is Reader markSupported: "
                               + reader.markSupported());

            reader.close();
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

**输出:**

```
Is Reader markSupported: true

```

**程序二:**

```
// Java program to demonstrate
// Reader markSupported() method

import java.io.*;
import java.util.*;

class GFG {
    public static void main(String[] args)
    {

        try {
            char[] str = { 'G', 'E', 'E', 'K', 'S' };

            // Create a Reader instance
            Reader reader
                = new CharArrayReader(str);

            // Check if the Reader is
            // markSupported using markSupported()
            System.out.println("Is Reader markSupported: "
                               + reader.markSupported());

            reader.close();
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

**输出:**

```
Is Reader markSupported: true

```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/io/reader . html # markSupported–](https://docs.oracle.com/javase/9/docs/api/java/io/Reader.html#markSupported--)