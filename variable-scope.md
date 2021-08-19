---
tags: variable scopes
---

```java
public class Test {
    int x;
    public Test() {
        // A
    }
    public int doStuff() {
        int y;
        // B
        for (int i = 0; i < 10; i++) {
            int z = 3;
            // C
        }
    }
    public String doOtherStuff() {
        // D
    }
}
```

Question 1: From which sections of the code above (A, B, C, D) can the variable `x` be accessed? 

Question 2: From which sections of the code above (A, B, C, D) can the variable `y` be accessed? 

Question 3: From which sections of the code above (A, B, C, D) can the variable `z` be accessed? 