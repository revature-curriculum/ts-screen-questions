---
tags: debugging
---

```java
public class Program {
    private int main(String[] args) {
        Program p = new Program("foo");
        p.hello();
    }

    public void hello(String s) {
        System.out.println(s);
    }
}
```

Identify and fix all the problems you can see in this code snippet so that the program will print "foo"


```java
char a = "hello"
for (i < 5; i = 0; i++) {
    if (a.charAt(i) == 'e') {
        System.out.println(i);
    }
}
```

Correct any mistakes in the code
