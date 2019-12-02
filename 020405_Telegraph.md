---
layout: default
---

# micro:bit Binary Telegraph
[Home](./)

Use your micro:bit to send and recive secret messages with your friends.

<iframe width="560" height="315" src="https://www.youtube.com/embed/wCQSIub_g7M" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Most everyone who uses a computer has heard the terms, kilobyte (kB), Megabyte (MB), Gigabyte (GB) and even Terabyte (TB), usually when referring to the size of computer files and hard drives as well as download speeds. Bandwidth or connection rates are measured in bits/second. But what is a bit and what is a byte and what do they have to do with computers?

Picture a basic room light. The light is either on or it is off. You control the current state of the light by flipping a switch that has only two settings, down (light off) and up (light on). The earliest computers used a series of mechanical switches to control the flow of electricity through their circuits, turning each one on or off. The on/off states of the circuits was used to represent and even store information. The smallest unit of information, representing the state of one switch, is known as a bit.

A bit is a binary digit and has only two possible values, zero or one. The value of the bit represents the current state of a single switch. If the switch is off, then the bit has the value zero. If the switch is on, then the bit has the value one. 

A bit can only represent two different values, zero or one. To represent larger pieces of information, bits are strung together in sequences of 8 called bytes. 

A byte is a sequence of binary digits made up of 8 bits.

A byte can represent any value from 00000000 through 11111111, for a total of 256 different possible values. Each digit in a byte can be thought of as representing an individual switch that is either off (zero) or on (one). We can map these bytes to english characters using a format called [ASCII](https://en.wikipedia.org/wiki/ASCII). Printable ASCII converstion chart [here](https://www.eecis.udel.edu/~amer/CISC651/ASCII-Conversion-Chart.pdf).

Modern computers rely on transistors, which pack millions of tiny switches into a chip smaller than your thumb, but information is still represented in essentially the same way: as a series of ones and zeros. By using binary, computers can represent information simply and efficiently using a system that is very effectively modeled in digital circuitry.

## Review

* A Bit is a binary digit with two possible values, zero or one
* A Byte is a sequence of 8 bits and has 256 possible values from 00000000 through 11111111
* A kilobyte (kB) is 1,024 bytes or 2^10 bytes
* A Megabyte (MB) is 1,048, 576 bytes or 2^20 bytes
* A Gigabyte (GB) is 1,073,741,824 bytes or 2^30 bytes
* A Terabyte (TB) is 1,099,511,627,776 bytes or 2^40 bytes
	
## Notes 

* The ones and zeros of bits and bytes can be used to represent letters, numbers, and even different keys on a computer keyboard. 
* A bit can be used to hold a Boolean (true/false) value.  A value of zero represents ‘false’ and a value of one represents ‘true’.
	
## Pseudocode

> NOTE: We have not discussed functions, but they are a way to make code more reusable. By taking a chunk of code and placing it in a function, I can execute that code by just calling the function, I dont have to retype or copy/paste that same code multiple times.

1. Global Variables
    1. `character` = this holds the last decoded ASCII character
    1. `bit` = this holds the postion in the binary character that we are entering (0 - 7)
    1. `word` = this holds the current word we have entered in ASCII
    1. `letter` = this holds the current binary that we have entered (i.e. 01001000 for the letter H)
1. function reset - the purpose of this function is to reset the program back to a none clear configuration
    1. reset all the global variables to zero or empty string
1. function nextBit - the purpose of this function is to accept a bit of input from the user and store it in memory
    1. if we are on bit 7 
        1. then decode the `letter` to english and put it in the `character` variable
        1. next show the `character` on the screen
        1. concatenate the `character` to the end of the `word`
        1. set the `bit` to 0
        1. set the `letter` to empty string
    1. if we are not on bit 7
        1. then incrment `bit`
1. `on start`
    1. set the radio group
    1. call the `reset` function
1. `on button A pressed`
    1. concatenate a '1' to the end of `letter`
    1. call the `nextBit` function
1. `on button B pressed`
    1. concatenate a '0' to the end of `letter`
    1. call the `nextBit` function
1. `on button A+B pressed`
    1. clear screen
    1. show string `word`
    1. radio send string `word`
    1. call the `reset` function
1. `on radio received`
    1. show the received string

## Operation

For our program we will input a 1 by pressing the A button and a 0 by pressing the B button. When we are ready to send our message we will press A & B together.

So to send the message HI or (01001000 01001001) we will enter BABBABBB BABBABBA. 

1. Download the code [here](./assets/hex/microbit-Telegraph.hex) and import it into Make Code.
1. Update the radio group # to one that is unique between you and your friend
1. Download the code onto both of your micro:bits
1. Using the ASCII chart send your friend secret messages.

> NOTE: The radio in the micro:bit is using [bluetooth low energy](https://en.wikipedia.org/wiki/Bluetooth_Low_Energy) so it has a max range of 300 feet. 