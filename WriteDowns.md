# Sets
## the empty set
	  Ø   = { }
	 |Ø|  =  0
	|{Ø}| =  1
	|{ }| =  0 

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

### Example
	P(Ø) 	= 0

	P({Ø}) = {Ø, {Ø}} = 2
	is A subset in P(A)?
		No
	is A element in P(A)?
		Yes

## set Operations, Venn Diagrams
> each set A is in a universe U 
	A is a subset of U 

# Truth Tables
## Negation (¬p, ~) (Same as Not in python)
| 	p 	| ¬p    |
|-------|-------|
|	1	| 	0	|
|	0	|	1	|
### ¬p = 1 - p

## Conjunction (^, &, .)
|	p 	|	q	|	p ^ q	|
|-------|-------|-----------|
|	1	|	1	|	  1		|
|	1	|	0	|	  0		|
|	0	|	1	|	  0		|
|	0	|	0	|	  0		|
	p ^ q = min(p,q)

## Disjunction (v, +)
|	p 	|	q	|	p v q	|
|-------|-------|-----------|
|	1	|	1	|	  1		|
|	1	|	0	|	  1		|
|	0	|	1	|	  1		|
|	0	|	0	|	  0		|
	p ^ q = max(p,q)

## Conditional (--> , ⊃ )
|	p 	|	q	|  p --> q	|
|-------|-------|-----------|
|	1	|	1	|	  1		|
|	1	|	0	|	  0		|
|	0	|	1	|	  1		|
|	0	|	0	|	  1		|
	p --> q == 1; iff p is less than or equal to q;

## Biconditional (<->,) iff
|	p 	|	q	|  p <-> q	|
|-------|-------|-----------|
|	1	|	1	|	  1		|
|	1	|	0	|	  0		|
|	0	|	1	|	  0		|
|	0	|	0	|	  1		|
	p == q; then p <-> q = 1

## Excluside Or (⊕, ⊻) iff
|	p 	|	q	|   p v q	|
|-------|-------|-----------|
|	1	|	1	|	  0		|
|	1	|	0	|	  1		|
|	0	|	1	|	  1		|
|	0	|	0	|	  0		|
	p is not equal to q; then p (+) q = 1

## Sheffer Stroke
## Nand  (not and equal )
|	p 	|	q	| not(p ^ q)|
|-------|-------|-----------|
|	1	|	1	|	  0		|
|	1	|	0	|	  1		|
|	0	|	1	|	  1		|
|	0	|	0	|	  1		|

## Nand (not and equal) 
|	p	| not(p ^ p) |
|-------|------------|
|	1	|	   0	 |
|	0	|	   1	 |
	p nand p <=> ¬p

# Logic Laws
> We can use logical equivalences to reduce complex formulas into simpler ones.
	T0 = Tautology	(Always 1)
	F0 = Tautology	(Always 0)

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
not(¬p) v ((p v F) ^ not(¬q))

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
	not(p ^ q) ^ q
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
	* ∃x == there exists at least one x/ fpr some x


		∀x P(x): "For all  x, x is P"
		∃x P(x): "For some x, x is P"

### Example

	For every real number n, there is a real number m such that m^2 = n.
	\					  /  \					    / \				   /
			  ∀n∈ℝ					 ∃m∈ℝ 		 : 		 m^2		

## Negating Quantifiers
* Define ∀x, ∃x for a universe with elements {1,2,..., n}


	∀x P(x) <=> p(1) ^ p(2) ^ ... ^ p(n)  
	∃x P(x) <=> p(1) v p(2) v ... v p(n)

### Example
	
	¬∀xP(x) <=> ¬(p(1) ^ p(2) ^ ... ^ p(n))

