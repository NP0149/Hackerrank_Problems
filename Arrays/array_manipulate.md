[Problem Link](https://www.hackerrank.com/challenges/crush/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=arrays)



```
 public static long arrayManipulation(int n, List<List<Integer>> li) {
        long arr[]=new long[n+1];
        for(List<Integer> al:li){
            int a=al.get(0);
            int b=al.get(1);
            int val=al.get(2);
            arr[a]+=val;
            if(b+1<arr.length)
            arr[b+1]-=val;
        }
        long max=Long.MIN_VALUE;
        long sum=0;
        for(int i=0;i<arr.length;i++){
            sum+=arr[i];
            max=Math.max(sum,max);
        }
        return max;
    }

}
```
