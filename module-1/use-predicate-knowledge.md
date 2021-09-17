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


5. Reference 8-bit-adder.png


6. "A" and "B" are XOR'd and then pushed to the final XOR gate for the fist adder. This is then XOR'd with any carry brought forward from a previous calculation. This determines the result for the first bit calculation. Furthermore, the result of the initial XOR with "A" and "B" is AND'd with the carry bit brought in from the previous calculation, and then sent to the final OR gate for the carry bit. In addition to this, an AND gate is branched off from right before the initial XOR gate for "A" and "B" and sent to the OR gate with the result of "C AND (A XOR B)". This determines what the carry bit that will be brought forward is.


7. 


8. L & H
