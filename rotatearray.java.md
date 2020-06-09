https://leetcode.com/problems/rotate-array/submissions/


class Solution {
    public void swap(int n[],int i,int j){
        while(i<j){
            int t=n[i];
            n[i]=n[j];
            n[j]=t;
            ++i;
            --j;
        }
    }
    public void rotate(int[] nums, int k) {
        k=k%nums.length;
        if(k==0) //array size and rotations are equal
        return;
        if(k<=nums.length){
          swap(nums,0,nums.length-1);
          swap(nums,0,k-1);
          swap(nums,k,nums.length-1);
        }  
        
    }
}

tc-n+n
sc-1
