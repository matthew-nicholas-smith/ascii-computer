#README

This is an ascii-based computer architecture ide.

Terminology:
term|definition
-|-
wire|carries a signal in any direction it connects to, used as output for logic gates
diode|carries a signal from one direction to the opposite side only, used as input for logic gates
logic gates|gates that perform different functions, eg. `*+x!`

Syntax:
command|ascii|definition
-|-|-
bus|║ ═ ╠ ╩ ╦ ╣ ╚ ╗ ╔ ╝ ╬
wire|│ ─ ├ ┴ ┬ ┤ └ ┐ ┌ ┘ ┼
junction|■ (┼ and ╬ are crossing wires)
diode|^ v < >
and|* returns 1 if all inputs are 1
or|+ 
xor|x
nor|!
```
a
╠═══╦════╦════╦════╗
0   1┌┐  2┌┐  3┌┐  4
│   ├┘v  ├┘v  ├┘v  │
├─┬─┼>*┬─┼>*┬─┼>*┐ │
v │ v  │ v  │ v  │ v
! └>x  └>x  └>x  └>x
0   1    2    3    4
╠═══╩════╩════╩════╝
b
```
Currently implemented:
-[ ] 
-[ ]
-[ ]
-[ ]
-[ ]
