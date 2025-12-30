# Board name
Unknown with OPTi chipset

# Chips

### Processor
386DX -- socket 132PGA

### Chipset
OPTi F82C206
OPTi F82C382

### Ports
7x 16bit ISA
1x 8bit ISA

### Memory
8x 30 pin slots

# Board ref
1. https://theretroweb.com/motherboards/s/unknown-opti-386-16 Looks like this one. Except mine has 
OPTi chipset in place of Siemens. Also mine has a crystal near to the CPU, 
while the reference board has empty space.

# Source
Found it in my basement.

# Initial condition
1. Barrel battery was still installed. 
2. Broken traces near the chipset close to AT power connector.


# Treatment
## First session
1. Removed battery.
2. Tinned traces, and added wires to restore connection. I had to add 3 0.1 mm wires
near the chipset. 


# Tests
The board posted after the repair. I used it for a bit I think it works stable.

# Jumpers
I think there is only one jumper near the ISA slots.
The jumper is labeled J20 and has 4 pins. I need to figure out what it does.

# TODOs
1. Add RTC battery connector
2. Add jumpers description

# Other
The board seems to be either old or budget one. The BIOS settings are very limited.
At the beginning I had to wait a lot at the BIOS screen, but when I turned on BIOS
and video ROM shadowing BIOS screen and setup started to work as expected.

The board reports 11 pts. in landmark. Which is 1/3 of 384DX 40 MHz board.
This one is 25 MHz, I am not sure if this is correct. I could not find any cache
installed on board, nor any settings in BIOS. Maybe lack of cache is the reason
for low score.
