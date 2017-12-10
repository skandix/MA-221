# the empty set
	  Ø   = { }
	 |Ø|  =  0
	|{Ø}| =  1
	|{ }| =  0 

# SetBuilder Notation
	{ form | rule  }
	{ m/n  | m,n element in Z, n ≠ 0 }

# Cartesian Product AxB

	A = {a,b,c}
	B = {0,1}
	then A x B = {(a,0),(a,1),(b,0),(b,1),(c,0),(c,1)}
	|A| = 3
	|B| = 2
	if A and B are finite sets!
		|A x B | = |A| * |B|

	A1 x A2 x ... x An = {(A1, A2, ..., An)| Ai € Ai for all i}

# Subset
> B is a subset of A if every element in B is also in A.
### Example 
	A = {1,2,3,4,5,6}
	B = {1,3,4,5}
	B is a subset of A

# power set 
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

# set Operations, Venn Diagrams
> each set A is in a universe U 
	A is a subset of U 

# Truth Tables
## Negation (-p, ~)
| 	p 	| not(p)|
|-------|-------|
|	1	| 	0	|
|	0	|	1	|
### not(p) = 1 - p

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

## Conditional (--> , speilvendt(C) )
|	p 	|	q	|  p --> q	|
|-------|-------|-----------|
|	1	|	1	|	  1		|
|	1	|	0	|	  0		|
|	0	|	1	|	  1		|
|	0	|	0	|	  1		|
	p --> q == 1; iff p is less than or equal to q;

## Biconditional (<->,  ) iff
|	p 	|	q	|  p <-> q	|
|-------|-------|-----------|
|	1	|	1	|	  1		|
|	1	|	0	|	  0		|
|	0	|	1	|	  0		|
|	0	|	0	|	  1		|
	p == q; then p <-> q = 1

## Excluside Or ((+), ) iff
|	p 	|	q	|   p v q	|
|-------|-------|-----------|
|	1	|	1	|	  0		|
|	1	|	0	|	  1		|
|	0	|	1	|	  1		|
|	0	|	0	|	  0		|
	p is not equal to q; then p (+) q = 1

# Sheffer Stroke

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
	p nand p <=> not(p)

# Logic Laws
> We can use logical equivalences to reduce complex formulas into simpler ones.
	T0 = Tautology	(Always 1)
	F0 = Tautology	(Always 0)

# Identity Laws
	P ^ T <=> P
	P v F <=> P

# Domination Laws
	P v T <=> True
	P ^ F <=> False

### Example 
(P v F ) ^ (q v T)

	(P v F) == (Identity Laws) P
	(q v T) == (Domination Laws) True
	P ^ T   == (Identity Laws) P
	Answer; P 

# Double Negation
	not(not(p)) <=> p

# DeMorgan's Law
	not(p ^ q) <=> not(p) v not(q)
	not(p v q) <=> not(p) ^ not(q)

### Example
	not((not(p) ^ not(q)))
	not(not(p)) v not(not(q)) == (DeMorgans)
	answer; p v q			  == (Double Negation)

# Distributive Law
	p ^ (q v r) <=> (p ^ q) v (p ^ r)
	p v (q ^ r) <=> (p v q) ^ (p v r)

# Absorption Law
	p ^ (p ^ q) <=> P
	p v (p ^ q) <=> P

### Example 
not(not(p)) v ((p v F) ^ not(not(q)))

	p v ((p v F) ^ q) == (Double Negation)x2
	p v (p ^ q )	  == (Identity Law)
	P 				  == (Absorption Law)

# Commutativity (v, ^)
	p ^ q <=> q ^ p
	p v q <=> q v p

# Associativity (v, ^)
	p ^ (q ^ r) <=> (p ^q ) ^ r

# Inverse Laws
	p ^ not(p) <=> F 
	p v not(p) <=> T


# Conditional Law
p --> q <=> not(p) v q

|	p 	|	q	|  p --> q  | not(p) | not(p) v q |
|-------|-------|-----------|--------|------------|
|	1	|	1	|	  1		|	1	 |	 	1	  |
|	1	|	0	|	  0		|	1	 |	 	0	  |
|	0	|	1	|	  1		|	1	 |	 	0	  |
|	0	|	0	|	  1		|	1	 |	 	0	  |


### Example 
	not(p ^ q) ^ q
	( not(p) v not(q) ) ^ q 	== DeMorgan Law
	(q ^ not(p)) v (q ^ not(q)) == Distributive Law
	q ^ not(p) v False			== Inverse Laws					
	q ^ not(p)					== Identity Laws
	not(p) ^ q 					== Commutativity

