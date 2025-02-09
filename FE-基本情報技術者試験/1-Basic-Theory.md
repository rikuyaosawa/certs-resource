# Basic Theory

Table of Contents

- [Basic Theory](#basic-theory)
  - [Data Unit](#data-unit)
  - [Number Systems](#number-systems)
    - [Decimal Types](#decimal-types)
    - [Radix Conversion and Digit Weight](#radix-conversion-and-digit-weight)
  - [Negative Binary](#negative-binary)
  - [Four Arithmetic Calculation of Binary Number](#four-arithmetic-calculation-of-binary-number)
  - [Shift Operations](#shift-operations)
  - [Venn Diagram](#venn-diagram)
  - [Logical Operators](#logical-operators)
  - [Truth Table](#truth-table)
  - [Logical Circuits](#logical-circuits)
    - [MIL-STD Logic Symbols](#mil-std-logic-symbols)

## Data Unit

At the smallest scale in the computer, information is stored as bits and bytes. A **bit** is atomic: the smallest unit of storage. A bit stores just a 0 or 1. One **byte** = collection of 8 bits.

A **bit pattern** is a sequence of binary digits (bits)—0s and 1s—that represents data in digital systems. Each bit in the pattern holds a value of either 0 (off) or 1 (on).

## Number Systems

- **Binary (バイナリ)**: A number system using only 0 and 1, representing data in computers.
- **Decimal (十進法)**: The standard number system using digits 0 to 9, commonly used in daily life.
- **Hexadecimal (十六進法)**: A compact number system using digits 0–9 and letters A–F, often used in computing to simplify binary representation.

### Decimal Types

- **Finite (Terminating) Decimal (有限小数):** A decimal that has a limited number of digits after the decimal point (e.g., **0.75**).
- **Infinite (Non-Terminating) Decimal (無限小数):** A decimal that continues endlessly without stopping (e.g., **π = 3.14159...**).
- **Recurring (Repeating) Decimal (循環小数):** A type of infinite decimal where a specific digit or group of digits repeats continuously (e.g., **0.333... = 0.\overline{3}**).

### Radix Conversion and Digit Weight

**Radix conversion (基数変換)** is the process of converting numbers from one base (radix) to another, such as from binary to decimal, or decimal to hexadecimal .

**Digit weight (桁の重み)** refers to the value assigned to a digit based on its position in a number, determined by the base (radix) of the number system. It is calculated as the base raised to the power of the digit's position index.

**Index (指数 or インデックス)** refers to the exponent used to indicate the power to which a number (base) is raised, especially in positional number systems. It can also refer to the position of a digit in a sequence, starting from the right (least significant digit) or left (most significant digit), depending on the context.

- Example (Exponent): In 23=823=8, the number 3 is the index (指数).
- Example (Position): In binary 1101, the rightmost digit (1) is at index 0, the next (0) at index 1, and so on.

#### From Binary to Decimal

1. **Write the binary number** and list the powers of 2 from right to left (starting from \( 2^0 \)).
2. **Multiply each binary digit** by the corresponding power of 2.

![Binary to decimal: multiply each binary digits](https://d138zd1ktt9iqe.cloudfront.net/media/seo_landing_files/binary-to-decimal-step-1-1622615448.png)

3. **Sum the results** to get the decimal equivalent.

![Binary to decimal: sum the results](https://d138zd1ktt9iqe.cloudfront.net/media/seo_landing_files/binary-to-decimal-step-2-1622615940.png)

> [Binary to Decimal ↗](https://www.cuemath.com/numbers/binary-to-decimal/)

> [!TIP]
> To calculate a negative exponents:
>
> - Convert the negative exponent to a positive one by taking the reciprocal.
> - Calculate the positive exponent.

#### From Hexadecimal to Decimal

1. **Write the Hexadecimal Number**

2. **Convert Hex Digits to Decimal**: Hexadecimal uses digits 0-9 and letters A-F. Each letter represents a number:

   - A = 10
   - B = 11
   - C = 12
   - D = 13
   - E = 14
   - F = 15

3. **Assign Powers of 16**: Start from the rightmost digit and assign powers of 16.

4. **Multiply Each Hex Digit by the Corresponding Power of 16**

5. **Sum the Results**
   Add all the results together:

<br />

![Hex to Decimal example](https://www.inchcalculator.com/wp-content/uploads/2021/09/how-to-convert-hex-to-decimal-thumb.png)

[Converting Hex to Decimal ↗](https://byjus.com/maths/hex-to-decimal/)

#### From Decimal to Binary

**1. Convert the Integer Part:**

- Divide the integer part of the decimal number by 2.
- Record the remainders.
- Continue dividing the quotient by 2 until the quotient is 0.
- The binary number is formed by reading the remainders in reverse order.

![From decimal to binary: integer](https://d138zd1ktt9iqe.cloudfront.net/media/seo_landing_files/decimal-to-binary-conversion-1623818593.png)

**2. Convert the Fractional Part:**

- Multiply the fractional part by 2.
- Record the integer part of the result as the first binary digit.
- Take the fractional part of the result and repeat the process until the fraction becomes 0 (or until you reach a sufficient precision).

[How to Convert Decimal to Binary? ↗](https://www.cuemath.com/numbers/decimal-to-binary/)

[Decimal to binary: fractions ↗](https://hyperskill.org/learn/step/11938)

#### From Decimal to Hexadecimal

**1. Convert the Integer Part:**

- Divide the integer part of the decimal number by 16.
- Record the remainders.
- Continue dividing the quotient by 16 until the quotient is 0.
- The hexadecimal number is formed by reading the remainders in reverse order. Hexadecimal uses digits 0-9 and letters A-F, where:
  - 10 = A, 11 = B, 12 = C, 13 = D, 14 = E, 15 = F.

**2. Convert the Fractional Part (if any):**

- Multiply the fractional part by 16.
- Record the integer part of the result as the first hex digit.
- Take the fractional part of the result and repeat the process until the fraction becomes 0 (or until you reach a sufficient precision).

#### N-ary System

An **N-ary system** (n 進数) is a number system that uses a base **N**, where **N** can be any integer greater than 1. The **N** represents the number of unique digits (including zero) used in the system. For example:

- **Binary (base-2)**: Uses 2 digits, 0 and 1.
- **Decimal (base-10)**: Uses 10 digits, 0 to 9.
- **Hexadecimal (base-16)**: Uses 16 digits, 0-9 and A-F.

**How to Use an N-ary System:**

1. **Digits in N-ary**:
   The number system will have **N** digits. For example:

   - In binary (base-2), the digits are: \( 0, 1 \)
   - In decimal (base-10), the digits are: \( 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 \)
   - In hexadecimal (base-16), the digits are: \( 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F \)

2. **Value Representation**:
   Each digit in an N-ary system represents a multiple of a power of **N**. The rightmost digit represents \( N^0 \), the second rightmost digit represents \( N^1 \), and so on.

3. **Converting between N-ary and Decimal**:
   - To convert an N-ary number to decimal, multiply each digit by the corresponding power of **N** and sum them up.
   - To convert a decimal number to an N-ary number, repeatedly divide the number by **N** and record the remainders.

## Negative Binary

There are several ways to represent negative values in the binary number system. Here are the most common methods:

**1. Sign-Magnitude (絶対値表現):**

- **Concept:** The simplest approach. The leftmost bit (most significant bit, MSB) is used as the sign bit: 0 for positive, 1 for negative. The remaining bits represent the magnitude (absolute value) of the number.
- **Example (8-bit):**
  - +5: 00000101
  - -5: 10000101
- **Advantages:** Easy to understand and implement.
- **Disadvantages:**
  - Two representations for zero (+0 and -0). This can complicate comparisons.
  - Addition and subtraction require special handling depending on the signs of the operands. It's not as straightforward as with other representations.

**2. One's Complement (1 の補数表現):**

- **Concept:** To represent a negative number, invert all the bits of the positive representation (change 0s to 1s and 1s to 0s).
- **Example (8-bit):**
  - +5: 00000101
  - -5: 11111010 (Invert all bits of +5)
- **Advantages:** Relatively simple to implement.
- **Disadvantages:**
  - Still has two representations for zero (+0 and -0).
  - Addition and subtraction still require some special handling, although it's slightly simpler than sign-magnitude.

**3. Two's Complement (2 の補数表現):**

- **Concept:** The most widely used method. To represent a negative number:
  1. Invert all the bits of the positive representation (like one's complement).
  2. Add 1 to the result.
- **Example (8-bit):**
  - +5: 00000101
  - -5: 11111011 (Invert all bits of +5, then add 1)
- **Advantages:**
  - Only one representation for zero.
  - Addition and subtraction are performed using the same logic for both positive and negative numbers. This simplifies hardware implementation significantly. This is the _main_ reason two's complement is so popular.
- **Disadvantages:** Slightly more complex to understand initially than sign-magnitude.

**Why Two's Complement is Preferred:**

Two's complement is the standard representation for integers in most modern computers because it greatly simplifies arithmetic operations. The same adder/subtractor circuit can be used for both signed and unsigned numbers, making hardware design much more efficient. The single representation of zero also simplifies comparisons.

## Four Arithmetic Calculation of Binary Number

**Binary Addition**

Binary addition follows similar rules to decimal addition, with a few key differences:

- **0 + 0 = 0**
- **0 + 1 = 1**
- **1 + 0 = 1**
- **1 + 1 = 10** (0 with a carry of 1)

**Here's how to add binary numbers:**

1. **Align the numbers:** Write the binary numbers vertically, aligning the rightmost bits.

2. **Add the bits:** Start from the rightmost bit (least significant bit) and add the corresponding bits in each column.

3. **Handle carries:** If the sum in a column is 2 (10 in binary), write down 0 and carry over 1 to the next column to the left. If the sum is 3 (11 in binary), write down 1 and carry over 1.

4. **Continue:** Repeat steps 2 and 3 for all columns, moving from right to left.

**Example:**

```
   1011 (11 in decimal)
+  0110 (6 in decimal)
-------
  10001 (17 in decimal)
```

**Binary Subtraction**

Binary subtraction can be done using two's complement, which simplifies the process:

1. **Find the two's complement:** To subtract a binary number (the subtrahend) from another (the minuend), find the two's complement of the subtrahend.

2. **Add the two's complement:** Add the two's complement of the subtrahend to the minuend.

3. **Discard the carry:** If there is a carry-out from the leftmost bit, discard it. The result is the difference between the two numbers.

**Example:**

```
   1011 (11 in decimal)
-  0110 (6 in decimal)
-------
```

**1. Find the two's complement of 0110:**

- Invert the bits: 1001
- Add 1: 1010

**2. Add the two's complement to 1011:**

```
   1011
+  1010
-------
  10101
```

**3. Discard the carry:**

- The result is 0101 (5 in decimal).

## Shift Operations

> [!IMPORTANT] MUST KNOW
>
> **Shift operations** (シフト演算) are fundamental bitwise operations that manipulate the bits of a binary number by moving them to the left or right. They are crucial for various tasks in computer science, from low-level hardware control to high-level algorithms. There are two main types of shift operations:

**1. Logical Shifts (論理シフト):**

- **Left Logical Shift:** Shifts all bits to the left. Zeros are filled in on the right.

  ```
  Original: 01101011
  Left Shift (1 bit): 11010110
  Left Shift (2 bits): 10101100
  ```

- **Right Logical Shift:** Shifts all bits to the right. Zeros are filled in on the left.

  ```
  Original: 10110110
  Right Shift (1 bit): 01011011
  Right Shift (2 bits): 00101101
  ```

![Logical Shift](https://open4tech.com/wp-content/uploads/2016/11/Logical_Shift.jpg)

**2. Arithmetic Shifts (算術シフト):**

- **Left Arithmetic Shift:** Behaves exactly like a left logical shift. Zeros are filled in on the right.

- **Right Arithmetic Shift:** Shifts all bits to the right. The _sign bit_ (the leftmost bit) is copied and filled in on the left. This preserves the sign of the number, which is essential for signed integer arithmetic.

  ```
  Original (negative): 10110110
  Right Shift (1 bit): 11011011  (Sign bit '1' is copied)
  Right Shift (2 bits): 11101101  (Sign bit '1' is copied)

  Original (positive): 01101011
  Right Shift (1 bit): 00110101  (Sign bit '0' is copied)
  Right Shift (2 bits): 00011010  (Sign bit '0' is copied)
  ```

![Arithmetic Shifts](https://open4tech.com/wp-content/uploads/2016/11/Arithmetic_Shift.jpg)

**Key Differences and Uses:**

- **Logical shifts** are typically used for unsigned integers or when you're working with data that doesn't represent numerical values (e.g., bit flags). They are often used for bit manipulation and masking.

- **Arithmetic shifts** are used for signed integers. The right arithmetic shift is particularly important because it preserves the sign of the number, which is crucial for correct arithmetic operations. Left arithmetic shift is the same as left logical shift.

**Relationship to Multiplication and Division:**

Left shifts are equivalent to multiplying by powers of 2. A left shift of _n_ bits is the same as multiplying by 2<sup>_n_</sup>.

Right logical shifts are equivalent to dividing by powers of 2 (with truncation). Right arithmetic shift is approximately equivalent to dividing by powers of 2, but it correctly handles negative numbers by preserving the sign.

**Example:**

```
1011 (11 in decimal)

Left Shift (1 bit): 10110 (22 in decimal)  (11 * 2 = 22)
Left Shift (2 bits): 101100 (44 in decimal) (11 * 4 = 44)

Right Logical Shift (1 bit): 0101 (5 in decimal) (11 / 2 = 5.5, truncated to 5)
Right Arithmetic Shift (1 bit): 1101 (-5 in decimal) (11 / 2 = 5.5, rounded to -6 if you are using two's complement)
```

<br />

> [!NOTE] Overflow in digital system
>
> Overflow in digital systems occurs when the result of an arithmetic operation exceeds the maximum value that can be represented with the available number of bits. It's a crucial concept to understand because it can lead to incorrect calculations and program errors.
>
> <img src="https://miro.medium.com/v2/resize:fit:1400/1*PQnjqDxwt976o0xp68G6qA.png" alt="Overflow" width="400"/>
>
> More on it: [Overflow Error](https://www.lenovo.com/in/en/glossary/overflow-error/)

## Venn Diagram

A **Venn diagram** (ベン図) is a visual tool used to show the relationships between different sets or groups of items. It uses **overlapping circles** to represent these sets, illustrating how they share common elements (intersections) or have distinct elements (differences).

**Symbols:**

| **Symbol** | **Meaning**   | **Description**                       |
| ---------- | ------------- | ------------------------------------- |
| ∪          | Union         | All elements from both sets           |
| ∩          | Intersection  | Elements common to both sets          |
| ∖ or ー    | Difference    | Elements in one set but not the other |
| A′ or Ac   | Complement    | Elements not in the set               |
| ⊆          | Subset        | All elements of A are in B            |
| ⊂          | Proper Subset | A is a subset of B but not equal      |
| ∅          | Empty Set     | A set with no elements                |

## Logical Operators

(論理演算子)

| **Operator** | **Symbol**    | **Meaning**                                                   |
| ------------ | ------------- | ------------------------------------------------------------- |
| **AND**      | ∧ or **&&**   | True if **both** conditions are true                          |
| **OR**       | ∨ or **\|\|** | True if **at least one** condition is true                    |
| **NOT**      | ¬ or **!**    | Inverts the truth value (True → False, False → True)          |
| **XOR**      | ⊕             | True if **only one** of the conditions is true (exclusive OR) |
| **NAND**     | ↑             | Opposite of AND; true unless both are true                    |
| **NOR**      | ↓             | Opposite of OR; true only if both are false                   |

## Truth Table

(真理値表)

1. **AND ( A ∧ B )** (論理積)

| **A** | **B** | **A AND B** |
| ----- | ----- | ----------- |
| 0     | 0     | 0           |
| 0     | 1     | 0           |
| 1     | 0     | 0           |
| 1     | 1     | 1           |

2. **OR ( A ∨ B )** (論理和)

| **A** | **B** | **A OR B** |
| ----- | ----- | ---------- |
| 0     | 0     | 0          |
| 0     | 1     | 1          |
| 1     | 0     | 1          |
| 1     | 1     | 1          |

3. **NOT ( ¬A )** (否定)

| **A** | **NOT A** |
| ----- | --------- |
| 0     | 1         |
| 1     | 0         |

4. **XOR ( A ⊕ B )** (排他的論理和)

| **A** | **B** | **A XOR B** |
| ----- | ----- | ----------- |
| 0     | 0     | 0           |
| 0     | 1     | 1           |
| 1     | 0     | 1           |
| 1     | 1     | 0           |

5. **NAND ( A ↑ B )** (否定論理積)

| **A** | **B** | **A NAND B** |
| ----- | ----- | ------------ |
| 0     | 0     | 1            |
| 0     | 1     | 1            |
| 1     | 0     | 1            |
| 1     | 1     | 0            |

6. **NOR ( A ↓ B )** (否定論理和)

| **A** | **B** | **A NOR B** |
| ----- | ----- | ----------- |
| 0     | 0     | 1           |
| 0     | 1     | 0           |
| 1     | 0     | 0           |
| 1     | 1     | 0           |

**Logical Operators Precedence**

Order from Highest to Lowest:

1. **NOT**
2. **AND**
3. **OR**
4. **XOR**

## Logical Circuits

(論理回路)

A **logical circuit** is a network of interconnected **logic gates** that process binary inputs (0 and 1) to produce specific outputs based on **Boolean algebra**. These circuits form the foundation of **digital electronics**, including computers, calculators, and more.

- **Inputs**: Binary signals (0 = LOW, 1 = HIGH).
- **Outputs**: Resulting binary signals after processing.
- **Components**: Built using **logic gates** like AND, OR, NOT, NAND, NOR, XOR, and XNOR.

### MIL-STD Logic Symbols

The **MIL-STD** (MIL 記号) symbols are standardized by the **U.S. Department of Defense** for use in military and aerospace electronic schematics. These symbols are more **abstract** and less graphical than the conventional **ANSI** or **IEC** symbols, focusing on clarity in complex circuit diagrams.

![Basic logic gates figure](https://www.microcontrollertips.com/wp-content/uploads/2022/05/What-are-basic-logic-gates-figure-1.jpg)
