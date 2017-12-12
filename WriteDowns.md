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


# Sets
## the empty set
	  Ø   = { }
	 |Ø|  =  0
	|{Ø}| =  1
	|{ }| =  0 , Because  Ø   = { }

## SetBuilder Notation
	{ form | rule  }
	{ m/n  | m,n element in Z, n ≠ 0 }

## Cartesian Product AxB

	A = {a,b,c}
	B = {0,1}
	then A x B = {(a,0),(a,1),(b,0),(b,1),(c,0),(c,1)}
	|A| = 3
	|B| = 2
	if A and B are finite sets!
		|A x B | = |A| * |B|

	A1 x A2 x ... x An = {(A1, A2, ..., An)| Ai € Ai for all i}

## Subset
> B is a subset of A if every element in B is also in A.
### Example 
	A = {1,2,3,4,5,6}
	B = {1,3,4,5}
	B is a subset of A

## power set 
	is a set of all possible subsets

	If |A| = n
		|P(A)| = 2^n = 2^(|A|)
		Each element can be in a subset or not.

### Example's
	P(Ø) 	= 0
	
	A = {Ø}
	P({Ø}) = {Ø, {Ø}} = 2
	is A subset in P(A)?
		Yes, {Ø} is in P({Ø})
	is A element in P(A)?
		Yes, Ø is in P({Ø})

## set Operations, Venn Diagrams
> each set A is in a universe U 
	A is a subset of U 

# Truth Tables
## Negation (¬p, ~) (Same as Not in python)
| 	p 	| ¬p    |
|-------|-------|
|	0	| 	1	|
|	1	|	0	|
### ¬p = 1 - p

## Conjunction (^, &, .)
|	p 	|	q	|	p ^ q	|
|-------|-------|-----------|
|	0	|	0	|	  0		|
|	0	|	1	|	  0		|
|	1	|	0	|	  0		|
|	1	|	1	|	  1		|
	p ^ q = min(p,q)

## Disjunction (v, +)
|	p 	|	q	|	p v q	|
|-------|-------|-----------|
|	0	|	0	|	  0		|
|	0	|	1	|	  1		|
|	1	|	0	|	  1		|
|	1	|	1	|	  1		|
	p ^ q = max(p,q)

## Conditional (--> , ⊃ )
|	p 	|	q	|  p --> q	|
|-------|-------|-----------|
|	0	|	0	|	  1		|
|	0	|	1	|	  0		|
|	1	|	0	|	  1		|
|	1	|	1	|	  1		|
	p --> q == 1; iff p is less than or equal to q;

## Biconditional (<->,) iff
|	p 	|	q	|  p <-> q	|
|-------|-------|-----------|
|	0	|	0	|	  1		|
|	0	|	1	|	  0		|
|	1	|	0	|	  0		|
|	1	|	1	|	  1		|
	p == q; then p <-> q = 1
	note: ¬(p⊕q)= p <-> q and vice verca

## Excluside Or (⊕, ⊻) iff
|	p 	|	q	|   p ⊕ q	|
|-------|-------|-----------|
|	0	|	0	|	  0		|
|	0	|	1	|	  1		|
|	1	|	0	|	  1		|
|	1	|	1	|	  0		|
	p is not equal to q; then p (+) q = 1

## Sheffer Stroke
## Nand  (not and equal )
|	p 	|	q	| ¬(p ^ q)|
|-------|-------|-----------|
|	0	|	0	|	  1		|
|	0	|	1	|	  1		|
|	1	|	0	|	  1		|
|	1	|	1	|	  0		|

## Nand (not and equal) 
|	p	| ¬(p ^ p) |
|-------|------------|
|	1	|	   0	 |
|	0	|	   1	 |
	p nand p <=> ¬p
	nand is sometimes written as  ↑: p ↑ q <=> ¬(p ^ p)

# Logic Laws
> We can use logical equivalences to reduce complex formulas into simpler ones.

	T0 = Tautology		(Always 1, sometimes written as '1', instead of T)
	F0 = Contradiction 	(Always 0, sometimes written as '0', instead of F)

# Identity Laws
	P ^ T <=> P
	P v F <=> P

# Domination Laws
	P v T <=> T0
	P ^ F <=> F0

### Example 
(P v F ) ^ (q v T)

	(P v F) == (Identity Laws) P
	(q v T) == (Domination Laws) T0
	P ^ T   == (Identity Laws) P
	Answer; P 

# Double Negation
	¬¬p <=> p

# DeMorgan's Law
	¬(p ^ q) <=> ¬p v ¬q
	¬(p v q) <=> ¬p ^ ¬q

### Example
	¬(¬p ^ ¬q)
	¬¬p v ¬¬q == (DeMorgans)
	answer; p v q			  == (Double Negation)

# Distributive Law
	p ^ (q v r) <=> (p ^ q) v (p ^ r)
	p v (q ^ r) <=> (p v q) ^ (p v r)

# Absorption Law
	p ^ (p ^ q) <=> P
	p v (p ^ q) <=> P

