[Problem Link](https://www.hackerrank.com/challenges/ctci-array-left-rotation/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=arrays)



```
static void reverse(List<Integer> li,int a,int b){
    int i=a;
    int j=b;
    while(i<j){
        int temp=li.get(i);
        li.set(i,li.get(j));
        li.set(j,temp);
        i++;
        j--;
    }
  }
    public static List<Integer> rotLeft(List<Integer> a, int d) {
    // Write your code here
    d=d%a.size();
    int n=a.size();
     reverse(a,0,n-1);
     reverse(a,0,n-d-1);
     reverse(a,n-d,n-1);
     return a;

    }

}
```
