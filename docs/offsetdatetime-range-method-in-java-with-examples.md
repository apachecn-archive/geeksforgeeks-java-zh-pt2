# Java 中的 OffsetDateTime range()方法，示例

> 原文:[https://www . geesforgeks . org/offsetdatetime-range-method-in-Java-with-examples/](https://www.geeksforgeeks.org/offsetdatetime-range-method-in-java-with-examples/)

**OffsetDateTime** 类的 **range()** 方法用于获取 ValueRange 对象，该对象是作为参数传递给该方法的字段的最小值和最大值的字段范围。该方法只为 OffsetDateTime 对象支持的那些字段返回 ValueRange 对象。因此，当该方法不支持该字段时，该方法将引发异常。

**语法:**

```
public ValueRange range(TemporalField field)

```

**参数:**该方法接受一个参数字段，即查询范围的字段。

**返回值:**此方法返回字段的有效值范围。

**异常:**该方法抛出以下异常:

*   **日期时间异常**–如果无法获得字段的范围。
*   **unsupportedtemporaltypexception**–如果不支持该字段。

以下程序举例说明了 range()方法:
**程序 1:**

```
// Java program to demonstrate
// OffsetDateTime.range() method

import java.time.*;
import java.time.temporal.*;

public class GFG {
    public static void main(String[] args)
    {
        // create OffsetDateTime objects
        OffsetDateTime offsetdateTime
            = OffsetDateTime
                  .parse(
                      "2018-12-12T13:30:30+05:00");

        // apply range() method of OffsetDateTime class
        ValueRange result
            = offsetdateTime.range(
                ChronoField.CLOCK_HOUR_OF_AMPM);

        // print results
        System.out.println("Range in CLOCK_HOUR_OF_AMPM: "
                           + result);
    }
}
```

**Output:**

```
Range in CLOCK_HOUR_OF_AMPM: 1 - 12

```

**程序 2:**

```
// Java program to demonstrate
// OffsetDateTime.range() method

import java.time.*;
import java.time.temporal.*;

public class GFG {
    public static void main(String[] args)
    {
        // create OffsetDateTime objects
        OffsetDateTime offsetdateTime
            = OffsetDateTime
                  .parse(
                      "2018-12-12T13:30:30+05:00");

        // apply range() method of OffsetDateTime class
        ValueRange result
            = offsetdateTime.range(
                ChronoField.SECOND_OF_DAY);

        // print results
        System.out.println("Range in SECOND_OF_DAY: "
                           + result);
    }
}
```

**Output:**

```
Range in SECOND_OF_DAY: 0 - 86399

```

**参考文献:**[https://docs . Oracle . com/javase/10/docs/API/Java/time/offsetdatetime . html # range(Java . time . temporal field)](https://docs.oracle.com/javase/10/docs/api/java/time/OffsetDateTime.html#range(java.time.temporal.TemporalField))