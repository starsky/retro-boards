# Board name
8517 REV: 2.1

# Chips

## Processor
386SX -- soldered to the mb

## Chipset
ALI M1217-40

## Ports
6x 16bit ISA

## Memory
4x 30 pin slots

# Board ref
1. https://theretroweb.com/motherboards/s/mg-8517-rev-2-2 -- pretty similar. JP6 seems to be hardwired. We have it open.
2. The above referes here: https://theretroweb.com/motherboards/s/auva-computer-npm16-a0 It has manual with jumpers explained.

# Source
Bought it from local online platform (OLX).

# Initial condition
1. Barrel attery was still installed. 
2. Two broken traces on the bottom of PCB (keyboard related).
3. Trace for + terminal of battery damaged.
4. Trace from goldpin header marked "ext battery" damaged.
5. RTC batt power trace damaged. Via to the other side of the PCB completly damaged.
6. Trace from power good pin damaged. 
7. Dull solder on resistors and capacitors near power good trace.
8. DIP sockets with blue colored damage from battery.
..

# Treatment
## First session
1. Removed battery.
2. Removed ext battery gold pin header.
3. Tinned traces from 2., 3., 4., 5.
4. Added jumper wire to fix 5.
5. Removed 4 electrolytic caps (10uF), 1 ceramic (100nF), and 4 resistors (10k, 1k, 10k, 10k).
6. Tinned power rails traces and power good (6.), covered with naild polish to prevent any shorts.
7. Reinstalled same components as measured params were OK.
8. Removed all ICs from socket. Cleand contacts. Reinstalled ICs.
9. Dumped ROM and saved to file.

# Tests
Initialid it did not POST at all. POST ISA card showed no activity. CPU got warm.
I reinstalled ROM chip couple of times, and it started to work. The DIP socket looks broken.

It POSTed normally, the DOS booted up.

# Jumpers
Jumpers are explained in the pdf in the doc directory.

# TODOs
1. Replace ROM DIP socket. Also replces jumper goldpins next to it.
2. Install JST battery header.

# Other
The power good circuit consists of 100nF capacitor and 10k resistor. It looks like this:
PG-----|---|------out
       C   R
       |   |
      gnd +5V
When powere supply starts it is an open collector thus current flows thru resistor to PG.
Next when power supply is ready, it is no longer a open collector, thus current flows from
+5V through resistor and capacitor. It gives ceratin delay, before reset signal is off.
