# Elements of coding Theory

## How to solve error-code matrix..

		| 1 0 1 0 0 0 |
		| 1 1 0 1 0 0 |
		| 1 1 0 0 1 0 |
		| 0 1 0 0 0 1 |
		This is matrix H

		H-Matrix == Parity Checking Matrix
		G-Matrix == Generator Matrix

		We need to split H Matrix into two seprate, Matrixes

		| 1 0 |
		| 1 1 |
		| 1 1 |
		| 0 1 |
		This is a remainder matrix A

		| 1 0 0 0 |
		| 0 1 0 0 |
		| 0 0 1 0 |
		| 0 0 0 1 |
		This is a identity Matrix I

		Since we are finding G-Matrix, we know that G = [I A^T]
					
		A^T = | 1 1 1 0 |
				  | 0 1 1 1 |
				    
		I = | 1 0 |
		    | 0 1 |

		G = | 1 0 1 1 1 0 |
	  		| 0 1 0 1 1 1 |

since there is m = 2 rows in G, then the message is 2bits, this gives ut that M = [2^m * m] = [4 * 2]
* m1 = 00
* m2 = 01
* m3 = 10
* m4 = 11
 
* C1 = [00] * | 1 0 1 1 1 0 | 
	  					| 0 1 0 1 1 1 |	
	* 0x1 (xor) 0x1 = 0
							 
* C2 = [01] * | 1 0 1 1 1 0 |
	  					| 0 1 0 1 1 1 |

* C3 = [10] * | 1 0 1 1 1 0 |
	  					| 0 1 0 1 1 1 |

* C4 = [11] * | 1 0 1 1 1 0 |
	  					| 0 1 0 1 1 1 |
