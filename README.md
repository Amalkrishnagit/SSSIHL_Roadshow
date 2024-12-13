**Introduction :**

In VLSI (Very-Large-Scale Integration) design, EDI refers to Electronic Design Interchange or Electronic Design Integration. It focuses on the integration and exchange of electronic design data between different tools, teams, and stages of the VLSI design process. EDI in VLSI design facilitates the efficient sharing of design information, ensuring that data flows seamlessly between various stages of design, verification, and manufacturing. This helps teams optimize the design process and maintain consistency across different platforms and tools.

Here are some key areas where EDI plays a role in VLSI design:

1. Tool Integration and Data Exchange
VLSI design often involves multiple tools that specialize in different aspects, such as schematic capture, simulation, place and route, timing analysis, and verification. EDI standards and frameworks help facilitate data exchange between these tools.
For example, tools like Cadence, Synopsys, and Mentor Graphics may use EDI protocols to exchange netlists, simulation results, layout files, and more.
2. Interoperability between Design Stages
In VLSI design, data needs to flow through various stages like high-level synthesis, RTL (Register Transfer Level) design, physical design (layout), verification, and final production.
EDI helps ensure that data from one stage is compatible with the next. For instance, netlists generated in the synthesis stage must be compatible with place-and-route tools that handle physical design.
3. Standard Data Formats
EDI systems in VLSI design often involve using standardized data formats for the exchange of design data, which ensures compatibility between different tools and systems. Common formats include:
GDSII (Graphic Data Stream): Used for layout data and physical design.
LEF/DEF (Library Exchange Format/Design Exchange Format): Used for exchanging library and design information.
Verilog/VHDL: Hardware description languages used for RTL design.
SPICE: Used for analog and mixed-signal simulation.
OASIS (Open Artwork System Interchange Standard): Used for physical design data exchange, especially in the mask-making process.
4. EDA Tool Integration Platforms
EDA (Electronic Design Automation) tools are a collection of software tools used for the design, simulation, and verification of integrated circuits. EDI plays a crucial role in integrating these tools into a cohesive workflow.
Platforms such as Cadence Design Systems, Synopsys, Mentor Graphics, and Ansys often use EDI techniques to share design data, synchronize processes, and facilitate collaboration between different design teams.
5. Version Control and Collaboration
EDI can also facilitate version control for large VLSI designs, where many teams are working on different parts of the design at the same time. It ensures that design changes made by different teams are synchronized, and the integrity of the design is maintained.
Tools like Git, SVN (Subversion), and Perforce can be integrated with EDI workflows to track changes to design files and collaborate in real-time.
6. Design Verification and Validation
EDI tools also play a key role in design verification. For example, ensuring that the RTL code written in Verilog or VHDL works correctly with the physical design (place and route) is an important part of the verification process.
The exchange of design data between simulation tools, formal verification tools, and the physical layout tools is crucial for ensuring that the final VLSI design is error-free and optimized.
7. Manufacturing Data Exchange
After the design process, VLSI designs are sent to fabrication. The manufacturing process needs precise data to create the physical chips. EDI ensures that data such as GDSII files, masks, and other manufacturing specifications are correctly communicated from design to fabrication.
EDI tools help in the exchange of production data for creating photomasks, which are critical in the photolithography process during chip manufacturing.
8. Supply Chain Integration
In large-scale VLSI design projects, various stakeholders, including design teams, fabrication plants, and assembly plants, need to exchange data in an efficient manner.
EDI can also be used to streamline the supply chain by facilitating the exchange of data such as inventory information, ordering details, and component specifications between suppliers and manufacturers.
Benefits of EDI in VLSI Design
Interoperability: EDI ensures that different tools and platforms can exchange data smoothly, making it easier to use specialized tools across various stages of design.
Efficiency: Automated data exchange reduces manual effort and the potential for errors, speeding up the design process.
Data Integrity: EDI protocols help maintain consistency and data accuracy, ensuring that design files are up-to-date and version-controlled across teams.
Collaboration: Multiple teams, sometimes across different locations, can work on a design simultaneously with EDI ensuring that data flows seamlessly between them.
Challenges of EDI in VLSI Design
Complexity: VLSI designs can be highly complex, and the integration of various tools can be challenging. The data exchanged often needs to be formatted in a way that ensures compatibility between different systems.
Standardization: While there are many standardized formats, each company may have specific requirements or proprietary formats, making full interoperability difficult.
Tool Compatibility: Different EDA tools may not natively support the same EDI standards, which can lead to challenges when trying to exchange data between different software platforms.
Conclusion
EDI in VLSI design serves as a critical enabler for efficient, automated, and error-free data exchange across various stages of the design, verification, and manufacturing processes. It promotes collaboration, interoperability, and synchronization of complex design data, which is essential for creating cutting-edge semiconductor products. However, it requires a strong integration strategy and attention to detail in managing data formats, standards, and tool compatibility.



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
**Step 1:**
![1](https://github.com/user-attachments/assets/b916021f-4ede-486a-8ca5-85ce0cdac1af)
virtual environment was loaded.

#include<stdio.h> int main(){ int sum = 0, i, n; printf("Enter the value of n = "); scanf("%d",&n); for(i = 1;i <= n;i++){ sum = sum + i; } printf("The Sum of numbers from 1 to %d is %d\n",n,sum); return 0; }
![2](https://github.com/user-attachments/assets/21eb5996-823c-4d3a-9b26-eda6a0cb5e92)
./a.out
![3](https://github.com/user-attachments/assets/781d6443-ebe7-4cbd-9161-403fb1ba68f1)

riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o hello.o hello.c
![4](https://github.com/user-attachments/assets/e0503bd3-6443-4e27-934a-165cb0a72fa8)

riscv64-unknown-elf-objdump -d hello.o
![5](https://github.com/user-attachments/assets/3894c449-40ad-40b7-8ac4-c7e885e1adf6)



**Change directory to openlane flow directory**
![6](https://github.com/user-attachments/assets/4bfbac96-eb21-42a3-9bb4-e036a869916c)
cd Desktop/work/tools/openlane_working_dir/openlane
![7](https://github.com/user-attachments/assets/b3e72ea9-2758-4857-b006-b42b47173456)

docker
![8](https://github.com/user-attachments/assets/1fad969c-99d9-4929-a33e-8c7429d60698)

./flow.tcl -interactive
![9 0](https://github.com/user-attachments/assets/897144f9-ad79-4474-bb56-c7254621cfce)

package require openlane 0.9
![9](https://github.com/user-attachments/assets/7315abe3-c74c-4b9b-92ed-2741b9328fc6)

prep -design picorv32a
![10](https://github.com/user-attachments/assets/ac112113-e225-49af-ab2a-8468aabea9cd)

run_synthesis
![11](https://github.com/user-attachments/assets/94e44717-645f-4414-8b95-bb5d168ff0ce)

run_floorplan

eog designs/picorv32a/runs/13-12_07-00/results/floorplan/picorva32a.floorplan.def.png

![12](https://github.com/user-attachments/assets/e04b1bd3-c841-48b8-958a-af999f6298d1)
![13](https://github.com/user-attachments/assets/550b6df7-ec04-4545-9d43-2388cad06e2d)
![14](https://github.com/user-attachments/assets/05970689-ced3-4c3a-a211-64d49c1d6f25)
![15](https://github.com/user-attachments/assets/80f83722-275d-4993-8bc1-fef96f3647d2)
![16](https://github.com/user-attachments/assets/4598b6bf-e146-48b6-8e03-bcde908162be)

**CODE FOR BLINKING**
// #include <ch32v00x.h>
// #include <debug.h>

// #define BLINKY_GPIO_PORT GPIOD
// #define BLINKY_GPIO_PIN GPIO_Pin_6
// #define BLINKY_CLOCK_ENABLE RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE)

// void NMI_Handler(void) __attribute__((interrupt("WCH-Interrupt-fast")));
// void HardFault_Handler(void) __attribute__((interrupt("WCH-Interrupt-fast")));
// void Delay_Init(void);
// void Delay_Ms(uint32_t n);

// int main(void)
// {
// 	NVIC_PriorityGroupConfig(NVIC_PriorityGroup_1);
// 	SystemCoreClockUpdate();
// 	Delay_Init();

// 	GPIO_InitTypeDef GPIO_InitStructure = {0};

// 	BLINKY_CLOCK_ENABLE;
// 	GPIO_InitStructure.GPIO_Pin = BLINKY_GPIO_PIN;
// 	GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
// 	GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
// 	GPIO_Init(BLINKY_GPIO_PORT, &GPIO_InitStructure);

// 	uint8_t ledState = 0;
// 	while (1)
// 	{
// 		GPIO_WriteBit(BLINKY_GPIO_PORT, BLINKY_GPIO_PIN, ledState);
// 		ledState ^= 1; // invert for the next run
// 		Delay_Ms(100);
// 	}
// }

// void NMI_Handler(void) {}
// void HardFault_Handler(void)
// {
// 	while (1)
// 	{
// 	}
// }

**
CODE FOR PULSEWIDTH MODULATION**
#include "debug.h"
#define TIME_PERIOD 1000
#define PRESC       0
#define PULSE       632
#define STEP_SIZE   10
volatile u16 val;
volatile u8 dir;
void TIM1_PWMOut_Init(void){
    GPIO_InitTypeDef GPIO_InitStructure={0};
    TIM_OCInitTypeDef TIM_OCInitStructure={0};
    TIM_TimeBaseInitTypeDef TIM_TimeBaseInitStructure={0};
    //RCC_APB2PeriphClockCmd( RCC_APB2Periph_GPIOC | RCC_APB2Periph_TIM1, ENABLE );
    RCC_APB2PeriphClockCmd( RCC_APB2Periph_GPIOD | RCC_APB2Periph_AFIO, ENABLE );
    RCC_APB1PeriphClockCmd( RCC_APB1Periph_TIM2, ENABLE );
    GPIO_PinRemapConfig(GPIO_FullRemap_TIM2, ENABLE);
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_6;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_AF_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init( GPIOD, &GPIO_InitStructure);
    TIM_TimeBaseInitStructure.TIM_Period = TIME_PERIOD;
    TIM_TimeBaseInitStructure.TIM_Prescaler = PRESC;
    TIM_TimeBaseInitStructure.TIM_ClockDivision = TIM_CKD_DIV1;
    TIM_TimeBaseInitStructure.TIM_CounterMode = TIM_CounterMode_Up;
    TIM_TimeBaseInit( TIM2, &TIM_TimeBaseInitStructure);
    TIM_OCInitStructure.TIM_OCMode = TIM_OCMode_PWM2;
    TIM_OCInitStructure.TIM_OutputState = TIM_OutputState_Enable;
    TIM_OCInitStructure.TIM_Pulse = PULSE;
    TIM_OCInitStructure.TIM_OCPolarity = TIM_OCPolarity_High;
    TIM_OC3Init( TIM2, &TIM_OCInitStructure );
    TIM_CtrlPWMOutputs(TIM2, ENABLE );
    //TIM_OC3PreloadConfig( TIM1, TIM_OCPreload_Disable );
    //TIM_ARRPreloadConfig( TIM1, ENABLE );
    TIM_Cmd( TIM2, ENABLE );
}
int main(void)
{
    NVIC_PriorityGroupConfig(NVIC_PriorityGroup_1);
    SystemCoreClockUpdate();
    Delay_Init();
    TIM1_PWMOut_Init();
    val = 0;
    dir = 0;
    // Loop
    while(1){
        val += (dir) ? -STEP_SIZE : STEP_SIZE;
        TIM_SetCompare3(TIM2, val);
        dir ^= (val == 1000 || val == 0) ? 1 : 0;
        Delay_Ms(15);
    }
}
