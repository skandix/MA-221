# Predicate Logic and Quantifiers

## Quantifiers
* **∀** = Universial
	* **∀x** == for all **x** 
* **∃** = Extensial 
	* **∃x** == there exists at least one **x** for some **x**

```
∀x P(x): "For all  x, x is P"			
∃x P(x): "For some x, x is P"
```

### Example

```
For every real number n, there is a real number m such that m^2 = n.
\					  /  \					    / \				   /
		∀n∈ℝ						∃m∈ℝ 		 : 		 m^2		

```
## Negating Quantifiers
* Define **∀x**, **∃x** for a universe with elements **{1, 2, ..., n}**
```
∀xP(x) <=> p(1) ^ p(2) ^ ... ^ p(n)  
∃xP(x) <=> p(1) v p(2) v ... v p(n)
```

### Example
Show that ```¬∀xP(x) <=> ∃x[¬P(x)]```
	
```
¬∀xP(x) = ¬(p(1) ^ p(2) ^ ... ^ p(n))
		= ¬P(1) v P(2) v ... v P(n)
		= ∃x[¬P(x)]			
```

## All Equivalencies
```
∀xP(x)  <=>	¬∃x[¬P(x)]
∃xP(x)  <=> ¬∀x[¬P(x)]
¬∀xP(x) <=> ∃x[¬P(x)]
¬∃xP(x) <=> ∀x[¬P(x)]
```

*https://datapor.no/loot/g6oRHTAIddv.png* wtf

### Example
> Negate the following
```
	[∀x[∃y[ P(x,y) ^ Q(y)]]]
=  ¬[∀x[∃y[ P(x,y) ^ Q(y)]]]
= 	∃x¬[∃y[P(x,y) ^ Q(y)]]
= 	∃x∀y¬[P(x,y) ^ Q(y)] == DeMorgans Law
=	∃x∀y[¬P(x,y) ^ ¬Q(y)]
```