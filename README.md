# ARM7_LPC2129

__1. Title: Led Light bilinking System Using LPC2129__

*Objective:* To understand and implement LED control using a microcontroller by turning it on and off at a fixed interval.

__Hardware Connection:__
 - LPC2129 P0.7 --> LED
 - LED --> GND

__Software Simulation:__


__Hardware Simulation:__

__Code:__
```
#include <lpc21xx.h>
void delay_s(unsigned int dly)
{
	dly=dly*12000000;
	while(dly--);
}
#define LED 7
int main()
{
	IODIR0 |=1<<LED;
	
	while(1)
	{
		IOSET0=1<<LED;
		delay_s(1);
		IOCLR0=1<<LED;
		delay_s(1);
	}
}
```

_________________________________________________________________________________________________________________________________________________________________________
