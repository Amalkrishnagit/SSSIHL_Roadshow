### Introduction :

In VLSI (Very-Large-Scale Integration) design, **EDI** (Electronic Design Interchange) refers to the exchange and integration of design data across different tools and stages of the design process. It ensures smooth communication between various tools like synthesis, simulation, layout, and verification, promoting efficient data sharing and reducing errors.

**Key Points:**
1. **Tool Integration**: EDI facilitates data exchange between different Electronic Design Automation (EDA) tools (e.g., Cadence, Synopsys, Mentor Graphics).
2. **Standard Formats**: EDI relies on standardized formats like **GDSII**, **LEF/DEF**, **Verilog/VHDL**, and **SPICE** to ensure compatibility across tools and stages.
3. **Verification and Collaboration**: EDI enables seamless verification and collaboration between teams working on different aspects of the design.
4. **Manufacturing Data**: It ensures accurate data exchange for chip fabrication, using formats like **GDSII** and **OASIS** for photomask generation.
5. **Supply Chain Integration**: EDI also supports data exchange with suppliers, streamlining inventory and component management.

**Benefits:**
- **Efficiency**: Automates data exchange, speeding up the design process.
- **Collaboration**: Facilitates team collaboration across locations.
- **Data Integrity**: Ensures accurate, consistent design data.

**Challenges:**
- **Complexity**: Integration of diverse tools can be difficult.
- **Standardization**: Ensuring full interoperability between different EDI standards can be challenging.

Overall, EDI in VLSI design enhances the design flow, ensuring consistency and collaboration across different teams and stages.

**POINTS TO NOTE**

_password :vsdiat

changing to risc-v commands(tamil to marathi)

PLL-High clock speeds

vlsisystemdesign.com

Foundry IP's-intellectual property

Why RISC (Architecture)file?

ARM Architecture-mobile phones

opensource versus proprietary

flip flops-registers

chip tapeout

firmware download

RVL-register transfer level-similar to c language converting to and other gates

welcome to linux - need a lot of focus to the atmost level

softcopy of RTL is ready and called

we have stick to one of the foundry-here skywater-minessota-sky130A-factory skywater-130 nanometers.

number of cells-4 billion gates-for processors-GPU

FPGA-BURNS PROGRAMME AND HARDWARE.

CLOCK SHOLUD REACH AT ALL END POINTS AT THE SAME TIME.

flipflop-clocks

routing

skew ?

