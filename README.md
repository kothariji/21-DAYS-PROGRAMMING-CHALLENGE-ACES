
# 21-DAYS-PROGRAMMING-CHALLENGE-ACES
### CP is OP :heart:  Saying hi to DP! :fire::fire:
---
<br/>

# Dynamic Programming :rocket::rocket:

### Definition : :orange_book:
```
Simply cached Recursion (Memoization) or in other words enhanced recursion.
```
##### _The main idea behind DP is to store the results of subproblems so that we can simply use the results of these subproblems without re-computing them when needed in the future. This idealogy saves a lot of time and makes the solution optimized._
---
## Day - 1 :blue_book:
### Knapsack Problem: :pushpin::pushpin:
_In this problem we are given an empty bag with its maximum weight holding capacity. Also, we are given a list of items with there weight and profit values. We need to find out the maximum profit we can earn._
#### Type of Knapsack Problems
- ***Fractional Knapsack*** - It is simply a greedy problem. In this, we can take fraction values. ***for eg. if we have space of 3 kg. left in a knapsack and we have an item of 6 kg that values 50 rs. , then we can take 50% of that item and we will gain a profit of 25 rs.***

- ***0/1 Knapsack*** - It is a classical DP problem. Many beginner-level problems are a variation of this problem. In this, we have only had two choices, either we include the item in Knapsack or we don't.

- ***Unbounded Knapsack*** - It is similar to 0/1 Knapsack but in this, we can include the same item multiple numbers of times.


```diff
! solved a classical knapsack problem using only recursion.
```
#### It all started with Day-1 :fire::fire:
---

## Day - 2 :green_book:
### Memosisation: Top - Down Approach :pushpin::pushpin:
_It is an **optimization technique** used to cache the results of subproblems so that we can use that results later on if required. **Memoization** ensures that a method doesn't run for the inputs whose results are previously calculated._

The dimensions of the memoization array/table depend upon variables.
If in recursive function:

- 1 variable is changing on recursive call, we will create a linear vector/array. ***E.g.  Fibonacci series***
- 2 variables are changing on recursive call, then we will use a 2-D matrix to store the results of subproblems. ***E.g. Longest Common Subsequence***
- and so on.....for 3, 4..n variables.

#### _Generally we should initialize these matrices with -1 and later on we can check that if the value of a particular cell is not  -1 then we will directly return that particular cell value. else we will do a recursive call and set the cell value and finally return the cell value._

```diff
+ solved a classical knapsack problem using the memoization technique.
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 GEEKSFORGEEKS |[0 - 1 Knapsack Problem](https://practice.geeksforgeeks.org/problems/0-1-knapsack-problem/0) | [View Solution](./DAY-02/0-1_Knapsack_Problem_(GEEKSFORGEEKS).cpp) | Easy |||
<pre>
<b>Important Tip</b> -  std::vector's at() function is similar to subscript operator [ ].
But when the performance is measured at() function is 3.1 times faster then subscript operator [ ]. 
</pre>
<b> This costed me 29 submissions :persevere: :laughing:</b>


---
## Day - 3 :ledger:
### 1.  Tabulation:  Bottom-Up Approach :pushpin::pushpin:
_It is one of the most preferable methods in dynamic programming. It is faster than the **memoization** method as it doesn't involve any recursive calls. In this method, we have an array/matrix and we start from the first cell and move down filling entries in each cell one by one._
#### 2-Steps to create dp matrix. 
- ***Step-1 Initialisation*** - It is similar to the base condition which we do in a recursive function. ***for eg.***
 ```
 //in recursive function
	 if((index <0)|| (w <= 0))
			return 0;

