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



# Conversions
* char to int => ```Character.getNumericValue(c)```
    
* int to char
```
int a=1;    
char c=(char)(a+'0');  //o/p: 1 => this will be character type
```
```
int num1 = 1;
int num2 = 13;
char a = Character.forDigit(num1, 10);
char b = Character.forDigit(num2, 16);
System.out.println(a);    // 1
System.out.println(b);    // d
```

#### Precision
  ```
  //M I
  DecimalFormat df = new DecimalFormat("#.##");
  double piValue = 3.14159265359;
  System.out.println(df.format(piValue));  //o/p: 3.14    //this method will not add 0 if the decimal point is given greater in ###
  ```
  ```
  //M II
  Formatter f = new Formatter();
  f.format("%1.9f", 29292929.98765432);
  System.out.println(f);  //292929.987654320    //this method will also add 0 to decimal if the fromatter demands more decimal
  ```
  ```
  //MIII
  System.out.println(String.format("%1.3f", 2929.987654));  //2929.987
  ```
 
