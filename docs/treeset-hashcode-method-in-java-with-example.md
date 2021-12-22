# Java 中的 TreeSet hashCode()方法，示例

> 原文:[https://www . geesforgeks . org/treeset-hashcode-method-in-Java-with-example/](https://www.geeksforgeeks.org/treeset-hashcode-method-in-java-with-example/)

Java 中 **TreeSet** 的 **hashCode()** 方法用于获取 TreeSet 这个实例的 hashCode 值。它返回一个整数值，该整数值是该树集实例的哈希值。

**语法:**

```java
public int hashCode()
```

**参数:**该功能没有参数。

**返回:**该方法返回一个**整数值**，这是该树集实例的哈希值。

下面的例子说明了 TreeSet.hashCode()方法:

**例 1:**

```java
// Java code to demonstrate the working of
// hashCode() method in TreeSet

import java.util.*;

public class GFG {
    public static void main(String[] args)
    {
        // creating an TreeSet
        TreeSet<Integer> LHS
            = new TreeSet<Integer>();

        // using add() to initialize values
        // [1, 2, 3, 4]
        LHS.add(1);
        LHS.add(2);
        LHS.add(3);
        LHS.add(4);

        // print TreeSet
        System.out.println("TreeSet: "
                           + LHS);

        // Get the hashCode value
        // using hashCode() value
        System.out.println("HashCode value: "
                           + LHS.hashCode());
    }
}
```

**Output:**

```java
TreeSet: [1, 2, 3, 4]
HashCode value: 10

```

**例 2:**

```java
// Java code to demonstrate the working of
// hashCode() method in TreeSet

import java.util.*;

public class GFG {
    public static void main(String[] args)
    {
        // creating an TreeSet
        TreeSet<String> LHS
            = new TreeSet<String>();

        // using add() to initialize values
        // [Geeks, For, ForGeeks, GeeksForGeeks]
        LHS.add("Geeks");
        LHS.add("For");
        LHS.add("ForGeeks");
        LHS.add("GeeksForGeeks");

        // print TreeSet
        System.out.println("TreeSet: "
                           + LHS);

        // Get the hashCode value
        // using hashCode() value
        System.out.println("HashCode value: "
                           + LHS.hashCode());
    }
}
```

**Output:**

```java
TreeSet: [For, ForGeeks, Geeks, GeeksForGeeks]
HashCode value: -482506029

```