# 用示例打包 Java 中的 getAnnotations()方法

> 原文:[https://www . geesforgeks . org/package-getannocations-method-in-Java-with-examples/](https://www.geeksforgeeks.org/package-getannotations-method-in-java-with-examples/)

**java.lang.Package 类**的 **getAnnotations()** 方法用于获取该类中存在的注释。方法返回存在的注释数组。

**语法:**

```
public Annotation[] getAnnotations()

```

**参数:**该方法不接受任何参数。

**返回值:**该方法返回**一组存在的注释**。

下面的程序演示了 getAnnotations()方法。

**例 1:**

```
// Java program to demonstrate
// getAnnotations() method

import java.util.*;
import java.lang.annotation.*;

@Deprecated
public class Test {

    public Object obj;

    public static void main(String[] args)
        throws ClassNotFoundException
    {
        try {
            // returns the Class object for this class
            Class myClass = Test.class;

            System.out.println(
                "Class represented by myClass: "
                + myClass.toString());

            // Get the annotation
            // using getAnnotations() method
            System.out.println(
                "Annotation of myClass: "
                + Arrays.toString(
                      myClass.getAnnotations()));
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

**输出:**

```
Class represented by myClass: class Test
Annotation of myClass: [@java.lang.Deprecated()]

```

**例 2:**

```
// Java program to demonstrate
// getAnnotations() method

import java.util.*;
import java.lang.annotation.*;

// create a custom Annotation
@Retention(RetentionPolicy.RUNTIME)
@interface Annotation {

    // This annotation has two attributes.
    public String key();

    public String value();
}

// call Annotation for method
// and pass values for annotation
@Annotation(key = "GFG", value = "GeeksForGeeks")
public class Test {

    public Object obj;

    public static void main(String[] args)
        throws ClassNotFoundException
    {

        // returns the Class object for this class
        Class myClass = Test.class;

        System.out.println(
            "Class represented by myClass: "
            + myClass.toString());

        // Get the annotation
        // using getAnnotations() method
        System.out.println(
            "Annotation of myClass: "
            + Arrays.toString(
                  myClass.getAnnotations()));
    }
}
```

**输出:**

```
Class represented by myClass: class Test
Annotation of myClass: [@Annotation(key=GFG, value=GeeksForGeeks)]

```

**参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/lang/package . html # getAnnotations–](https://docs.oracle.com/javase/9/docs/api/java/lang/Package.html#getAnnotations--)