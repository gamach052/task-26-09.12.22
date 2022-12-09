###  [Task 7 kyu](https://www.codewars.com/kata/57f609022f4d534f05000024/train/java)
You are given an odd-length array of integers, in which all of them are the same, except for one single number.

Complete the method which accepts such an array, and returns that single different number.

The input array will always be valid! (odd-length >= 3)


### My solution
```Java
class Solution {
    static int stray(int[] numbers) {
        if (numbers[0] != numbers[1] && numbers[0] != numbers[2]) return numbers[0];
        for (int i : numbers) if (i != numbers[0]) return i;
        return 0;
    }
}

```

### Fav solution
```Java
class Solution {
    static int stray(int[] numbers) {
        return java.util.stream.IntStream.of(numbers).reduce(0, (a, b) -> a ^ b);
    }
}
```
I like this solution because I like it
