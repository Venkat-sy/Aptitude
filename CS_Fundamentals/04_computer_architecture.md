# Computer Architecture (COA)

## Part 1: Quick Short Notes (Fundamentals)

### 1. Computer Architecture Fundamentals
*   **Architecture vs. Organization:** Architecture refers to the attributes of a system visible to a programmer (e.g., instruction set, number of bits). Organization refers to the operational units and their interconnections that realize the architecture (e.g., control signals, memory technology).
*   **Von Neumann Architecture:** A design where data and instructions are stored in the same memory. Follows the fetch-decode-execute cycle.
*   **Harvard Architecture:** A design with physically separate storage and signal pathways for instructions and data.

### 2. Number Systems
*   **Binary (Base 2):** Digits 0, 1.
*   **Octal (Base 8):** Digits 0-7. Each octal digit represents 3 binary bits.
*   **Hexadecimal (Base 16):** Digits 0-9, A-F. Each hex digit represents 4 binary bits. Useful for compacting long binary strings.
*   **Complements:**
    *   *1's Complement:* Invert all bits (0s to 1s, 1s to 0s).
    *   *2's Complement:* 1's Complement + 1. Widely used for representing negative numbers in computers because it simplifies subtraction to addition.

### 3. Logic Gates
*   **Basic Gates:** AND, OR, NOT.
*   **Universal Gates:** NAND, NOR. They are "universal" because any boolean function can be implemented using only NAND or only NOR gates.
*   **Derived Gates:** XOR (Exclusive-OR), XNOR (Exclusive-NOR).

### 4. CPU Organization
*   **ALU (Arithmetic Logic Unit):** Performs arithmetic and bitwise logical operations.
*   **CU (Control Unit):** Directs the operation of the processor. It extracts instructions from memory, decodes them, and executes them by sending control signals to the ALU and memory.
*   **Registers:** Small, fast memory locations inside the CPU.
    *   *PC (Program Counter):* Holds the address of the next instruction to be executed.
    *   *IR (Instruction Register):* Holds the instruction currently being executed.
    *   *MAR (Memory Address Register):* Holds the address of the memory location to be accessed.
    *   *MDR (Memory Data Register):* Holds data being transferred to or from memory.

### 5. Addressing Modes
*   **Definition:** The way the operands are chosen during program execution.
*   **Immediate:** The operand is specified directly in the instruction. (e.g., ADD 5)
*   **Direct:** The address of the operand is explicitly specified in the instruction.
*   **Indirect:** The instruction specifies a register or memory location that holds the address of the operand.
*   **Register:** The operand is held in a CPU register.
*   **Index / Base Register:** Used for accessing arrays or relocating programs.

### 6. Memory Hierarchy
*   **Goal:** To obtain the highest possible average access speed while minimizing the total cost of the memory system.
*   **Hierarchy (Fastest/Smallest to Slowest/Largest):** CPU Registers $\rightarrow$ Cache Memory $\rightarrow$ Main Memory (RAM) $\rightarrow$ Secondary Storage (Magnetic Disk/SSD) $\rightarrow$ Tertiary Storage (Tape).
*   **Locality of Reference:** The principle that cache memory relies on.
    *   *Spatial Locality:* If a memory location is accessed, nearby locations are likely to be accessed soon (e.g., arrays).
    *   *Temporal Locality:* If a memory location is accessed, it is likely to be accessed again soon (e.g., loops).

### 7. Cache Memory
*   **Function:** A small, fast memory placed between the CPU and main memory to hold frequently requested data and instructions.
*   **Mapping Techniques:** How main memory blocks are assigned to cache lines.
    *   *Direct Mapping:* Each block maps to exactly one cache line.
    *   *Associative Mapping:* A block can map to any cache line.
    *   *Set-Associative Mapping:* A compromise; a block maps to any line within a specific set.
*   **Cache Hit/Miss:** A 'Hit' is when data is found in the cache; a 'Miss' is when it is not, requiring a fetch from main memory.

### 8. Interrupts & DMA
*   **Interrupt:** A signal sent to the CPU indicating an event that needs immediate attention. The CPU pauses current execution, saves its state, and runs an Interrupt Service Routine (ISR).
*   **DMA (Direct Memory Access):** A hardware mechanism that allows peripheral devices (like disk controllers) to transfer data directly to/from main memory without CPU involvement, freeing the CPU for other tasks.

