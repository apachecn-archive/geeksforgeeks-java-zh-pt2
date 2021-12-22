# Java 中的 StringReader 标记(int)方法，示例

> 原文:[https://www . geeksforgeeks . org/string reader-markint-method-in-Java-with-examples/](https://www.geeksforgeeks.org/stringreader-markint-method-in-java-with-examples/)

Java 中 **[StringReader](https://www.geeksforgeeks.org/java-io-stringreader-class-java/)** 类的 **mark()** 方法用于在调用 reset()后，将流标记为流读取将从其开始的检查点。StringReader 类的所有子类都不支持此方法。

**语法:**

```
public void mark(int readAheadLimit)
```

**参数:**该方法接受一个强制参数 **readAheadLimit** ，它是在保留标记的同时可以读取的字符数的限制。读取这么多字符后，尝试重置流可能会失败。

**返回值:**此方法不返回值。

**异常:**如果在不支持输入输出或 mark()方法时出现一些错误，此方法将引发 IOException。

下面的方法说明了 mark()方法的工作原理:

**程序 1:**

```
// Java program to demonstrate
// StringReader mark() method

import java.io.*;
import java.util.*;

class GFG {
    public static void main(String[] args)
    {

        try {
            String str = "GeeksForGeeks";

            // Create a StringReader instance
            StringReader reader
                = new StringReader(str);

            // Get the character
            // to be read from the stream
            int ch;

            // Read the first 10 characters
            // to this reader using read() method
            // This will put the str in the stream
            // till it is read by the reader
            for (int i = 0; i < 10; i++) {
                ch = reader.read();
                System.out.print((char)ch);
            }

            System.out.println();

            // mark the stream for
            // 5 characters using mark()
            reader.mark(5);

            // reset the stream position
            reader.reset();

            // Read the 5 characters from marked position
            // to this reader using read() method
            for (int i = 0; i < 5; i++) {
                ch = reader.read();
                System.out.print((char)ch);
            }
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

**输出:**

```
GeeksForGe
eks??

```

**程序二:**

```
// Java program to demonstrate
// StringReader mark() method

import java.io.*;
import java.util.*;

class GFG {
    public static void main(String[] args)
    {

        try {
            String str = "GeeksForGeeks";

            // Create a StringReader instance
            StringReader reader
                = new StringReader(str);

            // Get the character
            // to be read from the stream
            int ch;

            // Read the first 10 characters
            // to this reader using read() method
            // This will put the str in the stream
            // till it is read by the reader
            for (int i = 0; i < 10; i++) {
                ch = reader.read();
                System.out.print((char)ch);
            }

            System.out.println();

            // mark the stream for
            // 10 characters using mark()
            reader.mark(10);

            // reset the stream position
            reader.reset();

            // Read the 1 characters from marked position
            // to this reader using read() method
            for (int i = 0; i < 1; i++) {
                ch = reader.read();
                System.out.print((char)ch);
            }
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

**输出:**

```
GeeksForGe
e

```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/io/stringreader . html # mark-int-](https://docs.oracle.com/javase/9/docs/api/java/io/StringReader.html#mark-int-)