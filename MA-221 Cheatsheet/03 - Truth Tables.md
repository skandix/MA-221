# Truth Tables
## Negation (¬p, ~) (Same as Not in python)
| 	p 	| ¬p    |
|-------|-------|
|	0	| 	1	|
|	1	|	0	|

```
¬p = 1 - p
```

## Conjunction (^, &, .)
|	p 	|	q	|	p ^ q	|
|-------|-------|-----------|
|	0	|	0	|	  0		|
|	0	|	1	|	  0		|
|	1	|	0	|	  0		|
|	1	|	1	|	  1		|
```python
p ^ q = min(p,q)
```

## Disjunction (v, +)
|	p 	|	q	|	p v q	|
|-------|-------|-----------|
|	0	|	0	|	  0		|
|	0	|	1	|	  1		|
|	1	|	0	|	  1		|
|	1	|	1	|	  1		|
```python
p v q = max(p,q)
```

## Conditional (--> , ⊃ )
|	p 	|	q	|  p --> q	|
|-------|-------|-----------|
|	0	|	0	|	  1		|
|	0	|	1	|	  1		|
|	1	|	0	|	  0		|
|	1	|	1	|	  1		|
```
p --> q == 1
iff p is less than or equal to q
```

## Biconditional (<->, ≡) iff
|	p 	|	q	|  p <-> q	|
|-------|-------|-----------|
|	0	|	0	|	  1		|
|	0	|	1	|	  0		|
|	1	|	0	|	  0		|
|	1	|	1	|	  1		|
```
p == q; then p <-> q = 1
note: ¬(p⊕q)= p <-> q and vice verca
```

## Exclusive Or (⊕, ⊻)
|	p 	|	q	|   p ⊕ q	|
|-------|-------|-----------|
|	0	|	0	|	  0		|
|	0	|	1	|	  1		|
|	1	|	0	|	  1		|
|	1	|	1	|	  0		|
```
p is not equal to q; then p (+) q = 1
```

## Sheffer Stroke
## Nand  (not and equal )
|	p 	|	q	| ¬(p ^ q)|
|-------|-------|-----------|
|	0	|	0	|	  1		|
|	0	|	1	|	  1		|
|	1	|	0	|	  1		|
|	1	|	1	|	  0		|
```python
not(p and q)
```

## Nand (not and equal) 
|	p	| ¬(p ^ p) |
|-------|------------|
|	1	|	   0	 |
|	0	|	   1	 |
```
p nand p <=> ¬p
nand is sometimes written as  ↑: p ↑ q <=> ¬(p ^ p)
```