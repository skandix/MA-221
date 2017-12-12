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