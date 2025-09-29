//Checkpoint 2
//README
//Name: Yunzhe Jiang
//NetID:yj257

//Design Description
// Implements addition (00000) and subtraction (00001).
// Subtraction uses A - B = A + (~B) + 1 with a Carry-Select Adder.
// The 32-bit Carry-Select Adder is built from 8-bit Ripple-Carry Adders.
// Overflow is detected when inputs have same sign but result has different sign.

// Implements bitwise AND (00010) and OR (00011).
// Done with gate-level primitives for each bit.
// Implements SLL (00100) and SRA (00101).
// Built a 32-bit barrel shifter with shifts by 1,2,4,8,16.
// SLL fills with zeros, SRA fills with the sign bit.
// isNotEqual is 1 if (A - B) != 0, checked with an OR-tree.
// isLessThan is (A - B sign) XOR overflow.
// isNotEqual, isLessThan, overflow are only active for SUB or ADD.

//Issues
// No major issues found in testing.
// Some testbenches for edge cases maybe have some problems.
// Pass the tesbench checking.
