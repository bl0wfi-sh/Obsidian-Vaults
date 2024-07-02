Tutorials
- STM32 blue pill
	- https://youtu.be/_1u7IOnivnM?si=GNdCuDZQ-ttLJ4UW
Mcu-link (nxp)
- https://mcuoneclipse.com/2020/12/15/openocd-with-mcu-link/

General takeaways
- You really only need to configure two things when using OpenOCD
1. The type of prob you are using
	- jlink
	- mcu-link
	- Stlink
2. The type of CPU you are debugging
	- stm32f7
	- rt1176
	- pico
- Once the configuration is sorted out things work easily!
- OpenOCD opens 3 local ports when it connects to the cpu
	- 3333 - gdb remote target
	- 

