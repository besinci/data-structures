# Arrays

### What is an Array?

The collection of items could be integers, strings, etc. The items are stored in **contiguous** memory locations. Imagine as boxes **stick together** in RAM.

![min-array-image.jpg](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2e31838a-2135-42f3-8d87-7d4a2e98bb1c/min-array-image.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220213%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220213T083802Z&X-Amz-Expires=86400&X-Amz-Signature=80e3570fdd1b8b3229354501a91b48323cae7acc0e2f63de557de0e93cfc7f59&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22min-array-image.jpg%22&x-id=GetObject)

### Writing to an Array

```csharp
var arr = new string[7]; // initialize a new array with 7 capacity.
arr[3] = "Ali"; // add a string item into array to index of 3.
arr[6] = "Besinci"; // add a string item into array, index of 6.

// the result of the array would be like:
[null, null, null, "Ali", null, null, "Besinci", null]

// If you want to add new item into the index already filled. 
// It would just override the item.
arr[3] = "Veli";
[null, null, null, "Veli", null, null, "Besinci", null]
```

### Reading from an Array

C# initialize empty array slots to **null** if the array contains an object or to default values. If it contains primitive types for example int it would contain the default values of the int which is 0, If it contains float default value would be 0.0 and the boolean value would contain false.

As shown in the below array indexes start counting from **zero(0)**.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/17d9e655-328f-4948-b756-097c3b9c203a/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220213%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220213T084532Z&X-Amz-Expires=86400&X-Amz-Signature=86ab274174925a8822343524adff61dd01536c42587ff15474fe637bc2f7fc75&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

### Array Capacity vs Length

If we have an array initialize with 10 numbers, like: 

```csharp
var arr = new int[10]; // this 10 is the **capacity**
// and if we set only 3 items to this array.
arr[3] = 2;
arr[5] = 53;
arr[7] = 95;
// **length** of this array is 3.
```

- Reading    → O(1)   — constant time
- Searching → O(N) — linear time
- Insertion   → O(N) — linear time
- Deletion    → O(N) — linear time

> PS: You need to set the type of array you want to create. You cannot change array type after creation or you cannot add a string item inside of integer array.
— **Ordered Arrays:** If your array is ordered you can use different approaches from searching inside. You can use **Binary Search** instead of **Linear Search**.
>