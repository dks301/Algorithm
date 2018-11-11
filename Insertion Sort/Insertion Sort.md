# Insertion Sort
![insertionSort1](https://github.com/dks301/Algorithm/images/insertionSort1.PNG)

* Insertion Sort란 위 이미지처럼 자료 배열의 모든 요소를 앞에서 부터 차례대로 비교하여 삽입함으로써 정렬을 완성하는 알고리즘이다.



**Pseudo Code**

```C
INSERTION-SORT(A, n)  ◁ A[1 .. n]
for j ← 2 to n
	key ← A[j]
	i ← j-1
    while i > 0 and A[i] > key
    	A[i+1] ← A[i]
    	i ← i-1
    A[i+1] = key
```


