### [Filter range "in place"](https://javascript.info/array-methods#filter-range-in-place)

[](https://javascript.info/task/filter-range-in-place)

importance: 4

Write a function `filterRangeInPlace(arr, a, b)` that gets an array `arr` and removes from it all values except those that are between `a` and `b`. The test is: `a ≤ arr[i] ≤ b`.

The function should only modify the array. It should not return anything.

For instance:

``` `let` arr `=` `[``5``,` `3``,` `8``,` `1``]``;`  `filterRangeInPlace``(`arr`,` `1``,` `4``)``;` `// removed the numbers except from 1 to 4`  `alert``(` arr `)``;` `// [3, 1]` ```

# Solution
```js
function filterRangeInPlace(arr,a,b) {
	for(let i = 0; i < arr.length ; i++) {
        if(arr[i] < a || arr[i] > b) {
            arr.splice(i,1);
            i--; //correct the index
        }
    }
}


let arr = [5, 9,3, 8, 1];
filterRangeInPlace(arr,1,4)
```