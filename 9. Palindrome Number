//LEETCODE PROBLEM
//LEVEL - EASY
//9. Palindrome Number

/* JAVA */

class Solution {
    public boolean isPalindrome(int x) 
    {
        int temp = x;
        int r = 0;
        
        while(temp>0)
        {
        r= 10*r+temp%10;
        temp=temp/10;
        }
       
        if(x==r)
            return true;
        else
            return false;
    }
}
