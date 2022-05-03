# 8BitComputer
Documentation of my Ben Eater style 8 bit breadboard computer

Videos and pictures I took at different stages of constructing the 8 bit computer.

A few things I had to change from Ben Eaters design:

1. Filters on the control and clock lines. There was too much noise on the bus and control lines at higher clock frequencies, so I had to run especially noisey
lines through double inverter RC filters to clean up the signals. This meant I had to add a bunch of inverter HCT7404's on the computer and rearrange some things

2. Capacitors everywhere. The power distribution wasnt ideal on the breadboards, so capacitors where necessary on every power rail, as well as across the power pins
of power hungry chips

3. Resistors on every LED. The LS series(used in this build) IC's internal resistors are not reliable enough to draw current directly into an LED to ground from on of
the pins. Doing this would result in hot, fried chips. So I had to add 220-1000 ohm resistors to the LEDS. Where there was room I just added these into the breadboards,
where you see rows of resistors and wires leading into LEDS. Where there wasn't room, I soldered the resistors to the LED legs directly. Earlier attempts at this
used all purpose solder, resulting in messy solder jobs like the one in the LED solder photo. Eventually I spent some money on some electronics solder and 
the solder jobs became much cleaner and easier

4. Pull up/Pull down resistors on all input pins. The LS series chips didn't work as specified with floating inputs, so I tied all of them to 
either Hi or Lo with a resistor. This resulted in more consistent behaviour.

