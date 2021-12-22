# Java 中的 ThaiBuddhistChronology getId()方法，示例

> 原文:[https://www . geeksforgeeks . org/thaibudhistechr-getid-method-in-Java-with-example/](https://www.geeksforgeeks.org/thaibuddhistchronology-getid-method-in-java-with-example/)

类的**Java . time . chrono . thaibudhisterography**的 **getId()** 方法用于检索 getId()方法被撤销的特定年表的标识状态。

**语法:**

```java
public String getId()
```

**参数:**此方法不接受任何参数作为参数。

**返回值:**该方法返回 getId()方法被撤销的特定年表的标识状态。

以下是说明 **getId()** 方法的例子:

**例 1:**

```java
// Java program to demonstrate
// getId() method

import java.util.*;
import java.io.*;
import java.time.*;
import java.time.chrono.*;

public class GFG {
    public static void main(String[] argv)
    {
        // creating and initializing
        // ThaiBuddhistDate Object
        ThaiBuddhistDate hidate
            = ThaiBuddhistDate.now();

        // getting ThaiBuddhistChronology
        // used in ThaiBuddhistDate
        ThaiBuddhistChronology crono
            = hidate.getChronology();

        // getting id of this Chronology
        // by using getId() method
        String id = crono.getId();

        // display the result
        System.out.println("id : " + id);
    }
}
```

**输出:**

```java
id : ThaiBuddhist

```

**例 2:**

```java
// Java program to demonstrate
// getId() method

import java.util.*;
import java.io.*;
import java.time.*;
import java.time.chrono.*;

public class GFG {
    public static void main(String[] argv)
    {
        // creating and initializing
        // ThaiBuddhistDate Object
        ThaiBuddhistDate hidate
            = ThaiBuddhistDate.now(
                Clock.systemDefaultZone());

        // getting ThaiBuddhistChronology
        // used in ThaiBuddhistDate
        ThaiBuddhistChronology crono
            = hidate.getChronology();

        // getting id of this Chronology
        // by using getId() method
        String id = crono.getId();

        // display the result
        System.out.println("id : " + id);
    }
}
```

**输出:**

```java
id : ThaiBuddhist

```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/time/chrono/thaibudhistorager . html # Getid–](https://docs.oracle.com/javase/9/docs/api/java/time/chrono/ThaiBuddhistChronology.html#getId--)