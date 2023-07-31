# Proplem-Solving-Challenge
Course-Task - Problem-Solving-Challenge

# question(1)
You are given an array of arrays a. Your task is to group the arrays a[i] by their mean values, so that arrays with equal mean values are in the same group, and arrays with different mean values are in different groups.

Each group should contain a set of indices (i, j, etc), such that the corresponding arrays (a[i], a[j], etc) all have the same mean. Return the set of groups as an array of arrays, where the indices within each group are sorted in ascending order, and the groups are sorted in ascending order of their minimum element.

----------------
# My Answer(1)
      function groupArray(Arrays) { 
      function calculateMeans(array) { 
      let sum = 0; 
      for(let i = 0; i < array.length; i++) { 
        sum += array[i]; 
      } 
     return sum / array.length  
      } 
 
    let emptyArray = []; 
    for(let i = 0; i < Arrays.length ; i++) { 
      emptyArray.push(calculateMeans(Arrays[i])) 
    } 
    console.log(emptyArray) 
    } 
    groupArray([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

--------------------------------------------------------------------------------------------------------------------------------------------
# question(2)
Let's say a triple (a, b, c) is a zigzag if either a < b > c or a > b < c.

Given an array of integers numbers, your task is to check all the triples of its consecutive elements for being a zigzag. More formally, your task is to construct an array of length numbers.length - 2, where the ith element of the output array equals 1 if the triple (numbers[i], numbers[i + 1], numbers[i + 2]) is a zigzag, and 0 otherwise.

Example

For numbers = [1, 2, 1, 3, 4], the output should be solution(numbers) = [1, 1, 0].

(numbers[0], numbers[1], numbers[2]) = (1,

---------------
# My Answer(2)
      let zigArr = []; 
      function calcZigzag(zigFun) { 
      for (let i = 0 ; i < zigFun.length - 2; i++) { 
      let a = zigFun[i] 
      let b = zigFun[i + 1] 
      let c = zigFun[i + 2] 
      console.log(`i am a ${a}`) 
      console.log(`i am b ${b}`) 
      console.log(`i am c ${c}`) 
      if(a < b && b > c || a > b && b < c) { 
        zigArr.push(1) 
      } else { 
        zigArr.push(0) 
      } 
    } 
    return zigArr 
} 
console.log(calcZigzag([2,3,1,4,5,0])) //first compare the index 0 and 1 and 2 after finsh put the value is 0 or 1 in array zigArr after finsh this step go to compare the index 1 , 2 , 3  and put the value is 0 or 1 in empty array zigArr after finsh that go to compare the index 2 , 3 , 4 and put the vlaue is 0 or 1 in empty array zigArr after finsh go to compare the index 3 , 4 , 5 and put the value is 0 or 1 in empty array zigArr



