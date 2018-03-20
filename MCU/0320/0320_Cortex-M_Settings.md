Download(Install)
    STM32CubeMX : http://www.st.com/en/development-tools/stm32cubemx.html
        Java 8 : https://www.java.com/ko/download/
    STM32 Flash loader demonstrator : http://www.st.com/en/development-tools/flasher-stm32.html
    IAR Embedded Workbench for ARM : https://www.iar.com/kr/iar-embedded-workbench2/#!?architecture=Arm



1. STM32CubeMX Create Project (MCU Part Number : STM32F103VCTx)

2. Set Pinout
        OSC_IN : RCC_OSC_IN
        OSC_OUT : RCC_OSC_OUT
        PE2, PE3, PE4 : GPIO_Output

3. Clock Configuration
        HCLK (MHz) : 72
        APB1 Prescaler : /2

4. [Project] -> [Generate Code (Ctrl + Shift + G)] -> Opened IAR Embedded Workbench

5. Write Code [Project/Application/User/main.c]
    "HAL_GPIO_WritePin(GPIOE, GPIO_PIN_2|GPIO_PIN_3|GPIO_PIN_4, GPIO_PIN_SET);"

6. [Project] -> [Rebuild All]

7. Demonstrator GUI (Flash Loader Demonstrator)
    Connect Device-UART
    Select File [..\'Project_Name'\EWARM\"Project_Name"\Exe\'Project_Name.bin']
    

Word
    HAL : Hardware Abstraction Layer


Blog
    http://rodneyhuh.tistory.com/13

