https://leetcode.com/problems/squares-of-a-sorted-array/submissions/


class Solution {
    public int[] sortedSquares(int[] a) {
                int n=a.length;
                int [] res = new int [n];
                int start = 0, end = n-1, j=n-1;//j is pointer form resultant array
                
                while(start <= end) {
                    if(a[start]*a[start] > a[end]*a[end] ) {
                        res[j--] = a[start]*a[start];
                        start++;
                    }
                    else {
                        res[j--] = a[end]*a[end];
                        end--;
                        
                    }
                }
                return res;
            }
}

tc-n
sc-n
