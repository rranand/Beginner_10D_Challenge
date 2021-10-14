# Question 2

***Difficulty: Easy***

### Explaination:
You need to start loop from L to R while traversing extract all digits from the number and check for divisibility. If all digits are divisible then, print the number else move for next number.

### Time Complexity:
O(N)

### Code:
```
void solve(int L, int R) {
  while (L <= R) {
    int temp = L;
    bool f = 0;
    
    while (!f && temp > 0) {
      int x = temp%10;
      if (x>0) {
        if (L%x) {
          f = 1;
        }
      }
      temp/=10;
    }
    
    if (!f) {
      cout << L << ' ';
    }
    L++;
  }
  cout << endl;
}

```
