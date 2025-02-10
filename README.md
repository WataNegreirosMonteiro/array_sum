# array_sum
Solution to array values in a matrix

```py
[
[1, 2, 3],
[1, 2, 3],
[1, 2, 3],
]
```

The algorithm must return: 0
Cause: | matrix([0][0], [0][1], [0][2]) - matrix([0][2], [0][1], [0][0]) | = 0


```py
def matrix(arr):
    sums = [0,0]
    for index, array in enumerate(arr):
        array_size = len(array)-1
        sums[0] += array[index]
        sums[1] += array[array_size-index]

    return abs(sums[0] - sums[1])

print(matrix([[1,2,3], [1,2,3], [1,2,3]]))
```
