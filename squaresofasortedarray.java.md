https://leetcode.com/problems/squares-of-a-sorted-array/submissions/


class Solution {
    public int[] sortedSquares(int[] A) {
        int a=0; //pointing to start of given array
        int b=A.length-1; //pointing to end of given array
        int x[]=new int[A.length];
        int k=b; //pointing to end of resultant aray
        while(a<=b){
            if((A[a]*A[a])>(A[b]*A[b])){
                x[k--]=A[a]*A[a];
                ++a;
            }
            else{
                x[k--]=A[b]*A[b];
                --b;
            }
        }
        return x;
    }
}

tc-n  //to traverse the array using two pointers
sc-n  
