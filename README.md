# RL78_G15_DataFlash
 RL78_G15_DataFlash

udpate @ 2024/06/14

1. use RL78 G15 EVB to test data flash , refer to sample code and application note as below 

https://www.renesas.com/us/en/document/scd/rl78g15-group-renesas-flash-sample-program-type01-sc-version-data-flash-sample-code?language=en
 
 
https://www.renesas.com/us/en/document/apn/rl78g15-group-renesas-flash-sample-program-type01-sc-version-data-flash-application-notes
 
 
2. add data flash by Smart Configurator , base on application note 

3. modify setting , base on application note 

if MCU is 8K flash

.text,.data,.sdata,.RLIB,.SLIB,.textf,.constf/000D8,.const/01D00,.dataR,.bss/FFB00,.sdataR,.sbss/FFE20

if MCU is 16K flash

.text,.data,.sdata,.RLIB,.SLIB,.textf,.constf/000D8,.const/03D00,.dataR,.bss/FFB00,.sdataR,.sbss/FFE20

if MCU is 32K flash

.text,.data,.sdata,.RLIB,.SLIB,.textf,.constf/000D8,.const/07D00,.dataR,.bss/FFB00,.sdataR,.sbss/FFE20


![image](https://github.com/released/RL78_G15_DataFlash/blob/main/Link_Options_Section_1.jpg)


![image](https://github.com/released/RL78_G15_DataFlash/blob/main/Link_Options_Section_2.jpg)


4. set the common file header and c code from sample code , 

![image](https://github.com/released/RL78_G15_DataFlash/blob/main/include_file.jpg)


![image](https://github.com/released/RL78_G15_DataFlash/blob/main/Common_Options_Additional_include_paths.jpg)

 
5. use terminal digit 1 , to test data flash write at byte index 2

use terminal digit 2 , to read data flash with expect length

under CS+ debug mode , read memory address when stop debug 


below is length : 16 
![image](https://github.com/released/RL78_G15_DataFlash/blob/main/log_16bytes.jpg)


below is length : 64
![image](https://github.com/released/RL78_G15_DataFlash/blob/main/log_64bytes.jpg)


