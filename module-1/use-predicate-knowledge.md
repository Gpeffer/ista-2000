Understand

1.
¬(NOT)
∧(AND)
∨(OR); ⊻(XOR)
⇔(EQUAL TO)

2. A Half Adder take two single digit binary numbers and gives a two digit output, being the result of the equation and the carry.

3. A Full Adder is essentially two half Adders combined, with the exception of having three inputs as opposed to two inputs. It has the two orginal input, A and B, as well as the Carry input from a previous calculation or half adder. This will also result in a two digit output, the result of the calculation and the carry.



Apply

1.	A	NOT			A  B	AND
	0	1			0  0    0
	1	0			0  1	0
					1  0	0
					1  1	1


	A  B	OR			A  B	XOR
	0  0	0			0  0	0
	0  1	1			0  1	1
	1  0	1			1  0	1
	1  1	1			1  1	0



2.
	A   B   C		A ∧ B		¬C		A ∧ B ∨ ¬C   Result
	0   0   0		  0		 1		  0	 1   1
	0   0   1		  0		 0		  0	 0   0
	0   1   0		  0		 1		  0	 1   1
	0   1   1		  0		 0		  0	 0   0
	1   0   0		  0		 1		  0	 1   1
	1   0   1		  0		 0		  0	 0   0
	1   1   0		  1		 1		  1	 1   1
	1   1   1		  1		 0		  1	 0   1


3. Using truth tables, show ¬(P ∨ Q) ⇔ (¬P) ∧ (¬Q)

	P ∨ Q   Result		¬(P ∨ Q)	(¬P) ∧ (¬Q)	Result
	0   0	0		1		1	1	1
	0   1	1		0		1	0	0
	1   0	1		0		0	1	0
	1   1	1		0		0	0	0



4. Using truth tables, show ¬(P ∧ Q) ⇔ (¬P) ∨ (¬Q)

	P ∧ Q	Result		¬(P ∧ Q)	(¬P) ∨ (¬Q)	Result
	0   0	0		1		1	1	1
	0   1	0		1		1	0	1
	1   0	0		1		0	1	1
	1   1	1		0		0	0	0
