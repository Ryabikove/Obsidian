Sorting algorithm which uses "Devide and Conquer" strategy:
1. Devide - splits the list in half until every list has only one element inside
2. Conquer - list of one is, by definition, already sorted
3. Combine - merge lists together in the correct order

```
static void mergeSort(int[] arr) {  
       if (arr.length < 2) return;  
       
       int mid = arr.length / 2;  
       int[] left = new int[mid];  
       int[] right = new int[arr.length - mid];  
  
       System.arraycopy(arr, 0, left, 0, mid);  
       System.arraycopy(arr, mid, right, 0, arr.length - mid);  
  
       mergeSort(left);  
       mergeSort(right);  
  
       merge(left, right, arr);  
  
  
    }  
  
    static void merge(int[] left, int[] right, int[] arr) {  
       int i = 0, j = 0, k = 0;  
  
       while (i < left.length && j < right.length) {  
          if (left[i] <= right[j]) {  
             arr[k++] = left[i++];  
          } else {  
             arr[k++] = right[j++];  
          }  
       }  
  
       while (i < left.length) {  
          arr[k++] = left[i++];  
       }  
  
       while (j < right.length) {  
          arr[k++] = right[j++];  
       }  
    }
```

*Speed* - [[Java/operations/Big O notation|O(N*log N)]] always.
*Memory* - O(N) always.