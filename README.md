# Pace
leetcode count frequency 
for education purpose 
class Solution {
public:
    vector<int> intersect(vector<int>& nums1, vector<int>& nums2) {
        unordered_map<int, int> freq;
        vector<int> result;
        
        // Count frequency of elements in nums1
        for (int x : nums1) {
            freq[x]++;
        }
        
        // Check elements in nums2
        for (int x : nums2) {
            if (freq[x] > 0) {
                result.push_back(x);
                freq[x]--;
            }
        }
        
        return result;
    }
};
