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
	p ^ (p v q) <=> P
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

|	p 	|	q	|  p --> q  | ¬p | ¬p v q |?
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
