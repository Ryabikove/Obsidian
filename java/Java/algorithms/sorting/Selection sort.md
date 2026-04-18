Sorting algorithm which has next steps:
- Starts from the begining;
- Find smallest element and put it first;
- Go to start and ignore previous element;
- Repeate until all elements become sorted.

```
for (int i = 0; i < arr.length; i++) {  
	int min = arr[i];  
    for (int j = i+1; j < arr.length; j++) {  
	    if  (arr[j] < min) {  
	        min = arr[j];  
        }  
    }  
    result[i] = min;  
}
```

*Speed* - [[Java/operations/Big O notation|O(N**2)]] always. 
*Memory* - O(1) always.