# 使用 Java 中的 LinkedHashMap 按照出现的顺序打印字符及其频率

> 原文:[https://www . geeksforgeeks . org/print-characters-and-frequency-按出现顺序使用-linkedhashmap-in-java/](https://www.geeksforgeeks.org/print-characters-and-their-frequencies-in-order-of-occurrence-using-a-linkedhashmap-in-java/)

给定一个只包含小写字符的字符串**字符串**。任务是按照字符在给定字符串中出现的顺序打印字符及其频率。
**例:**

> **输入:**输入: str = "helloworld"
> **输出:** h1 e1 l3 o2 w1 r1 d1

**方法:**逐个字符遍历给定的字符串，并将所有字符串的频率存储在[链接哈希表](https://www.geeksforgeeks.org/linkedhashmap-class-java-examples/)中，该哈希表维护存储这些字符串的元素的顺序。现在，迭代 LinkedhashMap 的元素并打印内容。
以下是上述办法的实施情况:

## Java 语言(一种计算机语言，尤用于创建网站)

```
// Java implementation of the approach
import java.util.LinkedHashMap;

public class GFG {

    // Function to print the characters and their
    // frequencies in the order of their occurrence
    static void printCharWithFreq(String str, int n)
    {

        // LinkedHashMap preserves the order in
        // which the input is supplied
        LinkedHashMap<Character, Integer> lhm
            = new LinkedHashMap<Character, Integer>();

        // For every character of the input string
        for (int i = 0; i < n; i++) {

            // Using java 8 getorDefault method
            char c = str.charAt(i);
            lhm.put(c, lhm.getOrDefault(c, 0) + 1);
        }

        // Iterate using java 8 forEach method
        lhm.forEach(
            (k, v) -> System.out.print(k + " " + v));
    }

    // Driver code
    public static void main(String[] args)
    {
        String str = "geeksforgeeks";
        int n = str.length();

        printCharWithFreq(str, n);
    }
}
```

**Output:** 

```
g2 e4 k2 s2 f1 o1 r1
```