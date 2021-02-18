# Insertion Sort

**For getting started with Insertion Sort refer to**

### [Insertion Sort](https://www.interviewbit.com/tutorial/insertion-sort-algorithm/)
### [Problem with Tut](https://www.hackerearth.com/practice/algorithms/sorting/insertion-sort/tutorial/)

**For further info. and understanding google it.**

**The basic Algorithm is as below**

```
INSERTION-SORT(A)
   for i = 1 to n
   	key ← A [i]
    	j ← i – 1
  	 while j > = 0 and A[j] > key
   		A[j+1] ← A[j]
   		j ← j – 1
   	End while 
   	A[j+1] ← key
   End for 
```

**Here we can see from the algorithm itself that we start from left and keep making each next term key element
And after that we check where the key fits into the previous sorted array to the left side of the key element
The left side is sorted and it goes on sorting as we move to the right side.**

**So, in the while loop we see that we are travelling toward left till the point where we see A[j]>key
where j is the index travelling for shifting the key value. key is stored differently so we don't have
to keep track of it. We keep on shifting other elements and when we get A[j] < key we just place the key
at right position.**

### CPP code.

```
//Let us assume we get array and it's size as input

void InsertionSort(int a[],int n){
    int i,j,key;
    for(i=1;i<n;i++){
        key=a[i];
        j=i-1;
        while(j>=0 && a[i]>key){
            a[j+1]=a[j];
            j=j-1;
        }
        a[j+1]=key;
    }
}

```

