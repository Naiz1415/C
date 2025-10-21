// Checkpoint 4 README
// Name: Yunzhe Jiang, Mingyuan Sun
// NetID: yj257, ms1347

// Design Description
// This checkpoint implements the top-level skeleton and connects the processor,
// instruction memory (imem), data memory (dmem), and register file (regfile).
// The design also adds clock division modules to provide slower clocks for
// certain components for stable timing during simulation and synthesis.
// Two divider modules are used:
//  freq_div_by2: divides the 50 MHz input clock by 2
//  freq_div_by4: divides the 50 MHz input clock by 4
// The slower clocks are then assigned as follows:
//  processor_clock = clk_div4， which is 12.5 MHz
//  regfile_clock   = clk_div4， which is 12.5 MHz
//  dmem_clock      = clk_div2， which is 25 MHz
//  imem_clock      = base 50 MHz clock
// Ensures that memory and CPU operations stay synchronized but avoid race conditions.

// The skeleton instantiates four main modules:
//  imem: instruction memory, initialized using basic_test.mif
//  dmem:data memory, read/write controlled by processor
//  regfile: 32x32 register file for data storage
//  processor - the CPU that fetches, decodes, executes instructions, and interfaces with memory and regfile

// Each module is fully connected through address, data, and control signals,
// matching the processor specification. The processor drives control lines

// Issues
// freq_div_by2 and freq_div_by4 modules were write in 2 files
// Don't know if the crossover can be used.
// Time space between different divided clocks may cause mismatched waveforms
// System passes synthesis and basic testbench checks.
