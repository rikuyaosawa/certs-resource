# Computer Components

Table of Contents

- [Computer Components](#computer-components)
  - [Overview](#overview)
  - [CPU (Processor)](#cpu-processor)
    - [Clock Frequency](#clock-frequency)
    - [MIPS](#mips)
    - [Core](#core)
  - [CPU Process Flow](#cpu-process-flow)
    - [RAM](#ram)
    - [Register](#register)
    - [Memory Address Modes](#memory-address-modes)

## Overview

This chapter will cover important computer hardware components such as:

- **CPU (Processor)**: types, structure, and how it works.
- **Memory**: types and features, and access method.
- **I/O devices**: types and features, input interfaces.

![CPU architecture](https://computersciencewiki.org/images/1/1a/Cpu_diagram.png)

## CPU (Processor)

**The Central Processing Unit (中央処理装置) is the brain of the computer.**

It is is the primary component of a computer that acts as its “control center.” The CPU, also referred to as the “central” or “main” processor (プロセッサ), is a complex set of electronic circuitry that runs the machine's operating system and apps.

A CPU's capability is mainly evaluated by the following three points:

1. Clock frequency (クロック周波数)
2. MIPS
3. Core (コア)

### Clock Frequency

**CPU clock frequency** (クロック周波数), also known as clock speed, is the number of cycles a CPU performs in one second. It's a key specification for a CPU and is usually measured in gigahertz (GHz).

> [!IMPORTANT]
>
> **Formula for IPS (Instructions Per Second)**
>
> The formula to calculate CPU instructions per second (IPS) is:
>
> ```
> IPS = Clock Speed (Hz) / Cycles per Instruction (CPI)
> ```
>
> where clock speed is the CPU's operating frequency in Hertz and CPI represents the average number of clock cycles needed to execute a single instruction.

### MIPS

**Million instructions per second (MIPS)** is an approximate measure of a computer's raw processing power.

> [!IMPORTANT]
>
> **Formula for MIPS**
>
> ```
> MIPS = IPS x 1,000,000.
> ```

### Core

A CPU core is a single processing unit within the CPU that can execute instructions. The more cores a CPU has, the more tasks it can handle simultaneously.

A multi-core CPU, or multi-core processor, is a computer processor with multiple cores on a single chip. Each core can run instructions independently, which allows for faster processing and multitasking.

## CPU Process Flow

In order to understand how CPU process works, we need to understand what main memory, or Random Access Memory (RAM) is.

### RAM

**Random access memory (RAM)** (主記憶装置) is a type of short-term memory used by computers to store **data or instructions** which it needs to retrieve quickly.

### Register

**A processor register** (レジスタ) is a quickly accessible location available to a computer's processor. Registers usually consist of a small amount of fast storage.

Depending on the CPUs architecture and design, the type and number of registers can vary. Common types of registers found in a CPU may include:

- **Program Counter (PC)** (プログラムカウンタ): keeps track of the memory address of the next instruction to be fetched and executed.

- **Instruction Register (IR)** (命令レジスタ): The Instruction Register holds the currently fetched instruction being executed.

- **General-Purpose Registers (R0, R1, R2…)** (汎用レジスタ): These registers are used to store data during calculations and data manipulation. They can be accessed and utilized by the programmer for various purposes.

### Memory Address Modes

There are many ways to locate data and instructions in primary memory and these methods are called **memory address modes** (アドレス指定方式).

Memory address modes determine the method used within the program to access data either from the Cache or the RAM.
In this challenge we will focus on four different memory address modes:

- Immediate Access
- Direct Access
