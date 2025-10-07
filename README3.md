// Checkpoint 3 README
// Name: Yunzhe Jiang
// NetID: yj257

// Design Description
// Implements a 32-bit register file with 2 read ports and 1 write port
// Register x0 is always equal to 0
// Write happens on rising clock edge when ctrl_writeEnable is high
// Outputs change once the address changes
// All storage bits use the provided dffe_ref flip-flop
// Address decoding is one-hot using XNOR + AND gates, no behavioral if/case.
// Read ports built with tri-state bus style, only the selected register can drive the bus
// ctrl_reset asynchronously clears all registers to 0.

// Issues
// No major issues found in testing
// Auto-checker flagged behavioral statements in dffe_ref but that file is given by course
// The regfile itself follows the structural-Verilog rules
