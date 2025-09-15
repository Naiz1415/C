// README
// Simple ALU Checkpoint 1

//Name: [Yunzhe Jiang]
//NetID: [yj257]

// Implements addition (00000) and subtraction (00001). Subtraction is implemented by bitwise inverting B and adding 1, meaning A - B = A + (~B) + 1.
// Use a Carry-Select Adder to split the 32-bit adder into four 8-bit segments. Each segment uses two Ripple-Carry Adders to select the correct result based on the carry bit.
// Implements overflow detection by checking whether the two operands have the same sign and the results have different signs. Use logic gates such as xor, not, and and to construct the logic.
// Checkpoint 1 does not require any other functionality; isNotEqual and isLessThan are set to 0.
