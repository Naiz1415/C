// Checkpoint 4 README
// Name: Yunzhe Jiang
// NetID: yj257

// Design Description
// Implements the top-level simple processor system integrating all major components:
//  - processor.v: CPU core containing datapath and control logic
//  - alu.v: performs arithmetic and logic operations (add, sub, and, or, sll, sra)
//  - regfile.v: 32-bit register file with 2 read ports and 1 write port
//  - dmem.v and imem.v: on-chip data and instruction memories (altsyncram-based ROM/RAM)
//  - dffe_ref.v: provided D flip-flop with enable and asynchronous clear
//  - skeleton.v: top-level wrapper connecting all modules for simulation and testing
//
// The processor fetches 32-bit instructions from imem, executes them via the ALU,
// reads/writes register file and data memory, and writes results back to registers.
// The instruction set includes add, sub, and, or, sll, sra, lw, sw, addi.
//
// The imem uses a .mif file (basic_test.mif) generated from basic_test.s assembly code.
// Each instruction is stored as a 32-bit binary word loaded at simulation start.
// The top-level simulation (ModelSim) shows instruction fetch and execution over time.
//
// Simulation setup:
//   vsim -L altera_mf_ver -L lpm_ver work.skeleton
//   add wave *
//   run 2000ns
// The test program (basic_test.s) verifies arithmetic, logical, shift, and memory ops.
// Expected waveforms show register writes (ctrl_writeEnable high) and correct ALU results.

// Issues
// - The initial simulation showed all-zero waveforms due to empty basic_test.mif.
//   This was resolved by regenerating the MIF from basic_test.s using the assembler script.
// - Must include the altera_mf_ver and lpm_ver libraries for altsyncram instantiation.
// - The imem and dmem require correct path setup for MIF loading during RTL simulation.
// - After fixing MIF and library linkage, the processor executes correctly in ModelSim.
// No other major functional issues remain; all basic_test instructions execute as expected.
