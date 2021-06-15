# VIS 16 PC - Specifications
<span style="display: block;text-align: center">
<img src="media/vis-logo.png">
</span>

## 0-What is this?
This is the specifications for the VIS 16 PC, this includes the CPU, RAM, ROM, instruction sets and etc.
### 0.1-Licence
<span style="display: block;text-align: center">
<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">VIS 16 specs</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/vis-PC/" property="cc:attributionName" rel="cc:attributionURL">VIS COMPUTER INDUSTRIES</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://vis16specs.glitch.me" rel="dct:source">vis16specs.glitch.me</a>.
</span>

## 1-The Computer
### 1.1-Introduction to the VIS 16
The VIS 16 is a capable small computer with the best performance, graphics, speed and functionality.
### 1.2-Components
This computer runs on a ```VIS MC 16x2``` (or ```16x1``` for the e model, a ```16x3``` for the plus model, a ```16x0``` for the mini model or a ```16x2p``` for the VIS 16 portable) with the ```SSTx16™``` architecture (Smart and Safe Threads 16 bit architecture).

It has ```64kb``` of ```SM0``` RAM (Safe Memory gen 0 RAM).

It has a ```VIS Visuals Fancy x3ff``` Graphic Unit.

It has a state of the art VIS Sharp CRT Display; a Click Safe™ Keyboard and a Roll Top™ mouse.

It has 2 Floppy Drive Slots, One is Boot-able.

## 2-CPU
The is a ```VIS MC 16x2``` (or ```16x1``` for the e model, a ```16x3``` for the plus model, a ```16x0``` for the mini model or a ```16x2p``` for the VIS 16 portable) with the ```SSTx16™``` architecture (Smart and Safe Threads 16 bit architecture).

### 2.1-Instructions

```
incM | increments memory by the given value              | incM: [memory address], [value (a number)];
movM | Transfer the value in the selected memory address | movM: [memory address], [value or memory address];
getM | gets and returns the value from a memory address  | getM: [memory address]
setM | sets the value for a memory adress                | setM: [memory address], [value]
oprM | does the chosen operation on a memory address     | oprM: [memory address], [operation options: add (addition) | sub (subtranction) | mut (multiplication) | 'div (division)], [value (a number)]
clsM | clear a memory address                            | clsM: [memory address]

```
### 2.2-Memory addresses
The Memory is a Safe Memory; so, it co-operates with the code.
you get 32 memory address, to select in code you start with a 'm' followed by a number to represent the memory location.
for example if I want to select the 26th address I will write ```m26```
If you try selecting over 32, it will default to 32.

You will get 64kb of memory which is 512000 bits which is divided into 32 addresses; so, each address is 16000 bits, because this is safe memory, it can overflow into the next memory, if there is data in the next memory address it will push the data to the next address until it gets to 32, where it dumps it out of ROM forever. so the best practice is to work with alternate memory addresses; for example you will use the m1 address, if you need another address, instead of using m2 you will use m3 and instead of m4 you will use m5, so on so forth.

To not overflow you can use the ```t``` operator to truncate the value to the desired length of the address; example: ```m29t``` to truncate my value to 16000.