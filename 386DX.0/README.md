# Board name
Unknown

# Chips

## Processor
386DX -- soldered to the mb

## Chipset
UMC UM82C491F

## Ports
5x 16bit ISA
1x 8bit ISA

## Memory
4x 30 pin slots
2x 72 pin slots

# Board ref
Could not find any similar.

# Source
Found it in my basement.

# Initial condition
1. Barrel attery was still installed. 
2. 2 broken traces close to batter. One from + battery terminal.

# Treatment
## First session
1. Removed battery.
2. Removed ext battery gold pin header.
3. Tinned traces, and added wires to restore connection.
4. Installed JST-XH connector in place of ext battery goldpins. Connected to CR2032 battery in external case.

# Tests
System boots fine after repairs. 
The battery works, CMOS settings are preserved.

There is a minor issue, RTC on battery seems to work too slow. It lost couple of days in 10 months.

# Jumpers
It looks like it has only one jumper on the board.

# TODOs
1. Dump ROM
2. Check RTC battery power. Why clock is running too slow?
3. Why disc controller has to be in a specific slot?

# Other
I used it succesfully, event with one long session with games (couple of hours). Board works stable.
I then tried to use it again after 10 months. I plugged VGA and disc controller to random ISA slots, and
I got messages about disc not present, or controller error. I checked the photos from the time when it was working.
When I placed VGA and controller to same ISA slots, system booted.
