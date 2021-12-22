# 用示例将 getDeclaredAnnotationsByType()方法打包到 Java 中

> 原文:[https://www . geesforgeks . org/package-getdeclaredannotationbytype-method-in-Java-with-examples/](https://www.geeksforgeeks.org/package-getdeclaredannotationsbytype-method-in-java-with-examples/)

**java.lang.Package 类**的**getdeclaredannotationbytype()**方法用于获取该类中存在的指定声明注释类型的声明注释。方法返回指定声明注释类型的声明注释数组。

**语法:**

```
public A[] getDeclaredAnnotationsByType(Class<T> declared annotationClass)

```

**参数:**该方法接受一个参数**声明的注释类**，它是要获取的声明注释的类型。

**返回值:**这个方法为指定的声明注释类型返回一个声明注释的数组**。**

****异常:**此方法抛出:**

*   ****NullPointRexception:**如果给定的声明注释类为空。**

**下面的程序演示了 getDeclaredAnnotationsByType()方法。**

****例 1:****

```
// Java program to demonstrate
// getDeclaredAnnotationsByType() method

import java.util.*;
import java.lang.annotation.*;

// create a custom DeclaredAnnotation
@Retention(RetentionPolicy.RUNTIME)
@interface DeclaredAnnotation {

    // This declared annotation has two attributes.
    public String key();

    public String value();
}

// call DeclaredAnnotation for method
// and pass values for declared annotation
@DeclaredAnnotation(key = "GFG", value = "GeeksForGeeks")
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

        // Get the declared annotation
        // using getDeclaredAnnotationsByType() method
        System.out.println(
            "DeclaredAnnotation of myClass"
            + " of type DeclaredAnnotation: "
            + Arrays.toString(
                  myClass
                      .getDeclaredAnnotationsByType(
                          DeclaredAnnotation.class)));
    }
}
```

****输出:****

> **由 myClass 表示的类:class Test
> DeclaredAnnotation 类型的 myClass 的 DeclaredAnnotation:[@ DeclaredAnnotation(key = GFG，value=GeeksForGeeks)]**

****例 2:****

```
// Java program to demonstrate
// getDeclaredAnnotationsByType() method

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

            // Get the declared annotation
            // using getDeclaredAnnotationsByType() method
            System.out.println(
                "DeclaredAnnotation of myClass"
                + " of type Deprecated: "
                + Arrays.toString(
                      myClass
                          .getDeclaredAnnotationsByType(
                              Deprecated.class)));
        }
        catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

****输出:****

> **由 myClass 表示的类:class Test
> DeclaredAnnotation 类型的 myClass 已弃用:[@java.lang.Deprecated()]**

****参考:**[https://docs . Oracle . com/javase/9/docs/API/Java/lang/package . html # getdeclaredannotationbytype-Java . lang . class-](https://docs.oracle.com/javase/9/docs/api/java/lang/Package.html#getDeclaredAnnotationsByType-java.lang.Class-)**