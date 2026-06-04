A great idea from ‘juh’—it makes the TM1638 LED&Key board more universally controllable via I2C. Based on https://www.printables.com/model/312494-tm1638-ledkey-with-i2c-for-fischertechnik

I designed a dedicated PCB so I wouldn’t have to build it on experiment-board with holes. After removing the original pin header from the LED&Key board, this small PCB can be soldered to the side using five pieces of mounting wire. I placed the ATtiny85 in an IC socket so I could program it with my ISP programmer.

I also made a simpler open enclosure for use with the fischertechnik construction system. 
Both the PCB design and the STL file for the 3D enclosure can be found on GitHub. On the bottom of the enclosure, there are four studs with a 4.4mm hole for M3x5 melt-in wire stubs to secure the board. These can be drilled out if the PCB is mounted with standard M3 screws.

The board is powered by 5 volts via the 6-pin DC3 header. In the case of a 5-volt I2C bus (such as the ftDuino) that also provides the necessary DC voltage (on pin 2 of the DC3 connector), this is therefore possible using a direct flat cable. To use the board with the classic fischertechnik TXT or the more modern TXT4.0 controller (both 3.3V I2C!), a level shifter with an additional 5-volt power supply must be connected in between. I personally used my I2C hub, available elsewhere on GitHub, for this purpose.

Since I preferred flexible I2C adapters and extension cables with color-coded wires instead of the stiff DC3 flat cables with cut and crossed wires for adapters to, say, Grove/Seeed, I designed a simple adapter that allows a female 2x3 Dupont header to be easily converted into a six-pin IDC header with a positioning tab.