---

## Part 2: Placement-Related MCQs

1. Which CPU register holds the address of the next instruction to be fetched from memory?

A) Instruction Register (IR)

B) Memory Address Register (MAR)

C) Program Counter (PC)

D) Accumulator (ACC)

**Answer:** Option **C**

**Explanation:**

The Program Counter (PC) keeps track of the execution sequence. It holds the memory address of the next instruction that needs to be fetched and executed. Once the instruction is fetched, the PC is automatically incremented.

---

2. Which architecture physically separates the memory for instructions and data?

A) Von Neumann Architecture

B) Harvard Architecture

C) Turing Architecture

D) RISC Architecture

**Answer:** Option **B**

**Explanation:**

The Harvard architecture uses physically separate storage and signal pathways for instructions and data. This allows the CPU to fetch an instruction and read/write data simultaneously, unlike the Von Neumann architecture where they share a single bus.

---

3. Which of the following gates are known as Universal Gates?

A) AND, OR

B) XOR, XNOR

C) NAND, NOR

D) NOT, AND

**Answer:** Option **C**

**Explanation:**

NAND and NOR gates are called universal gates because any boolean expression or basic logic gate (AND, OR, NOT) can be constructed using only NAND gates or only NOR gates.

---

4. In which addressing mode is the operand value explicitly specified within the instruction itself?

A) Direct Addressing Mode

B) Indirect Addressing Mode

C) Register Addressing Mode

D) Immediate Addressing Mode

**Answer:** Option **D**

**Explanation:**

In Immediate addressing mode, the actual data to be operated on is embedded directly into the instruction operand field (e.g., `ADD #5` adds the literal value 5).

---

5. Which memory principle states that if a memory location is accessed, recently accessed locations are likely to be accessed again in the near future?

A) Spatial Locality

B) Temporal Locality

C) Cache Coherence

D) Virtual Memory

**Answer:** Option **B**

**Explanation:**

Temporal locality refers to the tendency of a processor to access the same memory locations repeatedly within a short period (like variables in a loop). Spatial locality refers to accessing memory locations that are physically close to each other (like elements in an array).

---

6. What is the 2's complement of the binary number `0101`?

A) `1010`

B) `1011`

C) `1100`

D) `0110`

**Answer:** Option **B**

**Explanation:**

To find the 2's complement:
1) Find the 1's complement by inverting the bits: `0101` becomes `1010`.
2) Add 1 to the 1's complement: `1010 + 1 = 1011`.

---

7. Which mechanism allows I/O devices to transfer data directly to main memory without the intervention of the CPU?

A) Polling

B) Interrupts

C) Direct Memory Access (DMA)

D) Memory-Mapped I/O

**Answer:** Option **C**

**Explanation:**

Direct Memory Access (DMA) is a feature that allows certain hardware subsystems to access main system memory independently of the central processing unit (CPU). This greatly speeds up memory operations bypassing the CPU.

---

8. In a memory hierarchy, which memory type is the fastest and closest to the CPU execution unit?

A) Cache Memory

B) Main Memory (RAM)

C) CPU Registers

D) Solid State Drive (SSD)

**Answer:** Option **C**

**Explanation:**

CPU Registers are built directly into the processor chip and operate at the same speed as the processor itself, making them the fastest but smallest form of memory in the hierarchy.

---

9. Which cache mapping technique allows a main memory block to be loaded into any line of the cache?

A) Direct Mapping

B) Set-Associative Mapping

C) Fully Associative Mapping

D) Indexed Mapping

**Answer:** Option **C**

**Explanation:**

In Fully Associative mapping, a block of main memory can map to any free cache line. This provides the most flexibility and reduces conflict misses but requires complex hardware to search all cache lines simultaneously.

---

10. What does the Control Unit (CU) of a processor do?

A) Performs arithmetic operations.

B) Generates timing and control signals.

C) Stores frequently used data.

D) Connects the computer to a network.

**Answer:** Option **B**

**Explanation:**

