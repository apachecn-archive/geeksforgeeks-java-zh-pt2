# Java 中的 ThaiBuddhistChronology isLeapYear()方法，示例

> 原文:[https://www . geeksforgeeks . org/thaibudhistechr-islapyear-method-in-Java-with-example/](https://www.geeksforgeeks.org/thaibuddhistchronology-isleapyear-method-in-java-with-example/)

**Java . time . chrono . thaibudhistory**类的**IsLapyear()**方法用于区分闰年和非闰年。如果是闰年，它将返回真或假。

**语法:**

```java
public boolean isLeapYear(long prolepticYear)

```

**参数:**该方法以**普理年**为参数，检查是否为闰年。

**返回值:**如果前一年是闰年，该方法返回**布尔值**为真，否则为假。

以下是说明**方法的示例:**

**例 1:**

```java
// Java program to demonstrate
// isLeapYear() method

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
        // by using isLeapYear() method
        boolean flag = crono.isLeapYear(2016);

        // display the result
        if (flag)
            System.out.println(
                "this is leap year");
        else
            System.out.println(
                "this is non leap year");
    }
}
```

**输出:**

```java
this is non leap year

```

**例 2:**

```java
// Java program to demonstrate
// isLeapYear() method

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
        // by using isLeapYear() method
        boolean flag = crono.isLeapYear(2019);

        // display the result
        if (flag)
            System.out.println(
                "this is leap year");
        else
            System.out.println(
                "this is non leap year");
    }
}
```

**输出:**

```java
this is leap year

```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/time/chrono/thaibudhistorager . html # islapyear-long-](https://docs.oracle.com/javase/9/docs/api/java/time/chrono/ThaiBuddhistChronology.html#isLeapYear-long-)