GDS2(ii)-graphic database ii in VLSI-graphical dtatabase information interchange.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### From code to chip
**Step 1:**
A virtual environment was loaded and a terminal was opened.
![1](https://github.com/user-attachments/assets/b916021f-4ede-486a-8ca5-85ce0cdac1af)

**Step 2:**

The following sample code was saved in the directory,

#include<stdio.h>

int main(){ 

    int sum = 0, i, n; 
    printf("Enter the value of n = "); 
    scanf("%d",&n); 
    for(i = 1;i <= n;i++)
    {
    sum = sum + i;
    } 
    printf("The Sum of numbers from 1 to %d is %d\n",n,sum); 
    return 0; 
}

The command `sudo apt install gedit` is used to install **gedit**, which is a popular text editor in Linux, typically found on **Ubuntu** and other Debian-based distributions.

### Explanation:
- `sudo`: Runs the command with administrative (root) privileges.
- `apt`: The package manager used to install, update, or remove software in Debian-based systems.
- `install`: The command to install a package.
- `gedit`: The name of the text editor package.

### Usage:
1. Open your terminal.
2. Run the following command to install **gedit**:
   ```bash
   sudo apt install gedit
   ```
3. Enter your password when prompted.
4. After installation, you can open **gedit** by typing `gedit` in the terminal or finding it in your applications menu.

**gedit** is a lightweight, user-friendly text editor that supports syntax highlighting for various programming languages, making it a good choice for editing code and general text.

![2](https://github.com/user-attachments/assets/21eb5996-823c-4d3a-9b26-eda6a0cb5e92)

**Step 3:**
The command `./a.out` is used to run an executable file named `a.out` in a Unix-like system (e.g., Linux or macOS) from the terminal.

### Explanation:
- **`./`**: Specifies the current directory. In Unix-like systems, the `./` prefix is used to indicate that the file is located in the current directory (since, by default, the current directory is not included in the system's `PATH`).
- **`a.out`**: The default name for the executable file generated by a compiler, like GCC, when no output filename is specified.

### Usage:
1. **Compiling a Program**: When you compile a program (for example, using GCC), the default output is usually named `a.out` unless you specify a different filename using the `-o` flag:
   ```bash
   gcc myprogram.c  # This creates a.out by default
   ```
2. **Running the Executable**: To run the compiled program, you use:
   ```bash
   ./a.out
   ```

### Example Workflow:
1. **Compile** a C program:
   ```bash
   gcc myprogram.c
   ```
   This will create an executable file named `a.out`.

2. **Run** the executable:
   ```bash
   ./a.out
   ```
   This executes the compiled program.

### Note:
If you try to run `a.out` without the `./` prefix, it will not work unless `.` (the current directory) is included in your system's `PATH`.

![3](https://github.com/user-attachments/assets/781d6443-ebe7-4cbd-9161-403fb1ba68f1)

**GCC** (GNU Compiler Collection) is an open-source set of compilers that supports multiple programming languages, including **C**, **C++**, **Fortran**, **Go**, and others. It is widely used for compiling code into executable programs.

### Key Features:
- **Languages Supported**: C, C++, Fortran, Ada, Go, and more.
- **Cross-Platform**: Works on Linux, macOS, and Windows.
- **Optimizations**: Offers powerful optimizations for performance.
- **Open-Source**: Free to use, modify, and distribute under the GPL license.

### Benefits:
- **Portability**: Supports multiple architectures and platforms.
- **Efficiency**: Produces highly optimized code.
- **Extensibility**: Can be customized and extended.

In summary, GCC is a widely used, powerful, and flexible compiler for software development and embedded systems.

**Step 4:**

riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o hello.o hello.c

The command:

```bash
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o hello.o hello.c
```

is used to **compile** a C program (`hello.c`) for the **RISC-V** architecture, targeting a 64-bit processor with a specific ABI (Application Binary Interface) and instruction set. Here's a breakdown of the components:

### Breakdown of the command:

1. **`riscv64-unknown-elf-gcc`**:
   - This is the **RISC-V 64-bit GCC compiler**. It is used to compile code for the **RISC-V architecture** (specifically, the 64-bit variant).
   - **`unknown-elf`** indicates that the target system is a generic embedded system, without specifying a particular OS (this is common in bare-metal development).

2. **`-O1`**:
   - This option enables **optimizations** at level 1. It's a moderate optimization level, balancing between compilation time and performance.
   - Higher optimization levels like `-O2` or `-O3` could result in better performance but longer compile times.

3. **`-mabi=lp64`**:
   - This specifies the **ABI (Application Binary Interface)** for the target system.
   - `lp64` means:
     - **Long integers** (`long`) are 64-bit.
     - **Pointers** are 64-bit.
     - **`long long`** integers are also 64-bit.
   - It's a common ABI used for 64-bit systems.

4. **`-march=rv64i`**:
   - Specifies the **RISC-V architecture** and instruction set.
   - `rv64i` refers to:
     - **RISC-V 64-bit architecture** (`rv64`).
     - **Base integer instruction set** (`i`), which includes the basic instructions.
   - You can use other options for different RISC-V versions, such as `rv32i` for 32-bit.

5. **`-o hello.o`**:
   - This specifies the **output file**. Instead of generating a default output file (like `a.out`), the compiled object file will be named `hello.o`. This is the object file generated after compiling the source code, which is used for linking later to create an executable.

6. **`hello.c`**:
   - The **source code file** written in C that you want to compile.

### What this command does:
- Compiles the **C source file** `hello.c` for a **64-bit RISC-V processor** with the `rv64i` instruction set and the `lp64` ABI.
- The resulting output is an **object file** (`hello.o`), which is typically used in the next step of the build process (linking) to create a final executable.

### Common Use Case:
This command is useful for developing software for RISC-V based embedded systems or bare-metal environments where no operating system is running, or when targeting a specific architecture variant of the RISC-V instruction set.

### Example:
To compile and link a simple program for RISC-V:

1. **Compile** the C code:
   ```bash
   riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o hello.o hello.c
   ```

2. **Link** the object file to create an executable (e.g., `hello.elf`):
   ```bash
   riscv64-unknown-elf-gcc -o hello.elf hello.o
   ```

3. **Run** the program on a RISC-V emulator or actual hardware.

   
![4](https://github.com/user-attachments/assets/e0503bd3-6443-4e27-934a-165cb0a72fa8)

**Step 5:**

riscv64-unknown-elf-objdump -d hello.o

The command:

```bash
riscv64-unknown-elf-objdump -d hello.o
```

is used to disassemble the object file (`hello.o`) generated for a RISC-V 64-bit target architecture. Here's what each part of the command does:

### Breakdown of the command:

1. **`riscv64-unknown-elf-objdump`**:
   - This is the **objdump** utility specifically built for the **RISC-V 64-bit architecture**. 
   - **`unknown-elf`** indicates it is targeting a generic embedded system without a specific operating system.

2. **`-d`**:
   - This flag tells **objdump** to **disassemble** the object file, which means it will show the assembly code corresponding to the machine instructions in the object file.

3. **`hello.o`**:
   - This is the **object file** generated earlier from the source code (`hello.c`). The `.o` file contains machine code, symbols, and other information but isn't yet a full executable.

### What the command does:
- **Disassembly**: The command disassembles the `hello.o` object file, converting the raw machine code into a human-readable **assembly language** format.
  
  The output typically includes:
   - The **addresses** of the instructions.
   - The **machine code** (in hexadecimal).
   - The **disassembled assembly instructions** that correspond to the machine code.

### Example Output (simplified):
The output would look something like this:

```assembly
hello.o:     file format elf64-riscv

Disassembly of section .text:

0000000000000000 <_start>:
   0:   00000073                lui a5,0x0
   4:   00008067                jalr zero,a5,0
```

In this example:
- The first column shows the memory address of each instruction.
- The second column shows the **machine code** in hexadecimal.
- The third column shows the corresponding **disassembled assembly instruction**.

### Use Cases:
- **Debugging**: You can inspect the generated assembly to understand how your C code is translated into machine code.
- **Optimization**: Review the assembly output to spot areas where you might optimize performance or fix issues.
- **Reverse Engineering**: Examine the object file when you don't have access to the source code to understand what the program is doing.

In summary, `riscv64-unknown-elf-objdump -d hello.o` disassembles the object file `hello.o` for RISC-V and outputs the assembly code, allowing you to inspect the low-level details of your compiled program.
![5](https://github.com/user-attachments/assets/3894c449-40ad-40b7-8ac4-c7e885e1adf6)

**Step 6:** 

### Change directory to openlane flow directory

![6](https://github.com/user-attachments/assets/4bfbac96-eb21-42a3-9bb4-e036a869916c)

**Commands used:**cd Desktop/work/tools/openlane_working_dir/openlane

**Step7:** Execute the following commands one by one

**Commands used :**

"docker"

"./flow.tcl -interactive"

"package require openlane 0.9"

"prep -design picorv32a"

"run_synthesis"

"run_floorplan"

Note: Consult the below images for clarity

![7](https://github.com/user-attachments/assets/b3e72ea9-2758-4857-b006-b42b47173456)


![8](https://github.com/user-attachments/assets/1fad969c-99d9-4929-a33e-8c7429d60698)


![9 0](https://github.com/user-attachments/assets/897144f9-ad79-4474-bb56-c7254621cfce)


![9](https://github.com/user-attachments/assets/7315abe3-c74c-4b9b-92ed-2741b9328fc6)


![10](https://github.com/user-attachments/assets/ac112113-e225-49af-ab2a-8468aabea9cd)


![11](https://github.com/user-attachments/assets/94e44717-645f-4414-8b95-bb5d168ff0ce)

**Step 8:** opening floorplan image

**Command used:**
"eog designs/picorv32a/runs/13-12_07-00/results/floorplan/picorva32a.floorplan.def.png"

![12](https://github.com/user-attachments/assets/e04b1bd3-c841-48b8-958a-af999f6298d1)

**Step 9:** run_placement

 and openplacement image,if succesful you fill see the following  image.

![13](https://github.com/user-attachments/assets/550b6df7-ec04-4545-9d43-2388cad06e2d)

**Step 10:** run_cts

![14](https://github.com/user-attachments/assets/05970689-ced3-4c3a-a211-64d49c1d6f25)

**Step 11:** run_routing

![15](https://github.com/user-attachments/assets/80f83722-275d-4993-8bc1-fef96f3647d2)


![16](https://github.com/user-attachments/assets/4598b6bf-e146-48b6-8e03-bcde908162be)

### The end![2 ILE 2](https://github.com/user-attachments/assets/60b56f1f-6e9c-4ea9-a613-aa4e4e8cc4d9)


### ------------------ RISC V INTERNSHIP ------------------
### ______________WEEK-1___________________________________

Installing Leafpad editor

![1 Installing Leafpad editor](https://github.com/user-attachments/assets/cf0d0b1f-2648-497f-8e25-4988b0ed6498)

![2 ILE 2](https://github.com/user-attachments/assets/c3880c81-035f-4148-8f83-11773a7a1025)

Creating a file named "sum1ton.c"

![3](https://github.com/user-attachments/assets/66d37427-0388-4628-a0df-5c79066dd790)

A C-programme is written to find the sum of numbers from 1 to n, and the programme is executed.
![4](https://github.com/user-attachments/assets/2c8e884c-3864-416b-aaab-07542628cb0f)

 The programme is then compiled using the gcc compiler.
 
![5 2 Calling out the programme](https://github.com/user-attachments/assets/70a4ad2d-5a52-473b-a96d-90cf4546d541)



![4 2 Compiling the program](https://github.com/user-attachments/assets/d3850517-d8e3-4831-8ad1-f5a0dd0da041)


Cross-verification of the output of the programme.

![5 confirming](https://github.com/user-attachments/assets/101136e5-5033-4b38-b643-5cc9837168ff)


Updating the written programme to start a new command in the next line.


![6 Updating the programme](https://github.com/user-attachments/assets/40454273-9f46-4c57-b2cc-5c179b2fe81f)


We can see that the next command starts in a new line.
![7 The next command starts in a new line](https://github.com/user-attachments/assets/56b8c3eb-19ba-43c0-adbd-3e20518fb912)

Playing around with the programme.

![8 Playing Around](https://github.com/user-attachments/assets/96f30490-8836-460c-8a9f-b03cf6a4f1f7)


![8 2](https://github.com/user-attachments/assets/d162f5f6-db17-48c7-af3b-9c71d372caec)

Renaming the written programme from sum1ton.c to lab1sum1ton.c via the terminal.

![9 Renaming a file](https://github.com/user-attachments/assets/12edf1f1-bf72-4bb9-8d99-81ee255a26db)

The clear screen command -clear.
![10 Clear sreen](https://github.com/user-attachments/assets/604a9394-ce6c-472b-a74c-36aa88bc9e7b)

Compiling the written programme using Risc-V compiler.
![11 compiling using RISCv compiler](https://github.com/user-attachments/assets/39d69293-072b-4060-ba6c-f1afd251bb10)


The objectdump command is employed , and filtered out the main section which was found to have 17 instructions.
![12 objdump](https://github.com/user-attachments/assets/8136f9dd-ca4e-49ff-8777-ae04bc5e432f)

Cross-verification of the number of instructions.
![13 main section](https://github.com/user-attachments/assets/e4d77596-1eef-4d7a-92ba-2361798d9647)


![14 we have 17 instructions](https://github.com/user-attachments/assets/f826a5d3-5647-4ae0-8c2d-5dc2884818cd)

Changing the **option** fron **-O1 to -Ofast**
![15  Ofast](https://github.com/user-attachments/assets/7cf89e78-34eb-4d7d-8343-f732ad28e43f)

The number of instructions reduced from 17 to 13 under the -main section.

![15 2](https://github.com/user-attachments/assets/193fb232-633d-4539-a908-fc939eb327b7)

### __________________________________________________