The Control Unit directs the operation of the processor. It tells the computer's memory, arithmetic and logic unit, and input and output devices how to respond to the instructions sent to the processor by generating the necessary control signals.

---

11. A Pipeline is used in processors to:

A) Increase memory capacity

B) Decrease the clock speed

C) Improve overall instruction throughput

D) Reduce power consumption

**Answer:** Option **C**

**Explanation:**

Pipelining is an implementation technique where multiple instructions are overlapped in execution. The computer pipeline is divided into stages, and each stage completes a part of an instruction. This increases the overall throughput of instructions per clock cycle.

---

12. What is a "Cache Miss"?

A) When data requested by the CPU is found in the cache.

B) When data requested by the CPU is not found in the cache and must be fetched from main memory.

C) When the cache memory fails hardware diagnostics.

D) When the cache memory is entirely full.

**Answer:** Option **B**

**Explanation:**

A cache miss occurs when the CPU attempts to access data in the cache memory but does not find it there. It then must go to the slower main memory to retrieve the required data, causing a delay.

---

13. In boolean algebra, the expression `A + A'B` simplifies to:

A) `A`

B) `B`

C) `A + B`

D) `AB`

**Answer:** Option **C**

**Explanation:**

Using the distributive law of boolean algebra, `A + A'B` can be factored.
`A + A'B = (A + A')(A + B)`
Since `A + A' = 1`, the expression simplifies to `1 * (A + B) = A + B`.

---

14. What does RISC stand for in computer architecture?

A) Rapid Instruction Set Computer

B) Reduced Instruction Set Computer

C) Reliable Instruction Set Computer

D) Random Instruction Set Computer

**Answer:** Option **B**

**Explanation:**

RISC stands for Reduced Instruction Set Computer. It is a CPU design strategy based on the insight that a simplified, smaller set of instructions provides higher performance when combined with a microprocessor architecture capable of executing those instructions using fewer microprocessor cycles per instruction.

---

15. An interrupt that cannot be ignored by the processor is called a:

A) Maskable Interrupt

B) Non-Maskable Interrupt (NMI)

C) Vectored Interrupt

D) Software Interrupt

**Answer:** Option **B**

**Explanation:**

A Non-Maskable Interrupt (NMI) is a hardware interrupt that standard interrupt-masking techniques in the system cannot ignore. It typically signals attention for non-recoverable hardware errors.

---

16. What is the decimal equivalent of the binary number `1101`?

A) 11

B) 12

C) 13

D) 15

**Answer:** Option **C**

**Explanation:**

To convert `1101` from binary to decimal:
$(1 \times 2^3) + (1 \times 2^2) + (0 \times 2^1) + (1 \times 2^0)$
$= 8 + 4 + 0 + 1 = 13$.

---

17. Which logic gate produces a HIGH output (1) only when all its inputs are HIGH (1)?

A) OR Gate

B) AND Gate

C) XOR Gate

D) NOR Gate

**Answer:** Option **B**

**Explanation:**

The AND gate is a basic digital logic gate that implements logical conjunction. A HIGH output (1) results only if all the inputs to the AND gate are HIGH (1).

---

18. In Indirect Addressing Mode, the operand address part of the instruction contains:

A) The actual data value.

B) The address of the data in memory.

C) The address of a memory location or register that contains the address of the data.

D) The base address of an array.

**Answer:** Option **C**

**Explanation:**

In indirect addressing, the instruction specifies a location (either in memory or a register) whose contents are the *actual* address of the operand in memory, requiring an extra memory access to fetch the final data.

---

19. Which component acts as a temporary high-speed holding area for the results of ALU operations?

A) Accumulator

B) Memory Address Register

C) Instruction Register

D) Cache

**Answer:** Option **A**

**Explanation:**

The accumulator is a register in which intermediate arithmetic and logic results are stored. Without an accumulator, it would be necessary to write the result of each calculation to main memory, which is much slower.

---

20. A 32-bit processor can address a maximum theoretical memory size of:

A) 2 GB

B) 4 GB

C) 8 GB

D) 16 GB

**Answer:** Option **B**

**Explanation:**

A 32-bit processor uses 32 bits to represent a memory address. The total number of unique addresses it can represent is $2^{32}$. $2^{32}$ bytes equals exactly 4 Gigabytes (GB).
