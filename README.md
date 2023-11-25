# BlinkerTestBluePill
Blinker Test Project for STM32 Blue Pill Evaluation Board


## Tools used for this project:
- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html).
- STM32 [ST-LINK utility](https://www.st.com/en/development-tools/stsw-link004.html).
- STM32 [ST-LINK USB driver](https://www.st.com/en/development-tools/stsw-link009.html).


## HW used for this project:
- STM32 [Blue Pill](https://stm32-base.org/boards/STM32F103C8T6-Blue-Pill.html) board.
- [ST-LINK V2](https://stm32-base.org/guides/connecting-your-debugger.html) clone.

![image](https://github.com/AhmedEltorky/BlinkerTestBluePill/assets/26473614/d7fb5b5d-c974-4b82-8bb7-64a13dbd3afd)
![st_link](https://github.com/AhmedEltorky/BlinkerTestBluePill/assets/26473614/ea0bb447-8ebf-40a2-b178-9174ab8812eb)



## Configuration steps for CubeMX:

- Open the configurations perspective.

- Enable crystal for the board.

![image](https://github.com/AhmedEltorky/BlinkerTestBluePill/assets/26473614/acc2995f-cb59-422c-aa33-8cac633e00bd)

- Configure PC13 "user LED" as GPIO_OUT.

![image](https://github.com/AhmedEltorky/BlinkerTestBluePill/assets/26473614/890a5668-f0a5-43a8-b923-2012822b0669)

- Save changes "Ctrl + C" to generate the required files.

- Build the project to generate the HEX and ELF files.

- Make sure to add the following command in the post build commands to generate the HEX file.
```
arm-none-eabi-objcopy -O ihex ${ProjName}.elf ${ProjName}.hex
```

![image](https://github.com/AhmedEltorky/BlinkerTestBluePill/assets/26473614/a6fee773-156e-4918-aeaf-59375d89044b)
