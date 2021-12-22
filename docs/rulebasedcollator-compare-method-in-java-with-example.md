# Java 中的规则库比较()方法与示例

> 原文:[https://www . geesforgeks . org/rulesbasedcollator-compare-method-in-Java-with-example/](https://www.geeksforgeeks.org/rulebasedcollator-compare-method-in-java-with-example/)

**Java . text . rulesbasedcollator**类的 **compare()** 方法用于比较两个对象的强度，它会根据结果返回 0，正值和负值作为输出。

**语法:**

```
public int compare(Object o1, Object o2)
```

**参数**:该方法取**两个对象**，两者之间进行比较。
**返回值:**如果第一个对象等于、大于或小于另一个对象，那么它将分别返回零、正值和负值。
**异常:**如果其中一个参数为空，该方法抛出 *NullPointerException* 。

以下是说明**比较()**方法的示例:

**例 1:**

## Java 语言(一种计算机语言，尤用于创建网站)

```
// Java program to demonstrate
// compare() method

import java.text.*;
import java.util.*;
import java.io.*;

public class GFG {
    public static void main(String[] argv)
    {
        try {

            // Creating and initializing
            // RuleBasedCollator Object
            RuleBasedCollator col
                = new RuleBasedCollator("< a< b< c< d");

            // Creating an initializing
            // object for comparison
            Object obj1 = "ab";

            // Creating an initializing
            // Object for comparison
            Object obj2 = "Ab";

            // compare both object
            // using compare() method
            int i
                = col.compare((String)obj1,
                              (String)obj2);

            // display result
            if (i < 0)
                System.out.println("ab is less than Ab");
            else if (i > 0)
                System.out.println("ab is greater than Ab");
            else
                System.out.println("ab is equal to Ab");
        }

        catch (ParseException e) {

            System.out.println(e);
        }
        catch (NullPointerException e) {

            System.out.println(e);
        }
    }
}
```

**Output:** 

```
ab is less than Ab
```

**例 2:**

## Java 语言(一种计算机语言，尤用于创建网站)

```
// Java program to demonstrate
// compare() method

import java.text.*;
import java.util.*;
import java.io.*;

public class GFG {
    public static void main(String[] argv)
    {
        try {

            // Creating and initializing RuleBasedCollator Object
            RuleBasedCollator col
                = new RuleBasedCollator("< a< b< c< d");

            // Creating an initializing
            // object for comparison
            Object obj1 = null;

            // Creating an initializing
            // Object for comparison
            Object obj2 = "Ab";

            // compare both object
            // using compare() method
            int i
                = col.compare((String)obj1, (String)obj2);

            // display result
            if (i < 0)
                System.out.println("ab is less than Ab");
            else if (i > 0)
                System.out.println("ab is greater than Ab");
            else
                System.out.println("ab is equal to Ab");
        }

        catch (ParseException e) {

            System.out.println(e);
        }
        catch (NullPointerException e) {
            System.out.println("one of the object is null");
            System.out.println(e);
        }
    }
}
```

**Output:** 

```
one of the object is null
java.lang.NullPointerException
```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/text/rulesbasedcollator . html # compare-Java . lang . string-Java . lang . string-](https://docs.oracle.com/javase/9/docs/api/java/text/RuleBasedCollator.html#compare-java.lang.String-java.lang.String-)