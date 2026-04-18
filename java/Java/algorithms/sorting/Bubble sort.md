Sorting algorithm which has next steps:
- Starts from the begining
- Compare two side-by-side numbers
- If one on the left  bigger than one on the right
	- swap them
- Repeate until the largest numbers "bubble" up to the end of the list

```
for (int i = 0; i < arr.length; i++) {  
    for (int j = 0; j < arr.length - i - 1; j++) {  
       if (arr[j] > arr[j + 1]) {  
          int temp = arr[j];  
          arr[j] = arr[j + 1];  
          arr[j + 1] = temp;  
       }  
    }  
}
```

*Speed* - [[Java/operations/Big O notation|O(N**2)]] for the worst case and [[Java/operations/Big O notation|O(N)]] for the best case. 
*Memory* - O(1) always.