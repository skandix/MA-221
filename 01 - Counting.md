# Counting 

##  Rule of sum (Principle of Addition)
* For two seperate tasks, 
	* if Task A can be done in n ways, and
	* Task B can be done in m ways.
		* Then A and B can be done n + m ways

## Rule of Product (Product Principle)
* In a list, AB If there are
	* n ways of choosing A, and
	* m ways of choosing B, then
		*  There are n x m ways of choosing AB.

### Example
How many ways can we pick a license plate with

	a. 3 Letters, then 4 numbers
		* 26 x 26 x 26  x 10 x 10 x 10 x 10 = 26^3 x 10^4

	b. 2 Even numbers, 3 vowels, 1number, then 2 letters?
		* 2 Even Numbers =  5 x 5 
		* 3 Vowels = 5 x 5 x 5 
		* 1 Number = 10
		* 2 Letters = 26 x 26
			* Answer = 5^5 x 10 x 26^2


## Factorials

	n! = (n)(n-1)(n-2) ... (3)(2)(1)

* 4! = 4 x 3 x 2 x 1  = 24 
* 6! = 6 x 5 x 4 x 3 x 2 x 1 = 720
* 0! = 1

## Permutations
> The number of permutations of length k from a list of n elements is:

		n!/(n-k)! - With no repetition
		On the calculator p(n,k)

### Example 
1. How many ways can we list 4 number out of a list consisting of 7 numbers w/o repetition?

		n = 7
		k = 4 

		P(7,4) = 7!/(7-4)! = 7!/3! = 840

2. How many permutation can we make with the word BASE?
		
		n = 4
		k = 4
		P(4,4) =  4!/(4-4)! = 4!/0! = 4!/1

3. How many permutations can we make with the word BALL?

		B A L  
			L 

		4!/2! = 4x3 = 12

4. How many arrangements can we make with the word DATABASES?

		D A T B S E
		  A 	S
		  A

		  A = 3! 
		  S = 2!
		  9!/2!x3! = 30240

## Combinations
> if n and k are integers then (n over k) is the amount of subsets that can be made using k elements in an n elements set.

		(n over k ) = n choose k
					= C(n,k) <--- Can be found on the calculator
					= n!/ k!(n-k)!

### Example
1. Evaluate (9 over 4)

		(9 over 4) = 9! / 4!(5!) = 126

2. Evaluate (6 over 3)

		(6 over 3) = 6!/3!(6-3)! = 6!/3!x3! = 20 

3.  Given the word TALLAHASSE, how many arrangements can be made with no consecutive vowels?
	
		T A L H S E
		  A L   S E
		  A

		a)  
		TLLHSS = 6!
		L = 2!
		S = 2!
		6!/2!2!

		b)
		 . T . L . L . H . S . S .
		 . = 7
		 vowels = 5
		 (7 over 5)

		c)
		AAAEE
		A = 3!
		E = 2!
		5! / 3!2!

**Answer; (6!/2!2!) x (7 over 5) x (5!/3!2!)**
