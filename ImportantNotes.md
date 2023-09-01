* What is the meaning of: n=n&(n-1)
SIGNIFICANCE:
Whenever you perform the above operation the fact that the number of steps it will take for n to become zero will be equal to the number of setbits in n.
n -> is the number
n-1 -> saying let's find a new number by subtracting a bit from n
n=n&(n-1) -> let's eleminate the subtracted bit from n
Special cases: if n&n-1 run once becomes zero => in one step that means there is only one set bit in n => n isi also a pwoer of two.
Analysis:
We can eliminate one '1' by executing "n = n & (n - 1);" each time. To make it clear, we break it down to two cases: A) The last bit is 1, and B) the last bit is 0.
A) For any unsigned binary integer n = XXX...1, n = n & (n - 1) = XXX...1 & XXX...0 = XXX...0, the last 1 is eliminated;
B) n = XXX100...0: n & (n - 1) = XXX100...0 & XXX011...1 = XXX000...0, so that the last 1 followed by suffixal zeros is eliminated.
Repeating this process, all '1' are erased eventually, therefore the time of calling this statement is the number of '1's.


* Two integers x and y are coprime if there is no integer greater than 1 that divides both of them. In other words, x and y are coprime if gcd(x, y) == 1, where gcd(x, y) is the greatest common divisor of x and y.

* When we have to sort some values and return their original indexes or want the original indexes to be attacehd to array.
MI : Use pairs
MII : Use matrix array
```
int monsters[][] = new int[n][2]; // health of monsters //n->rows ; 2->columns(health, index)
for (int i = 0; i < monsters.length; i++) {
  monsters[i][0] = sc.nextInt(); //storing health
  monsters[i][1] = i + 1; //we make it one indexed
}
for (int i = 0; i < monsters.length; i++) {
  if (monsters[i][0] % k == 0) monsters[i][0] = k; //Since, we want to sort the array and keep the ones killed first in order
                                            //we need to bring them back to k to count them as greatest in health arr
  else monsters[i][0] %= k;
}
Arrays.sort(monsters, (a, b) -> b[0] - a[0]);
for (int i = 0; i < monsters.length; i++) {
  System.out.print(monsters[i][1] + " ");
}
```
Code example B. Monsters codeforces - Educational Codeforces Round 152 (Rated for Div. 2)
  

* Calculating first and last digit of a number.
  
  ```while(n>9){first=n/10;}```

  ```last=n%10;```


* HashSet to array
```String[] array = set.toArray(new String[0]);```

* Convert a specific char of string to integer
  
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



* **Multiple of 3** - If sum of digits is ina multiple of 3 then number is multiple of 3.
  Note : In case we are given a binary string - it is odd if the difference between the count of odd set bits and even set bits is divisible by 3.
  ```
  for(int i=s.length()-1;i>=0;i--){
            if(s.charAt(i)=='1' && i%2==0) even++;  //found bitset at even posiiton
            if(s.charAt(i)=='1' && i%2!=0) odd++;   //found bitset at odd position
        }
        if(Math.abs(even-odd)%3==0) return true;
  ```
  Note - The above problem can be solved using DFA.

* The sums of the elements in both groups have the same parity (either both groups have an even sum or both groups have an odd sum).

  
* Left Rotation of Array
  ```
  public class Main{
    public static void main(String args[]){
        int A[] = {5, 9, 6, 10, 12, 7, 3, 5, 4, 2};
        for(int x:A)
            System.out.print(x + ",");
        System.out.println("");
        int temp = A[0];
        for(int i=1; i<A.length; i++){
            A[i-1] = A[i];
        }
        A[A.length-1] = temp;
        for(int x:A)
            System.out.print(x+",");
        System.out.println("");
    }
}
```
In case of right rotation we simply travel backward in array.




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
 
