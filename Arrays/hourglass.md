[Problem Link](https://www.geeksforgeeks.org/problems/maximum-sum-of-hour-glass3842/1)


```
class Solution {
    public int maxHourglass(int[][] arr) {
        // code here
        if(arr.length<3 || arr[0].length<3){
            return -1;
        }
        int maxsum=Integer.MIN_VALUE;
        for(int i=0;i<arr.length-2;i++){
            for(int j=0;j<arr[0].length-2;j++){
                int sum=arr[i][j]+arr[i][j+1]+arr[i][j+2];
                 sum+=arr[i+1][j+1];
                 sum+=arr[i+2][j]+arr[i+2][j+1]+arr[i+2][j+2];
                 
                 maxsum=Math.max(maxsum,sum);
            }
        }
        return maxsum;
    }
}
```
