---
layout: default
---

# Array Sorting
[Home](./)

In this activity, we will demonstrate different kinds of sorting methods on you. 

1. We need 5 volunteers.
1. Each gets a number 1 - 5
1. Mix up

## Some Different Types of Sorts
In computer science, there are certain common strategies, or algorithms, for sorting a collection of values. 
 
### Bubble Sort
Compare the first two students. If the student on the right is smaller than the student on the left, they should swap places. Then compare the second and third students. If the student on the right is smaller than the student on the left, they should swap places. When you reach the end, start over at the beginning again. Continue in this way until you make it through the entire row of students without swapping anybody.
 
#### In pseudocode:
1. Create a variable called counter.
2. Set the counter to zero.
3. Go through the entire array.
4. If the value you are considering is greater than the value to its right:
    1. Swap them
    2. Add one to counter
5. Repeat steps 2 through 4 as long as counter is greater than zero.

### Selection Sort
Take the first student on the left and consider that person’s number the smallest number you have found so far. If the next person in line has a number that is smaller than that number, then make that person’s number your new smallest number and continue in this way until you reach the end of the line of students. Then, move the person with the smallest number all the way to the left. Then start over from the second person in line. Keep going, finding the smallest number each time, and making that person the rightmost person in the sorted line of students.
 
#### In pseudocode:
1. Find the smallest unsorted value in the array.
2. Swap that value with the first unsorted value in the array.
3. Repeat steps 1 and 2 while the number of unsorted items is greater than zero.

### Insertion Sort
Take the first student on the left and consider that person sorted. Next, take the next student and compare him to the first student in the sorted section. If he is greater than the first student, then place him to the right of the student in the sorted section. Otherwise, place him to the left of the student in the sorted section. Continue down the line, considering each student in turn and then moving from left to right along the students in the sorted section until you find the proper place for each student to go, shifting the other students to the right to make room.
 
#### In pseudocode:
1. For each element in the unsorted section of the list, compare it against each element in the sorted section of the list until you find its proper place.
2. Shift the other elements in the sorted list to the right to make room.
3. Insert the element into its proper place in the sorted list.

## Now lets see each in block code for our micro:bit

## And these are just a few of the common sorting algorithms used
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZZuD6iUe3Pc" frameborder="0" allowfullscreen></iframe>