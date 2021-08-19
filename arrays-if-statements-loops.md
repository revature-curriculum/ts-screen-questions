---
tags: arrays, if statements, for loops, continue & break statements
---

```java
int[] nums = {2,9,1,5,8,3,2};
int x = 0;
for (int i = 0; i < nums.length; i++) {
    if (nums[i] != 8) {
        continue;
    } else if (nums[i] == 8) {
        x = i;
        break;
    }
}
System.out.println(x);
```

Question 1: What will this code output?

