A great idea from ‘juh’—it makes the TM1638 LED&Key board more universally controllable via I2C. 

I designed a separate PCB so I wouldn’t have to build it on a breadboard. After removing the original pin header from the LED&Key board, this small PCB can be soldered to the side using five pieces of mounting wire. I placed the ATtiny85 in an IC socket so I could program it with my ISP programmer.

I also made a simpler open enclosure for use with the Fischertechnik construction system. 
Both the PCB design and the STL file for the 3D enclosure can be found on GitHub.

The board is powered by 5 volts via the 6-pin DC3 header. In the case of a 5-volt I2C bus (such as the ftDuino), this is therefore possible using a direct flat cable. To use the board with the classic fischertechnik TXT or the more modern TXT4.0 controller (both 3.3V I2C!), a level shifter with an additional 5-volt power supply must be connected in between. I personally used my I2C hub, available elsewhere on GitHub, for this purpose.

Translated with DeepL.com (free version)
