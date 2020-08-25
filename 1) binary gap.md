1) binary gap

https://app.codility.com/c/run/trainingYJY7NU-6E9/

C++

```c++
#include<vector>

int solution(int N) {
    // write your code in C++14 (g++ 6.2.0)
    vector<int> list;
    int max= 0;
    bool check = false;
    int count = 0;
    int a = 0;
    
    while(N!=0){
        a = N% 2;
        N = N/2;
        list.insert(list.begin(), a);
    }
    
    for(int i=0; i<list.size(); i++){
        if(list[i]==1){
            check = true;
        }
        if(check&&list[i]==0){
            count++;
        }
        if(check&&list[i]==1){
            if(max <= count) max= count;
            count=0;
        }
    }
    return max;
}
```

