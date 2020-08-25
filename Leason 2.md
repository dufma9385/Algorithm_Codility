Leason 2

1) CyclicRotation

```C++
vector<int> solution(vector<int> &A, int K) {
    // write your code in C++14 (g++ 6.2.0)
    int endN = 0;
    if(A.empty()){
        return A;
    }else{
        for(int i =0; i< K; i++){
            endN = A.back();
            A.insert(A.begin(), endN);
            A.pop_back();
        }
        return A;
    }
    
    
    // return A;
}
```

