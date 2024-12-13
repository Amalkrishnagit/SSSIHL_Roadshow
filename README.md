**Introduction :**

In VLSI (Very-Large-Scale Integration) design, **EDI** (Electronic Design Interchange) refers to the exchange and integration of design data across different tools and stages of the design process. It ensures smooth communication between various tools like synthesis, simulation, layout, and verification, promoting efficient data sharing and reducing errors.

### Key Points:
1. **Tool Integration**: EDI facilitates data exchange between different Electronic Design Automation (EDA) tools (e.g., Cadence, Synopsys, Mentor Graphics).
2. **Standard Formats**: EDI relies on standardized formats like **GDSII**, **LEF/DEF**, **Verilog/VHDL**, and **SPICE** to ensure compatibility across tools and stages.
3. **Verification and Collaboration**: EDI enables seamless verification and collaboration between teams working on different aspects of the design.
4. **Manufacturing Data**: It ensures accurate data exchange for chip fabrication, using formats like **GDSII** and **OASIS** for photomask generation.
5. **Supply Chain Integration**: EDI also supports data exchange with suppliers, streamlining inventory and component management.

### Benefits:
- **Efficiency**: Automates data exchange, speeding up the design process.
- **Collaboration**: Facilitates team collaboration across locations.
- **Data Integrity**: Ensures accurate, consistent design data.

### Challenges:
- **Complexity**: Integration of diverse tools can be difficult.
- **Standardization**: Ensuring full interoperability between different EDI standards can be challenging.

Overall, EDI in VLSI design enhances the design flow, ensuring consistency and collaboration across different teams and stages.





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
virtual environment was loaded and a terminal was opened.
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
