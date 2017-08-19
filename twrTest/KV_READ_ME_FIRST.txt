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
The Kinetis device has a Flash Security Register resident 1Kb above FLASH 
origin. Make sure that you do not unconsciously overwrite this register as 
this can permanently damage your Kinetis device and "lock" the FLASH memory.

Note2: 
If the Segger software included in Atollic TrueSTUDIO does not support the used 
Kinetis device it can be updated at:  
http://www.segger.com/cms/jlink-software.html

Note3:
The P&E Micro Kinetis GDB Server requires some configuration before debugging. 
Information on how to do this can be found in the Atollic TrueSTUDIO User Guide.
