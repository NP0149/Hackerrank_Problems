[Problem Link](https://www.hackerrank.com/challenges/minimum-swaps-2/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=arrays)

# Minimum number of swaps needed to swap an array

## just take a temporary 2D array and then store the values and index in orginal array and then sort this temporay matrix and then take visited array

```
public class Solution {

    // Complete the minimumSwaps function below.
    static int minimumSwaps(int[] arr) {
 int temp[][]=new int[arr.length][2];
 for(int i=0;i<arr.length;i++){
    temp[i][0]=arr[i];
    temp[i][1]=i;
 }
 Arrays.sort(temp,(a,b)->Integer.compare(a[0],b[0]));
 int swaps=0;
 boolean visited[]=new boolean[arr.length];
 for(int i=0;i<temp.length;i++){
    if(visited[i] || temp[i][1]==i){
        continue;
    }
    int j=i;
    int cycle=0;
    while(!visited[j]){
        visited[j]=true;
        j=temp[j][1];
        cycle++;
    }
    swaps+=cycle-1;
 }
 return swaps;

    }

```
