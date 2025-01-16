
# Nand2Tetris-Augmented ALU

## Description

In this project, we aim to enhance the basic ALU (Arithmetic Logic Unit) created in the Nand2Tetris course. The enhanced ALU will perform more arithmetic operations and detect overflows while integrating several combinational logic circuits.

The core of the ALU consists of:
- Two 16-bit inputs: `x` and `y`
- One 16-bit output: `out`
- One 1-bit overflow flag: `of`

### Features:

The ALU will be able to perform the following operations, controlled by the corresponding control inputs:

---

### 1. **Bit-wise Logic Operations** (6 marks)
- **Operations:** 
  - `x And y`
  - `x Or y`
  - `x Xor y`
  
- **Overflow Case:** No overflow occurs, and `of` should always be 0.

---

### 2. **Shift Operations** (4 marks)
- **Operations:**
  - **Left shift:** `x << 1`
    - Example: `1100, 0000, 0000, 1111 << 1` becomes `1000, 0000, 0001, 1110`
  
  - **Right shift:** `x >> 1`
    - Example: `1100, 0000, 0000, 1111 >> 1` becomes `0110, 0000, 0000, 0111`

- **Overflow Case:** No overflow occurs, and `of` should always be 0.

---

### 3. **Arithmetic Operations** (4 marks)
- **Operations:**
  - `x + y`
  - `x − y`
  
- **Overflow Handling:** If overflow occurs, set `of` to 1 and `out` to −1.

---

### 4. **Comparison Operations** (4 marks)
- **Operations:**
  - `x > y`
  - `x == y`
  
- **Output:** The comparison result should be stored in `out[0]`. The remaining bits (`out[1..15]`) should be set to 0.
  
- **Overflow Case:** No overflow occurs, and `of` should always be 0.

---

### 5. **Multiplication Operation** (2 marks)
- **Operation:** `x * y`
  
- **Overflow Handling:** If overflow occurs or inputs are out of the domain, set `of` to 1 and `out` to −1.

---

### 6. **Division Operation** (1 mark)
- **Operation:** `x ÷ y`
  
- **Rounding:** Fraction results should round down to the nearest integer. For example, `7/3 = 2`, `7/−3 = −3`.
  
- **Overflow Handling:** For overflow cases or inputs outside the domain, set `of` to 1 and `out` to −1.

---

## Project Structure

The project includes:
- **ALU chip designs:** Implementation in hardware description language (HDL).
- **Test scripts:** Test cases to verify the functionality of the ALU's operations.
- **Simulation files:** Files to simulate the ALU chip and verify its behavior with various inputs.

---

## Usage

1. Clone the repository to your local machine.
2. Use the provided HDL files with the Nand2Tetris tools to simulate the ALU chip.
3. Run the tests to verify that each operation works as expected.

```bash
git clone https://github.com/yourusername/Nand2Tetris-Augmented-ALU.git
cd Nand2Tetris-Augmented-ALU
# Run simulations or tests using the Nand2Tetris tools
```

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- This project builds upon the work done in the Nand2Tetris course, which introduces fundamental concepts of computer architecture and hardware design.