### Example 
¬(¬p) v ((p v F) ^ ¬(¬q))

	p v ((p v F) ^ q) == (Double Negation)x2
	p v (p ^ q )	  == (Identity Law)
	P 				  == (Absorption Law)

# Commutativity (v, ^)
	p ^ q <=> q ^ p
	p v q <=> q v p

# Associativity (v, ^)
	p ^ (q ^ r) <=> (p ^q ) ^ r

# Inverse Laws
	p ^ ¬p <=> F 
	p v ¬p <=> T


# Conditional Law
p --> q <=> ¬p v q

|	p 	|	q	|  p --> q  | ¬p | ¬p v q |
|-------|-------|-----------|--------|------------|
|	1	|	1	|	  1		|	1	 |	 	1	  |
|	1	|	0	|	  0		|	1	 |	 	0	  |
|	0	|	1	|	  1		|	1	 |	 	0	  |
|	0	|	0	|	  1		|	1	 |	 	0	  |


### Example 
	¬(p ^ q) ^ q
	( ¬p v ¬q ) ^ q 	== DeMorgan Law
	(q ^ ¬p) v (q ^ ¬q) == Distributive Law
	q ^ ¬p v False			== Inverse Laws					
	q ^ ¬p					== Identity Laws
	¬p ^ q 					== Commutativity


# Conditionals 

## Conditional
	p --> q <=> ¬q v p

## Contrapositive
	¬q --> ¬p <=> q v ¬p

## Converse
	q --> q <=> q v ¬p

## Inverse 
	¬p --> ¬q <=> p v ¬q

### Logically Equvialent (Just draw this)
https://datapor.no/loot/lVyftyrx298.png


## Biconditional
p <-> <=> (p --> q) ^ (q --> p)

|	p 	|	q	|  p <-> q  | p -> q |  	^     |  q --> p   |
|-------|-------|-----------|--------|------------|------------|
|	1	|	1	|	  1		|	1	 |	 	1	  |	 	1	   |
|	1	|	0	|	  0		|	0	 |	 	0	  |	 	1	   |
|	0	|	1	|	  0		|	1	 |	 	0	  |	 	0	   |
|	0	|	0	|	  1		|	1	 |	 	1	  |	 	1	   |

# Rules of Inference
> ∴ == Therefore

	R --> W } Premise
	R 		}
	______
	∴  W 	- Conclusion

	This is the same as above, if seen as a truth table*
	((R --> W) ^ R) --> W (Tautology)

* A set of premises P1, P2,...,Pn prove some conclusion q in an argument

	* (p1 ^ p2 ^ ... ^ pn ) --> q

* An argument is valid if the premiseslogically entail the conlcusion

## Laws
1. Modus Ponens (MPP)
	
		P --> q
		P
		_______
		∴ q

2. Modus Tollens (MTT)
	
		P --> q
		¬P
		_______
		∴ ¬p

3. Hypothetical Syllogism (HS)
	
		P --> q
		q --> r
		________
		∴ p --> r

4. Disjunctive Syllogism (DS)
	
		P v q
		¬P
		________
		∴ q

5. Addition (Or Introduction)
	
		P
		_______
		∴ p v q 

6. Simplification (And Elimination)
	
		P ^ q
		_______
		∴ p
		∴ q

7. Conjunction (And Introduction)
	
		P
		q
		_______
		∴ p ^ q

# Predicate Logic and Quantifiers

## Quantifiers
* ∀ = Universial
	* ∀x == for all x 
* ∃ = Extensial 
	* ∃x == there exists at least one x/ fOr some x


			∀x P(x): "For all  x, x is P"			
			∃x P(x): "For some x, x is P"


### Example

	For every real number n, there is a real number m such that m^2 = n.
	\					  /  \					    / \				   /
			  ∀n∈ℝ						∃m∈ℝ 		 : 		 m^2		

## Negating Quantifiers
* Define ∀x, ∃x for a universe with elements {1,2,..., n}


	∀xP(x) <=> p(1) ^ p(2) ^ ... ^ p(n)  
	∃xP(x) <=> p(1) v p(2) v ... v p(n)

### Example
Show that ¬∀xP(x) <=> ∃x[¬P(x)]
	
	¬∀xP(x) = ¬(p(1) ^ p(2) ^ ... ^ p(n))
			= ¬P(1) v P(2) v ... v P(n)
			= ∃x[¬P(x)]			


## All Equivalencies
	
	∀xP(x)  <=>	¬∃x[¬P(x)]
	∃xP(x)  <=> ¬∀x[¬P(x)]
	¬∀xP(x) <=> ∃x[¬P(x)]
	¬∃xP(x) <=> ∀x[¬P(x)]

*https://datapor.no/loot/g6oRHTAIddv.png* wtf

### Example
> Negate the following

		[∀x[∃y[ P(x,y) ^ Q(y)]]]
	=  ¬[∀x[∃y[ P(x,y) ^ Q(y)]]]
	= 	∃x¬[∃y[P(x,y) ^ Q(y)]]
	= 	∃x∀y¬[P(x,y) ^ Q(y)] == DeMorgans Law
	=	∃x∀y[¬P(x,y) ^ ¬Q(y)]

