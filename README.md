Open source EDI tools-has a lot of updates
power of open source
synopsis cadence
The virtual machine
open terminal
Insatlling gedit
sudo apt install gedit
vsdiat
gedit
sae code hello.c
putin commands
compiler-code
assembler-code.100010101001010101010
changing to risc-v commands(tamil to marathi)
PLL-High clock speeds
vlsisystemdesign.com
Foundry IP,s-intellectual property
Why RISC (Architecture)file?
ARM Architecture-mobile phones
opensource versus proprietary
flip flops-registers
chip tapeout
firmware download
register transfer lecel-similar to c language converting to and and other gates
welcome to linuxineed a lot of focus to the atmost level
softcopy of RTL is ready and call
we have stick to one of the foundry-here skywater-minessota-sky130A-factory skywater-130 nanometers.
number of cells-4 billion gates-for processors-GPU
FPGA-BURNS PROGRAMME AND HARDWARE.
CLOCK SHOLUD REACH AT ALL END POINTS AT THE SAME TIME.
flipflop clocks
routing
skew
routing
GDS2(ii)-graphic database ii in VLSI-graphical dtatabase information interchange.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
![1](https://github.com/user-attachments/assets/b916021f-4ede-486a-8ca5-85ce0cdac1af)

#include<stdio.h> int main(){ int sum = 0, i, n; printf("Enter the value of n = "); scanf("%d",&n); for(i = 1;i <= n;i++){ sum = sum + i; } printf("The Sum of numbers from 1 to %d is %d\n",n,sum); return 0; }

./a.out

riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o hello.o hello.c

riscv64-unknown-elf-objdump -d hello.o

**Change directory to openlane flow directory**
cd Desktop/work/tools/openlane_working_dir/openlane

docker

./flow.tcl -interactive

package require openlane 0.9

prep -design picorv32a

run_synthesis

run_floorplan

eog designs/picorv32a/runs/13-12_07-00/results/floorplan/picorva32a.floorplan.def.png


