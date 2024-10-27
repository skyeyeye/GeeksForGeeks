/*question link:https://www.geeksforgeeks.org/problems/triplet-family/1*/
//{ Driver Code Starts
#include <bits/stdc++.h>
using namespace std;


// } Driver Code Ends
class Solution {
  public:
    bool findTriplet(vector<int>& arr) {
        // Your code
        sort(arr.begin(), arr.end(), greater<int>());
        for(int i = 0; i < arr.size();i++){
            int target = arr[i];
            int start = i+1;
            int end = arr.size()-1;
            while(start<end){
                if(arr[start] + arr[end] == target){
                    return true;
                }
                if(arr[start]+arr[end] > target){
                    start++;
                }
                else{
                    end--;
                }
            }
        }
        return false;
    }
};

