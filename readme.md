#README

This is an ascii-based computer architecture ide.

Terminology:
term|definition
-|-
wire|carries a signal in any direction it connects to, used as output for logic gates
diode|carries a signal from one direction to the opposite side only, used as input for logic gates
logic gates|gates that perform different functions, ie. `*+x!`
bus|a set of wires, individual wires are accessed through 0-f
bus board|a global variable containing all busses, accessed through g-z

Syntax:
command|ascii|definition
-|-|-
bus|║ ═ ╠ ╩ ╦ ╣ ╚ ╗ ╔ ╝ ╬|carries wire references
wire|│ ─ ├ ┴ ┬ ┤ └ ┐ ┌ ┘ ┼|carries boolean references
junction|■|connects crossing lines (┼ and ╬ are crossing wires)
output|^ v < >|reads booleans to a wire from a logic gate (chooses direction of a logic gate)
and|\*|returns 1 if all inputs are 1
or|+|returns 0 if all inputs are 0 
xor|x|returns 1 if an odd number of inputs is 1
nor|!|returns 1 if all inputs are 0
bus call|a-z, A-Z|refers to a bus from the busboard 

```
a
╠═════╦══════╦══════╦══════╗
0     1      2      3      4
│     ├─┐    ├─┐    ├─┐    │
├───┬─┼─*>─┬─┼─*>─┬─┼─*>───x
!   └─x    └─x    └─x      v
v     v      v      v      │
0     1      2      3      4
╠═════╩══════╩══════╩══════╝
b
```
Currently implemented:
*-[ ]control 
  *-[]wires
*-[ ]running
