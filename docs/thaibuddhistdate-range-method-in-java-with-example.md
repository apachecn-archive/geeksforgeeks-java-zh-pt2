# Java 中的 ThaiBuddhistDate range()方法，示例

> 原文:[https://www . geeksforgeeks . org/thaibudhistdata-range-method-in-Java-with-example/](https://www.geeksforgeeks.org/thaibuddhistdate-range-method-in-java-with-example/)

**Java . time . chrono . thaibudhistate**类的 **range()** 方法用于从 TemporalField 类型的指定字段中获取的范围。

**语法:**

```
public ValueRange range(TemporalField field)

```

**参数**:该方法将临时场类型的**场**作为要获取其范围的参数。

**返回值:**该方法以 ValueRange 的形式返回指定字段的**范围**。

以下是说明**范围()**方法的示例:

**例 1:**

## Java 语言(一种计算机语言，尤用于创建网站)

```
// Java program to demonstrate
// range() method

import java.util.*;
import java.io.*;
import java.time.*;
import java.time.chrono.*;
import java.time.temporal.*;

public class GFG {
    public static void main(String[] argv)
    {
        try {
            // Creating and initializing
            // ThaiBuddhistDate Object
            ThaiBuddhistDate hidate
                = ThaiBuddhistDate.now();

            // Getting the ValueRange for
            // given ChronoField
            // by using range() method
            ValueRange range
                = hidate.range(ChronoField.ERA);

            // display the result
            System.out.println("Equivalent Range : "
                               + range);
        }
        catch (DateTimeException e) {
            System.out.println("passed parameter can"
                               + " not form a date");
            System.out.println("Exception thrown: " + e);
        }
    }
}
```

**Output:**

```
Equivalent Range : 0 - 1

```

**例 2:**

## Java 语言(一种计算机语言，尤用于创建网站)

```
// Java program to demonstrate
// range() method

import java.util.*;
import java.io.*;
import java.time.*;
import java.time.chrono.*;
import java.time.temporal.*;

public class GFG {
    public static void main(String[] argv)
    {
        try {
            // Creating and initializing
            // ThaiBuddhistDate Object
            ThaiBuddhistDate hidate
                = ThaiBuddhistDate.now();

            // Getting the ValueRange for
            // given ChronoField
            // by using range() method
            ValueRange range
                = hidate.range(ChronoField.YEAR);

            // display the result
            System.out.println("Equivalent Range : "
                               + range);
        }
        catch (DateTimeException e) {
            System.out.println("passed parameter can"
                               + " not form a date");
            System.out.println("Exception thrown: " + e);
        }
    }
}
```

**Output:**

```
Equivalent Range : -999999456 - 1000000542

```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/time/chrono/thaibudhistorager . html # range-Java . time . temporal . chronofield-](https://docs.oracle.com/javase/9/docs/api/java/time/chrono/ThaiBuddhistChronology.html#range-java.time.temporal.ChronoField-)