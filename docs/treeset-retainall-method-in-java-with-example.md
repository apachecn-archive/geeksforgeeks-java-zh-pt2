# Java 中的 TreeSet retainAll()方法，示例

> 原文:[https://www . geesforgeks . org/treeset-retain all-method-in-Java-with-example/](https://www.geeksforgeeks.org/treeset-retainall-method-in-java-with-example/)

**java.util.TreeSet** 类的**retainnal()**方法用于从该集合中保留指定集合中包含的所有元素。

**语法:**

```
public boolean retainAll(Collection c)
```

**参数:**该方法以**集合 c** 为参数，包含从该集合中保留的元素。

**返回值:**如果该设置因调用而改变，则该方法返回**真**。

**异常:**如果该集合包含空元素，并且指定的集合不允许空元素(可选)，或者指定的集合为空，则该方法抛出**空指针异常**。

以下是说明*retainal()*方法的例子。

**例 1:**

```
// Java program to demonstrate
// retainAll() method for Integer value

import java.util.*;

public class GFG1 {
    public static void main(String[] argv) throws Exception
    {

        try {

            // Creating object of TreeSet<Integer>
            TreeSet<Integer>
                set1 = new TreeSet<Integer>();

            // Populating set1
            set1.add(1);
            set1.add(2);
            set1.add(3);
            set1.add(4);
            set1.add(5);

            // print set1
            System.out.println("TreeSet before "
                               + "retainAll() operation : "
                               + set1);

            // Creating another object of  TreeSet<Integer>
            TreeSet<Integer>
                set2 = new TreeSet<Integer>();
            set2.add(1);
            set2.add(2);
            set2.add(3);

            // print set2
            System.out.println("Collection Elements"
                               + " to be retained : "
                               + set2);

            // Removing elements from set
            // specified in set2
            // using retainAll() method
            set1.retainAll(set2);

            // print set1
            System.out.println("TreeSet after "
                               + "retainAll() operation : "
                               + set1);
        }

        catch (NullPointerException e) {
            System.out.println("Exception thrown : " + e);
        }
    }
}
```

**Output:**

```
TreeSet before retainAll() operation : [1, 2, 3, 4, 5]
Collection Elements to be retained : [1, 2, 3]
TreeSet after retainAll() operation : [1, 2, 3]

```

**示例 2:** 适用于*空指针异常*

```
// Java program to demonstrate
// retainAll() method for Integer value

import java.util.*;

public class GFG1 {
    public static void main(String[] argv) throws Exception
    {

        try {

            // Creating object of TreeSet<Integer>
            TreeSet<Integer>
                set1 = new TreeSet<Integer>();

            // Populating set1
            set1.add(1);
            set1.add(2);
            set1.add(3);
            set1.add(4);
            set1.add(5);

            // print set1
            System.out.println("TreeSet before "
                               + "retainAll() operation : "
                               + set1);

            // Creating another object of  TreeSet<Integer>
            TreeSet<Integer>
                set2 = null;

            // print set2
            System.out.println("Collection Elements"
                               + " to be retained : "
                               + set2);

            System.out.println("\nTrying to pass "
                               + "null as a specified element\n");

            // Removing elements from set
            // specified in set2
            // using retainAll() method
            set1.retainAll(set2);

            // print set1
            System.out.println("TreeSet after "
                               + "retainAll() operation : "
                               + set1);
        }

        catch (NullPointerException e) {
            System.out.println("Exception thrown : " + e);
        }
    }
}
```

**Output:**

```
TreeSet before retainAll() operation : [1, 2, 3, 4, 5]
Collection Elements to be retained : null

Trying to pass null as a specified element

Exception thrown : java.lang.NullPointerException

```