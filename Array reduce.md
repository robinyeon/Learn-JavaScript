## `.reduce()`
- The `.reduce()` method is used to calculate a single value from an array.
- ***`.reduce()` method reduces an array into a single value.***

### `.reduce(reducer, initialValue)`
- Takes 2 parameters: `reducer` and `initialValue`.
  - The `initialValue` is always 0 for sum, 1 for multiplicaiton.
- The `reducer` is a callback funciton that receives 2 parameters: `total` and `current`.
  - The `total` (also called accumulator) keeps track of the result of the reduce method. For example, when calculating the sum, it keeps track of the sum, step by styp.
  - The `current` represents one item of the array.
  - The `reducer` is called for every item in the array.
<img src="https://user-images.githubusercontent.com/85475577/142443122-3b3e72fa-43f3-4c11-b86d-91ab1fc69713.jpeg" width="700px"/>
  
