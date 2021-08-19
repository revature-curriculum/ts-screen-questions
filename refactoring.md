---
tags: refactoring
---

```java
String[] strings = {"fourth","third","second","first"};
int x = 3;
while(x > 0) {
    System.out.println(strings[--x]);
}
```

Question 1: How would you change this code to make it work as expected?

```java
int[] nums = {3,6,1,9,7};
for (int x = 0; x < nums.length; x++) {
    System.out.println(nums[x]);
}
```

Question 2: How would you rewrite this with an enhanced for loop?

```java
public interface A {
    public void doStuff();
    public static int x = 2;
} 
public class B implements A {
    // ?
}
```

What must go inside of class B in this code?

Using the above snippet and your previous answer, what object-oriented principle(s) apply here?

```java
public int[] findMinAndMax() {
    int[] arr = {1,2,3,4,5};
    int min = arr[0];
    int max = arr[0];
    for (int i=1; i < arr.length; i++) {
        if (arr[i] < min) {
            min = arr[i];
        }
    }
    for (int j=1; j < arr.length; j++) {
        if (arr[j] > min) {
            max = arr[j];
        }
    }
    return new int[] {min, max};
}
```
How would you refactor this code to make it DRY?

```java
public class Ford {
    static final int WHEELS = 4;
    public Engine eng = new FordEngine();
    int numAirbags = 4;
    public void speedUp() {
        eng.faster();
    }
}
public class Toyota {
    static final int WHEELS = 4;
    public Engine eng = new ToyotaEngine();
    int numAirbags = 8;
    public void speedUp() {
        eng.faster();
        checkSeatbelts();
    }
}
```

How would you refactor this code to make it more abstract?

```java
public class EmailSender {
    public static void main(String[] args) {
        new EmailSender().validateAddressAndSend("foo@bar.com");
    }
    public String validateAddressAndSend(String email) {
        if (email.indexOf('@') == -1) {
            throw new InvalidEmailAddressException();
        }
        EmailAddress emailObj = new EmailAddress(email);
        emailObj.setMessageBody("Hi, nice to meet you!");
        emailObj.send();
    }
}
```

How would you refactor this code so that (a) we follow SRP, and (b) the user of this class can set the body of the message?

```java
public void printFileContents(String pathToFile) {
    String[] content = getFileContent(pathToFile); // FileNotFoundException could be thrown here
    System.out.println(content);
}
```

This code can throw a FileNotFoundException. How could you handle this so that the code continues to execute?
