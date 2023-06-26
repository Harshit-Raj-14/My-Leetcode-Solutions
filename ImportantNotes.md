* Two integers x and y are coprime if there is no integer greater than 1 that divides both of them. In other words, x and y are coprime if gcd(x, y) == 1, where gcd(x, y) is the greatest common divisor of x and y.

* Calculating first and last digit of a number.
  
  ```while(n>9){first=n/10;}```

  ```last=n%10;```

  *Convert a specific char of string to integer
  
    ```int age = (details[i].charAt(11) - '0')*10 + (details[i].charAt(12) - '0');```
  ```
      public int toInt(String s){
        int n=0;
        for(int i=0;i<s.length();i++){
            n=n*10+(s.charAt(i)-'0');
        }
        return n;
    }
  ````




* How to know if a problem can be solved by a greedy method.?
If you are able to find a strategy; which gives the best choice at your current position and is also guaranteed to give the best answer for the future then you can do the greedy technique.
In Greedy problems; the trick is you find some way and then you successfully try to disprove it if you are not able to disprove it means your theory is correct.
 
