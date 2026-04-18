# 6-Bit Signed/Unsigned Comparator

This project implements a **6-bit comparator** in **Verilog** for both **signed** and **unsigned** numbers.

## Features
- Compares two 6-bit inputs `A` and `B`
- Supports:
  - **Unsigned comparison**
  - **Signed comparison (2’s complement)**
- Selection input `S` chooses the comparison mode
- Outputs:
  - `Equal`
  - `Greater`
  - `Smaller`
- Includes synchronous input/output registers using `clk`
- Includes a **testbench** to verify all possible input combinations

## Inputs and Outputs

### Inputs
- `A[5:0]`: first number
- `B[5:0]`: second number
- `S`: mode select  
  - `0` → unsigned
  - `1` → signed
- `clk`: clock signal

### Outputs
- `Equal`: `1` if `A == B`
- `Greater`: `1` if `A > B`
- `Smaller`: `1` if `A < B`

## Modules
- `comparator` → top structural design
- `UnsignComparator` → unsigned comparison
- `SignComparator` → signed comparison
- `DFF_input` → input registers
- `DFF_output` → output registers
- `Comparator_Behavioural` → behavioral reference model
- `comparator_tb` → testbench

## Verification
The project verifies the structural design by comparing it against a behavioral model for all possible combinations of inputs. 

## Course
ENCS3310 – Advanced Digital Design. The project specification requires a structural comparator for 6-bit signed and unsigned numbers, with synchronous registers and full verification. 

## Author
Khaled
