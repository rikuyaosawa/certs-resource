# Basic Theory (1)

Table of Contents

- [Basic Theory (1)](#basic-theory-1)
  - [Data Unit](#data-unit)
    - [Bit and Byte](#bit-and-byte)
    - [Number Systems](#number-systems)
    - [Decimal Types](#decimal-types)
    - [Radix Conversion and Digit Weight](#radix-conversion-and-digit-weight)
    - [From Binary to Decimal](#from-binary-to-decimal)
    - [From Hexadecimal to Decimal](#from-hexadecimal-to-decimal)
    - [From Decimal to Binary](#from-decimal-to-binary)
    - [From Decimal to Hexadecimal](#from-decimal-to-hexadecimal)
  - [N-ary System](#n-ary-system)

## Data Unit

### Bit and Byte

At the smallest scale in the computer, information is stored as bits and bytes. A **bit** is atomic: the smallest unit of storage. A bit stores just a 0 or 1. One **byte** = collection of 8 bits.

A **bit pattern** is a sequence of binary digits (bits)—0s and 1s—that represents data in digital systems. Each bit in the pattern holds a value of either 0 (off) or 1 (on).

### Number Systems

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

### From Binary to Decimal

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

### From Hexadecimal to Decimal

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

### From Decimal to Binary

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

### From Decimal to Hexadecimal

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

## N-ary System

An **N-ary system** is a number system that uses a base **N**, where **N** can be any integer greater than 1. The **N** represents the number of unique digits (including zero) used in the system. For example:

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
