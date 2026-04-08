# Power Sum

## Question:

Power Sum - Let’s define a peculiar type of array in which each element is either an integer or another peculiar array. Assume that a peculiar array is never empty. Write a function that will take a peculiar array as its input and find the sum of its elements. If an array is an element in the peculiar array you have to convert it to it’s equivalent value so that you can sum it with the other elements. Equivalent value of an array is the sum of its elements raised to the number which represents how far nested it is. For e.g. [2,3[4,1,2]] = 2+3+ (4+1+2)^2

another example - [1,2,[7,[3,4],2]] = 1 + 2 +( 7+(3+4)^3+2)^2

## Solution
Time Complexity: $O(N)$, N = total no. of elements in array and sub-array

Space Complexity: $O(k)$, k = depth of call stack, or maximum level nested list in array.

```python3
def power_sum(array,power=1):
    #write code here
    sums = 0
    for element in array:
        if type(element) == list:
            sums += power_sum(element, power + 1)
        else:
            sums += element
        
    return sums**power
  

```
