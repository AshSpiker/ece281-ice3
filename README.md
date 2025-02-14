# ECE 281 ICE 3: Ripple-Carry Adder with Top Level Design

This is a **template** repository.

[ICE 3 instructions](https://usafa-ece.github.io/ece281-book/ICE/ICE3.html)

Targeted toward Digilent Basys3. Make sure to install the [board files](https://github.com/Xilinx/XilinxBoardStore/tree/2018.2/boards/Digilent/basys3).

Tested on Vivado 2024.2

---

## GitHub Actions Testbench

The workflow uses the [setup-ghdl-ci](https://github.com/ghdl/setup-ghdl-ci) GitHub action
to run a *nightly* build of [GHDL](https://ghdl.github.io/ghdl/).

First, the workflow uses GHDL to **analyze** all `.vhd` files in `src/`.

Then it **elaborates** the entity defined by `$TB_ENTITY`

Finally, the workflow **runs** the simulation. If successful then it will quietly exit with a `0` code.
If any of the `assert` statements fail then GHDL will cease the simulation and exit with non-zero code; this will also cause the workflow to fail.
Assert statements of other severity levels will be reported, but not fail the workflow.


![Waveform of my testbench on Vivado](Wave.png)
![PDF version of my sketch for the Basys3 top level](ICE3%20Sketch%20Schematic.pdf)

#DOCUMENTATION
For this assignment I recieved EI from Lt Col Wyche on 13 February 2025 because I was confused at how 
components worked and how the port mapping worked. He explained it to me, and sent me on my way, and 
I was able to complete it by myself. I also recieved other help from Lt Col Wyche while in my ECE 210
class due to the fact that I had never actually defined by Cout and was getting errors and was unsure why 
and it was because I had used too many interior cables. 