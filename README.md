# 153.-Find-Minimum-in-Rotated-Sorted-Array-
class Solution {
public:
    int findMin(vector<int>& nums) {
        
        int start=0;
        int end=nums.size()-1;
        while(start<=end){
            int mid=(start+end)/2;
            
            if(nums[start]>nums[end]){
                if(nums[mid]<=nums[end])
                end=mid-1;
                if(nums[start]<=nums[mid])
                start=mid+1;
            }
            else
            return nums[start];
            
            if(nums[start]>=nums[mid] && nums[mid]<=nums[end])
            return nums[mid];
        }
        return 0;
    }
};
