https://leetcode.com/explore/challenge/card/june-leetcoding-challenge/540/week-2-june-8th-june-14th/3357/

https://www.youtube.com/watch?v=sEQk8xgjx64
https://www.youtube.com/watch?v=BOt1DAvR0zI


class Solution {
    public void swap(int n[],int a,int b){
        int t=n[a];
        n[a]=n[b];
        n[b]=t;
    }
    public void sortColors(int[] nums) {
        int l=0;
        int m=0;
        int h=nums.length-1;
        while(m<=h){
            if(nums[m]==0){
                swap(nums,m,l);
                l++;
                m++;
            }
            else if(nums[m]==1)
                ++m;
            else{
                swap(nums,m,h);
                --h;
            }
        }
    }
}

tc-n //size of array
sc-1
