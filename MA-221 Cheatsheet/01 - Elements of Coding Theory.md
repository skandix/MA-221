# Elements of coding Theory

## How to solve error-code matrix..
		 _ 					 _
		| 1 0 1 0 0 0 |
		| 1 1 0 1 0 0 |
		| 1 1 0 0 1 0 |
		|_0 1 0 0 0 1_|
		This is matrix H

		H-Matrix == Parity Checking Matrix
		G-Matrix == Generator Matrix

		We need to split H Matrix into two seprate, Matrixes
		 _   _
		| 1 0 |
		| 1 1 |
		| 1 1 |
		|_0 1_|
		This is a remainder matrix A
		 _       _
		| 1 0 0 0 |
		| 0 1 0 0 |
		| 0 0 1 0 |
		|_0 0 0 1_|
		This is a identity Matrix I

		Since we are finding G-Matrix, we know that G = [I A^T]
					_ 			 _
		A^T = | 1 1 1 0 |
				  |_0 1 1 1_|
				 _   _
		I = | 1 0 |
		    |_0 1_|
		     _ 					 _
		G = | 1 0 1 1 1 0 |
	  		|_0 1 0 1 1 1_|

since there is m = 2 rows in G, then the message is 2bits, this gives ut that M = [2^m * m] = [4 * 2]
* m1 = 00
* m2 = 01
* m3 = 10
* m4 = 11

							 _					 _
* C1 = [00] * | 1 0 1 1 1 0 | 
	  					|_0 1 0 1 1 1_|
	
	* 0x1 (xor) 0x1 = 0
							 _					 _
* C2 = [01] * | 1 0 1 1 1 0 |
	  					|_0 1 0 1 1 1_|
							 _					 _
* C3 = [10] * | 1 0 1 1 1 0 |
	  					|_0 1 0 1 1 1_|
							 _					 _
* C4 = [11] * | 1 0 1 1 1 0 |
	  					|_0 1 0 1 1 1_|
