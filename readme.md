#README

This is an ascii-based computer architecture ide.

Terminology:
term|definition
-|-
wire|carries a signal in any direction it connects to, used as output for logic gates
diode|carries a signal from one direction to the opposite side only, used as input for logic gates
logic gates|gates that perform different functions, ie. `*, +, x, !, low, high`
bus|a set of wires, individual wires are accessed through 0-9, a-f
bus board|all busses, individual busses are accessed through A-Z
floating|whether or not a piece can sit with no references (not actual terminology)


Syntax:
floating|command|ascii|definition
-|-|-|-
no|bus|║ ═ ╠ ╩ ╦ ╣ ╚ ╗ ╔ ╝ ╬|carries wire references
no|wire|│ ─ └ ┐ ┌ ┘ ┼|carries boolean references
no|junction|■|connects crossing lines (┼ are crossing wires)
no|reader|r|reads booleans to a wire from a logic gate (chooses direction of a logic gate)
no|and|\*|returns 1 if all inputs are 1
no|or|+|returns 0 if all inputs are 0 
no|xor|x|returns 1 if an odd number of inputs is 1
no|nor|!|returns 1 if all inputs are 0 
yes|high|h|returns 1
yes|low|l|returns 0
yes|input|i|switch, shows and returns value, changed when clicked
no|output|0|shows the value of the wire connected to it
yes|bus call|A-Z|refers to a bus from the busboard
no|wire call|0-9, a-f|refers to a wire from the bus it connects to

Example program (4 bit incrementer):
```
a
╠═════╦══════╦══════╦══════╗
0     1      2      3      4
│     │      │      │      │
│     ■─┐    ■─┐    ■─┐    │
■───■─┼─*r─■─┼─*r─■─┼─*r───x
│   └─x    └─x    └─x      r
!     r      r      r      │
r     │      │      │      │
│     │      │      │      │
0     1      2      3      4
╠═════╩══════╩══════╩══════╝
b
```
Currently implemented:
- [ ] planning
    - [x] creating repository
    - [ ] checklist
    - [ ] syntax
    - [x] example program
    - [ ] data structure
    - [ ] determining compile order
    - [ ] determining run order
- [ ] writing
    - [ ] adding wires
    - [ ] adding busses
    - [ ] alphanumeric typing
    - [ ] 
- [ ] compiling
    - [ ] generating hashes based on readers
    - [ ] expanding/merging hashes using wires
    - [ ] making a list of all gates with which hashes control them
    
- [ ] running
    - [ ] 
