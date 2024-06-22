# singleelement
single element in array
class Solution {
public:
    int singleNumber(vector<int>& nums) {
        int n = nums.size();
        map<int,int>check;
        for(int i=0;i<n;i++){
            check[nums[i]]++;
        }
        for(int i=0;i<n;i++){
            if(check[nums[i]] == 1){
               return nums[i];
            }
        }
        return -1;
    }
};
