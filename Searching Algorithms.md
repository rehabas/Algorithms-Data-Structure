# Searching Algorithms

Searching is the process of finding some particular element in the list. If the element is present in the list, then the process is called successful and the process returns the location of that element, otherwise the search is called unsuccessful.

There are two popular search methods that are widely used in order to search some item into the list. However, choice of the algorithm depends upon the arrangement of the list.

#### 1. Linear Search
#### 2. Binary Search

## Linear Search

Linear search is the simplest search algorithm and often called sequential search. In this type of searching, we simply traverse the list completely and match each element of the list with the item whose location is to be found.

Linear search is mostly used to search an unordered list in which the items are not sorted.

#### Problem: 

Given an array ```arr``` of ```n``` elements, write a function to search a given element ```x``` in ```arr```.

#### How it works?

1. Start from the leftmost element of ```arr``` and one by one compare ```x``` with each element of ```arr```.
2. If ```x``` matches with an element, return the ```index```.
3. If ```x``` doesn’t match with any of elements, return ```-1```.

![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/Linear-Search.png)

#### Pseudo Code

```
for i = 0 to n
   if current element == target
      return index
   return -1
```

#### Analysis

##### Worst Case:
- Search for last element
- **O(n)**

##### Best Case:
- Search for first element
- **O(1)**

#### Implementation

```js
const linearSearch = (arr, num) => {
     for (let i = 0; i < arr.length; i++) {
        if (arr[i] === num) return i;
     }
     return -1;
  }
 
  linearSearch([2,3,4,6], 4);  // 2
 
  linearSearch([2,3,4,6], 8);  // -1
```

## Binary Search

Binary search is the search technique which works efficiently on the sorted lists. Hence, in order to search an element into some list by using binary search technique, we must ensure that the list is sorted.

Binary search follows **divide and conquer** approach in which, the list is divided into two halves and the item is compared with the middle element of the list. If the match is found then, the location of middle element is returned otherwise, we search into either of the halves depending upon the result produced through the match.

#### How it works?

1. Compare ```x``` with the middle element.
2. If ```x``` matches with middle element, we return the ```mid index```.
3. Else If ```x``` is greater than the ```mid``` element, then ```x``` can only lie in right half subarray after the ```mid``` element. So we recur for right half.
4. Else (```x``` is smaller) recur for the left half.

![](https://www.codenuclear.com/wp-content/uploads/2017/07/Binary_Search.jpg)

#### Pseudo Code

```
go to middle
   if middle == target
      return index
   if middle > target
      search in left side
   if middle < target
      search in right side
```

#### Analysis

##### Worst Case:
- Search for first or last element
- **O(log(n))**

##### Best Case:
- Search for the middle element
- **O(1)**

#### Implementation

```js
const binarySearch = (arr, num) => {
     let start = 0;
     let end = arr.length - 1;
     let middle;
     while (end >= start) {
         middle = start + (end - start) / 2;
         if (arr[middle] === num) return middle;
         else if (arr[middle] > num) end = middle - 1;
         else start = middle + 1;
     }
     return -1
  }
 
  binarySearch([1,5,20,35,50,65,70], 50); // 4
 
  binarySearch([1,5,20,35,50,65,70], 16); // -1

``` 



