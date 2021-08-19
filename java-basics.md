
---
tags: basics
---

```java
protected static String findName(long id) {}
```

Match all the parts of this method signature
class scope declaration

access modifier

return type

method parameter

```java
public class Driver {
    public int x = 0;
    public static int y = 0;
    public static void main(String[] args) {
        Driver d1 = new Driver();
        Driver d2 = new Driver();
        d1.incrementStatic();
        d1.incrementNonStatic();
        d2.incrementStatic();
        d2.incrementNonStatic();
        System.out.println(d1.x); // A
        System.out.println(d2.x); // B
        System.out.println(y);    // C
    }
    public void incrementStatic() {
        y++;
    }
    public void incrementNonStatic() {
        x++;
    }
}
```

What are the outputs at lines A, B, C?

Which of these commands will compile a java source code file?

```
java Program.java   <-- A
javac Program.java  <-- B
java Program        <-- C
javac Program.class <-- D
```