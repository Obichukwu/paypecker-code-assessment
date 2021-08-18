# Gloopro-Technical-Tests

## Question 1

A jail has a number of prisoners and a number of treats to pass out to them. Their jailer decides the fairest way to divide the treats is to seat the prisoners around a circular table in sequentially numbered chairs. A chair number will be drawn from a hat. Beginning with the prisoner in that chair, one candy will be handed to each prisoner sequentially around the table until all have been distributed.

The jailer is playing a little joke, though. The last piece of candy looks like all the others, but it tastes awful. Determine the chair number occupied by the prisoner who will receive that candy.

For example, there are **4** prisoners and **6** pieces of candy. The prisoners arrange themselves in seats numbered **1** to **4** . Let's suppose two is drawn from the hat. Prisoners receive candy at positions **2, 3, 4, 1, 2, 3** . The prisoner to be warned sits in chair number **3**.

### Function Description

Complete the **_saveThePrisoner_** function in the file provided. It should return an integer representing the chair number of the prisoner to warn.

saveThePrisoner has the following parameter(s):

* n: an integer, the number of prisoners
* m: an integer, the number of sweets
* s: an integer, the chair number to begin passing out sweets from


The **_saveThePrisoner_** function should return the chair number of the prisoner who receives the awful treat.

#### Sample Input 1
```
n = 5 
m = 2 
s = 1    
````
#### Sample Output 1
```
2  
```
#### Explanation 1

In this query, there are **n = 5** prisoners and **m = 2** sweets. Distribution starts at seat number **s = 1** . Prisoners in seats numbered **1** and **2**  get sweets. Warn prisoner **2**. 

#### Sample Input 2
```
n = 7
m = 19 
s = 2 
```  
#### Sample Output 2
```  
6
```
#### Explanation 2

In this query, there are **n = 7**  prisoners, **m = 19** sweets and they are passed out starting at chair **s = 2**. The candies go all around twice and there are **5**  more candies passed to each prisoner from seat **2** to seat **6**.

  # Question 2
You are given ***N*** sticks, where the length of each stick is a positive integer. A *cut operation* is performed on the sticks such that all of them are reduced by the length of the smallest stick.

Suppose we have six sticks of the following lengths

```
5 4 4 2 2 8
```

Then, in one *cut operation* we make a cut of length 2 from each of the six sticks. For the next *cut
operation* four sticks are left (of non-zero length), whose lengths are the following:

```
3 2 2 6
```

The above step is repeated until no sticks are left. 

Given the length of ***N*** sticks, return an array containing the number of sticks that are left before each subsequent *cut operations*.

Note: For each *cut operation*, you have to recalcuate the length of smallest sticks (excluding zero-length sticks).

## Function Description
Complete the `cutTheSticks` function in the question2.js or question2.php file depending on which language you prefer. 

It must return an array containing the number of sticks that are left before each subsequent *cut operation*

`cutTheSticks` has the following parameter:

* *arr* : an array of integers containing the initial lengths of the sticks

### Sample Input 1
```
arr = [5, 4, 4, 2, 2, 8]
```
### Sample Output 1
```
[6, 4, 2, 1]
```
### Explanation 1
```
sticks-length        length-of-cut   sticks-cut
5 4 4 2 2 8             2               6
3 2 2 _ _ 6             2               4
1 _ _ _ _ 4             1               2
_ _ _ _ _ 3             3               1
_ _ _ _ _ _           DONE            DONE
```

### Sample Input 2
```
arr = [1, 2,3, 4, 3, 3, 2, 1]
```
### Sample Output 2
```
[8, 6, 4, 1]
```
### Explanation 2
```
sticks-length         length-of-cut   sticks-cut
1 2 3 4 3 3 2 1         1               8
_ 1 2 3 2 2 1 _         1               6
_ _ 1 2 1 1 _ _         1               4
_ _ _ 1 _ _ _ _         1               1
_ _ _ _ _ _ _ _       DONE            DONE
```

