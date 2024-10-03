[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Alat-Musik-Piano-Berbasis-STM32?logo=Codeforces&logoColor=white&color=%23F7DF1E)
![Project](https://img.shields.io/badge/Project-STM32-light.svg?style=flat&logo=STMicroelectronics&logoColor=white&color=%23F7DF1E)
![Type](https://img.shields.io/badge/Type-Personal%20Experiment-light.svg?style=flat&logo=gitbook&logoColor=white&color=%23F7DF1E)

# Alat-Musik-Piano-Berbasis-STM32
<strong>Solo Project: STM32-based Piano Instrument</strong><br><br>
Piano is a melodic musical instrument that can produce tones when pressed. This musical instrument is in demand by many people because of its beautiful sound harmonization. However, its expensive price in the market makes some people unable to afford it. Therefore, this project was created with the aim of letting the general public know that pianos can actually be assembled by themselves, so price will no longer be a barrier. This will certainly be very beneficial for the wider community, because in addition to cutting costs, you can also customize it. This project has been done and took approximately 4 days. The results of this study show that the system can function properly.

<br><br>

## Project Requirements
| Part | Description |
| --- | --- |
| Development Board | STM32F103C8T6 |
| Code Editor | Arduino IDE |
| Programmer Tools | ST-Link/V2 |
| Driver | ST-Link USB Driver |
| Communications Protocol | Universal Asynchronous Receiver-Transmitter (UART) |
| Application Support | STM32CubeProgrammer |
| Programming Language | C/C++ |
| Arduino Library | • SoftwareSerial (default)<br>• DFRobotDFPlayerMini |
| Actuators | Speaker |
| Other Components | • Micro USB cable - USB type A (x1)<br>• Adaptor DC 5V (x1)<br>• Jumper cable (1 set)<br>• DF-Player Mini MP3-TF16P (x1)<br>• Micro SD card: SanDisk (x1)<br>• Breadboard (x2)<br>• Resistor (x1)<br>• Electrolytic capacitor (x1)<br>• Push button 12 x 12 mm (x8) |

<br><br>

## Download & Install
1. Arduino IDE

   <table><tr><td width="810">
         
   ```
   https://bit.ly/ArduinoIDE_Installer
   ```

   </td></tr></table><br>

2. ST-Link USB Driver

   <table><tr><td width="810">

   ```
   https://bit.ly/STLink_USB_Driver
   ```

   </td></tr></table><br>

3. STM32CubeProgrammer

   <table><tr><td width="810">
   
   ```
   https://bit.ly/STM32_Cube_Programmer_Installer
   ```

   </td></tr></table>
   
<br><br>

## Project Designs
<table>
<tr>
<th width="420">Block Diagram</th>
<th width="420">Pictorial Diagram</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Diagram/Block Diagram.jpg" alt="block-diagram"></td>
<td><img src="Assets/Documentation/Diagram/Pictorial Diagram.jpg" alt="pictorial-diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Wiring</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Table/Device Wiring.jpg" alt="wiring"></td>
</tr>
</table>

<br><br>

## Basic Knowledge
Basically, a device can be communicated with other devices either wirelessly or by cable. Communication between commonly used hardware is ``` Serial Communication ```. It can be known that there are three types of ``` Serial Communication ```, which include: ``` UART (Universal Asynchronous Receiver-Transmitter) ```, ``` SPI (Serial Peripheral Interface) ```, and ``` I2C (Inter Integrated Circuit) ```. There are two kinds of ``` UART Serial Communication ```, namely ``` Hardware Serial ``` and ``` Software Serial ```. ``` Hardware serial communication ``` can be done by connecting the ``` TX ``` and ``` RX ``` pins ``` crosswise ``` on each development board, for example: ``` RX-TX ```, then ``` TX-RX ```. The ``` TX ``` pin is for ``` sending data ```, while the ``` RX ``` pin is for ``` receiving data ```. ``` Serial Software Communication ``` is more or less the same as ``` Serial Hardware Communication ``` in terms of cabling, but there are differences in terms of coding. By using this ``` Serial Software ``` you can overcome the constraints of the limitations of ``` RX ``` and ``` TX ``` pins on the development board. To communicate with this ``` Serial Software ``` is quite easy, namely by using certain ``` Digital Pins ``` as a ``` substitute for TX pins and RX pins ```.

<br><br>

## Arduino IDE Setup
1. Open the ``` Arduino IDE ``` first, then open this project by clicking ``` File ``` -> ``` Open ``` :

   <table><tr><td width="810">
      
      ``` pianomini_stm32.ino ```

   </td></tr></table><br>
   
2. Fill in the ``` Additional Board Manager URLs ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` File ``` -> ``` Preferences ``` -> enter the ``` Boards Manager Url ``` by copying the following link :
      
      ```
      https://github.com/stm32duino/BoardManagerFiles/raw/main/package_stmicroelectronics_index.json
      ```

   </td></tr></table><br>
   
3. ``` Board Setup ``` in Arduino IDE

   <table>
      <tr><th width="810">

      How to setup the ``` STM32F103C8T6 ``` board
            
      </th></tr>
      <tr><td>
         
      • Click ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` STM32 MCU based boards ```.

      • Then click ``` Tools ``` -> ``` Board ``` -> ``` STM32 boards groups ``` -> ``` Generic STM32F1 series ```.

      </td></tr>
   </table><br>
   
4. ``` Change Board Part Number ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Tools ``` -> ``` Board part number ``` -> ``` BluePill F103C8 ```

   </td></tr></table><br>
   
5. ``` Change U(S)ART Support ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Tools ``` -> ``` U(S)ART Support ``` -> ``` Enabled (generic 'Serial') ```

   </td></tr></table><br>

6. ``` Change Upload Method ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Tools ``` -> ``` Upload method ``` -> ``` STM32CubeProgrammer (SWD) ```

   </td></tr></table><br>
   
7. ``` Install Library ``` in Arduino IDE

   <table><tr><td width="810">
         
      Download all the library zip files. Then paste it in the: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```

   </td></tr></table><br>
   
8. Before uploading the program please click: ``` Verify ```.<br><br>

9. If there is no error in the program code, the next step is to use the ``` STM32 ``` programming tool according to the procedure. Then click: ``` Upload ```.<br><br>

10. If there is still a problem when uploading the program, then try checking the ``` driver ``` / ``` port ``` / ``` programmer tool ``` / ``` others ``` section.

<br><br>

## ST-Link/V2 Setup
<img width="840" src="Assets/Documentation/Experiment/ST-Link Configuration.jpg" alt="stlink-configuration"><br><br>

<strong>Notes:</strong>

<table><tr><td width="840">

   • The JTAG or ``` Serial Cable Debugging (SWD) ``` interface module is basically used to communicate with the ``` STM32 ``` board.
   
   • You can see the wiring between the ``` ST-Link/V2 ``` and the ``` STM32 ``` board in the picture above.

   • To upload the program, besides using the ``` ST-Link/V2 ```, you can also use other programming tools such as: ``` CP2102 USB ```, ``` CH340 USB ```, ``` PL2303 USB ```, or with ``` FTDI USB ```.
   
   • Based on experience, I admit that using the ``` ST-Link/V2 ``` is much better than other programming tools because the process is easier, faster, and more stable.

</td></tr></table>

<br><br>

## Get Started
1. Download and extract this repository.<br><br>
   
2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Configure your device according to the settings above.<br><br>

5. Please enjoy [Done].

<br><br>

## Highlights
<img width="840" src="Assets/Documentation/Experiment/Device.jpg" alt="pianomini-stm32">

<br><br>

## Appreciation
If this work is useful to you, then support this work as a form of appreciation to the author by clicking the ``` ⭐Star ``` button at the top of the repository.

<br><br>

## LICENSE
MIT License - Copyright © 2024 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