//in bottom-up approach
	for(int i =0; i<=n; i++){
			for(int j= 0; j<=w; j++){
				if(i == 0 || j ==0)
				    dp[i][j] = 0;
				}
			}
 ```

- ***Step-2 Iterative Function*** - We create an iterative function that is similar to the recursive call function. All the conditions will be the same in both the methods, the only difference is that in memoization we do recursive calls whereas in the bottom-up approach we look up for previous cells in the matrix, this makes ***bottom-up approach a faster approach.***

```diff
- solved the classical knapsack problem using bottom-up approach.
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 SPOJ |[KNAPSACK - The Knapsack Problem](https://www.spoj.com/problems/KNAPSACK/) | [View Solution](./DAY-03/KNAPSACK-The_Knapsack_Problem(SPOJ).cpp) | Easy |||
<pre>
<b>Important Tip</b> -  The bottom-up approach is preferred over memoization because in the memoization technique 
we might get stack overflow on doing various recursive calls for large data.
</pre>

#### Though it's a rare condition. :sweat_smile::sweat_smile:
---
## Day - 4 :closed_book:
### Solved: Subset Sum Problem :pushpin::pushpin:
_It is a variation of the knapsack problem in which we are given an array of non-negative integers and a **required sum**. We need to find out that is it possible to create a subset of that array so that sum of elements of the subset equals the **required sum**._

```diff
@@ solved the subset sum problem @@
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 SPOJ |[PARTY - Party Schedule](https://www.spoj.com/problems/PARTY/) | [View Solution](./DAY-04/PARTY-Party_Schedule(SPOJ).cpp) | Easy |||
 GEEKSFORGEEKS |[Subset Sum Problem](https://practice.geeksforgeeks.org/problems/subset-sum-problem2014/1) | [View Solution](./DAY-04/Subset_Sum_Problem(GEEKSFORGEEKS).cpp) | Medium |||
  LEETCODE |[Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/) | [View Solution](./DAY-04/Partition_Equal_Subset_Sum(LEETCODE).cpp) | Medium |||

#### Finally DP started showing it's colors. :yellow_heart::blue_heart::purple_heart::green_heart::heart:

---
## Day - 5 :notebook:
### Solved: Count of Subsets with Required Sum :pushpin::pushpin:
_It is a slight variation of the *Subset Sum Problem* in which we are given an array of non-negative integers and a **required sum**. We need to find out the count of the total number of subsets of the given array whose sum equals the **required sum**._

```diff
! solved the Count of Subsets with Required Sum Problem
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 GEEKSFORGEEKS |[Perfect Sum Problem](https://practice.geeksforgeeks.org/problems/perfect-sum-problem5633/1) | [View Solution](./DAY-05/Perfect_Sum_Problem(GEEKSFORGEEKS).cpp) | Medium |||
#### :walking: “I walk slowly, but never backwards.” :walking: - — Abraham Lincoln :pray: :pray:

---
## Day - 6  :orange_book:
### Solved: Minimum Sum Partition Problem :pushpin::pushpin:
_Again its a variation of the **Subset Sum Problem**. The problem statement states that we are given an array with non-negative integers and our task is to divide the elements of that array into two subsets such that the absolute difference between their sums is **minimum.**_

```diff
+ solved the subset sum problem
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 GEEKSFORGEEKS |[Minimum sum partition](https://practice.geeksforgeeks.org/problems/minimum-sum-partition3317/1) | [View Solution](./DAY-06/Minimum_sum_partition(GEEKSFORGEEKS).cpp) | Hard |||
#### Some days are harder than others :confounded: :triangular_flag_on_post: :relieved:


---
## Day - 7  :blue_book:
### Solved: Count of Subsets with required difference :pushpin::pushpin:
_This is a variation of **Minimum Sum Partition Problem interesting problem**. In this, we are given an array with non-negative integers and our task is to divide the elements of that array into two subsets such that the absolute difference between their sums equals  **required difference.**_
##### Two equations to solve the problem are:
```cpp
 s1 = sum of 1st subset
 s2 = sum of 2nd subset
 S = required difference
 range = sum of entire array


 s1 - s2 = S 			//equation 1
 s1 + s2 = range		//equation 2

 // on solving eq1 and eq2 we get
 s1 = (range + S)/2
```
##### Target sum - It's an awesome problem. Must try:- https://leetcode.com/problems/target-sum/
```diff
- solved count of subsets with given difference
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 INTERVIEW BIT |[Minimum Difference Subsets!](https://www.interviewbit.com/problems/minimum-difference-subsets/) | [View Solution](./DAY-07/Minimum_Difference_Subsets!(INTERVIEWBIT).cpp) | Hard |||
  LEETCODE |[Target Sum :rocket:](https://leetcode.com/problems/target-sum/) | [View Solution](./DAY-07/Target_Sum(LEETCODE).cpp) | Hard |||
  
####  :yellow_heart:  7-Days Streak. :blue_heart: 7-Days of CP.  :purple_heart: 7-Days of DP :green_heart: 7-Days of OP :heart:
---
## Day - 8  :green_book:
### Solved: Unbounded Knapsack:pushpin::pushpin:
_**Unbounded Knapsack Problems** are slightly different from **0/1 Knapsack Problems**. In this, we can include the same item multiple numbers of times inside the knapsack and our aim is to just maximize the profit._ 
##### We just need to change one condition:
```cpp
//0-1 Knapsack
if(weight[i-1] <= j)
dp[i][j] = max((value[i-1] + dp[i-1][j-weight[i-1]]), dp[i-1][j]);

// Unbounded Knapsack
if(weight[i-1] <= j)
dp[i][j] = max((value[i-1] + dp[i][j-weight[i-1]]), dp[i-1][j]);
```
```diff
@@ solved Unbounded Knapsack Problem @@
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 HACKERRANK |[Knapsack](https://www.hackerrank.com/challenges/unbounded-knapsack/problem) | [View Solution](./DAY-08/Knapsack(HACKERRANK).cpp) | Medium |||
  GEEKSFORGEEKS |[Knapsack with Duplicate Items](https://practice.geeksforgeeks.org/problems/knapsack-with-duplicate-items4201/1) | [View Solution](./DAY-08/Knapsack_with_Duplicate_Items(GEEKSFORGEEKS).cpp) | Medium |||
  
####  Visited HackerRank after so Long ! Nostalgic :dizzy: :smile:
---

## Day - 9  :ledger:
### Solved: Rod Cutting Problem:pushpin::pushpin:
_**Problem Statement:** Given a rod of length **n** and an array of prices that contains prices of all pieces of size ranging from **1 to  n**. Determine the maximum value obtainable by cutting up the rod and selling the pieces._ 

```diff
! solved Rod Cutting Problem
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 GEEKSFORGEEKS |[Reach a given score](https://practice.geeksforgeeks.org/problems/reach-a-given-score/0) | [View Solution](./DAY-09/Reach_a_given_score(GEEKSFORGEEKS).cpp) | Easy |||
  GEEKSFORGEEKS |[Rod Cutting](https://practice.geeksforgeeks.org/problems/rod-cutting/0/?category) | [View Solution](./DAY-09/Rod_Cutting(GEEKSFORGEEKS).cpp) | Easy |||
  
####  Set Goals.  :star2:  Say Prayers. :pray:  Work Hard. :muscle:
---
## Day - 10  :closed_book:
### Solved: Coin Change Problem:moneybag: :moneybag:
_**Problem Statement:** You are given a value N and array of coins. You need to find out the number of ways in which you can get value N from that coins. There is infinite supply of coins.(Unbounded Knapsack :wink:)_ 

```diff
+ solved Rod Cutting Problem
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 GEEKSFORGEEKS |[Coin Change](https://practice.geeksforgeeks.org/problems/coin-change2448/1) | [View Solution](./DAY-10/Coin_Change(GEEKSFORGEEKS).cpp) | Medium |||
  HACKERRANK |[The Coin Change Problem](https://www.hackerrank.com/challenges/coin-change/problem) | [View Solution](./DAY-10/The_Coin_Change_Problem(HACKERRANK).cpp) | Medium |||
  
#### Prove Them Wrong :wink: :wink:


---
## Day - 11  :notebook:
### Solved: Maximize The Cut Segments Problem :pushpin: :pushpin:
 _**Problem Statement:** Given an integer **N** denoting the Length of a line segment. you need to cut the line segment in such a way that the cut length of a line segment each time is integer either **x**, **y**, or **z**. and after performing all cutting operations the total number of cut segments must be maximum._ 

```diff
- solved Coin Change 2 Problem
```
### Problem solved
|  Platform    | Title           |  Solution       | Difficulty    |
|--------------|---------------- | --------------- |---------------|
 GEEKSFORGEEKS |[Maximize The Cut Segments](https://practice.geeksforgeeks.org/problems/cutted-segments/0) | [View Solution](./DAY-11/Maximize_The_Cut_Segments(GEEKSFORGEEKS).cpp) | Easy |||
  LEETCODE |[Coin Change](https://leetcode.com/problems/coin-change/) | [View Solution](./DAY-11/Coin_Change(LEETCODE).cpp) | Medium |||
  GEEKSFORGEEKS |[Number of Coins](https://practice.geeksforgeeks.org/problems/number-of-coins1824/1) | [View Solution](./DAY-11/Number_of_Coins(GEEKSFORGEEKS).cpp) | Medium |||
  <pre>
<b>Important Tip</b> -  This is a unique problem of Knapsack Family. 
In this, we have to initialize 2nd row as well.
</pre>
```cpp
for(int i =1; i<amount+1;i++)
{
	if(i%coins[0] == 0)
		dp[1][i] = i/coins[0];
	else
		dp[1][i] = INT_MAX -1;
}
```

#### Finally, struggled for 3 days to solve Maximize The Cut Segments  :relieved: :relieved:
---
