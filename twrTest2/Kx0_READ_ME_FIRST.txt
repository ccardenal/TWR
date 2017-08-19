KINETIS:
Peripheral drivers are frequently updated by silicon vendors. Maintaining the target support for 
thousands of microcontrollers would be a tremendously time-consuming task. We therefore recommend 
all Kinetis developers to use the Processor Expert (PEx) and/or Kinetis Software development Kit (KSDK) 
to generate the latest versions of drivers, stacks and middleware for your project. Processor Expert 
integrates in to Atollic TrueSTUDIO seamlessly. Kinetis Software Development Kit builds example project 
package with out-of-the-box support for Atollic.

Read our application note on how to install Processor Expert in to Atollic TrueSTUDIO here:
http://www.atollic.com/resources/application-notes/

Read more on how to use Kinetis Software Development Kit here:
http://blog.atollic.com/custom-kinetis-sdk-for-truestudio


Note1:
In order to be able to program your Kinetis device FLASH you may need to first 
unlock the FLASH. This is done with JLink Commander <JLink.exe>. This program 
is located in folder %TRUESTUDIO_INSTALL_DIR%\Servers\J-Link_gdbserver

See Segger documentation for more information.

Note2:
The Kinetis device has a Flash Security Register resident 1Kb above FLASH 
origin. Make sure that you do not unconsciously overwrite this register as 
this can permanently damage your Kinetis device and "lock" the FLASH memory.

Note3:
In the SystemInit() function the clock speeds can be switched by changing 
the #define CLOCK_SETUP = x. CLOCK_SETUP = 0 (default = 41.94MHz)
The clock must be changed for SWV capabilities to any integer clock speed so 
that it works with Segger J-Link.

Note4: 
The Freescale KwikStik development tool for Kinetis MCU has a 4 MHz external 
crystal instead of 8 MHz. The SystemInit() function will set the MCU to run in 
24 MHz when CLOCK_SETUP = 1. The Freescale <system_MK40DZ10.c> file says that 
the frequency is 48 MHz but this information is wrong when used with the 
KwikStik board. The following Clock Settings can be used in the Debug  
Configurations to enable SWV functionality:  Core Clock 24.0 MHz and 
SWO Clock 500 kHz.

Note5: 
If the Segger software included in Atollic TrueSTUDIO does not support the used 
Kinetis device it can be updated at:  
http://www.segger.com/cms/jlink-software.html

Note6:
The P&E Micro Kinetis GDB Server requires some configuration before debugging. 
Information on how to do this can be found in the Atollic TrueSTUDIO User Guide.
