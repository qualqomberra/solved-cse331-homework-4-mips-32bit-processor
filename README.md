Download Link: https://assignmentchef.com/product/solved-cse331-homework-4-mips-32bit-processor
<br>
In this project, you will use Altera Quartus II with Verilog. You will implement a different version of 32-bit MIPS processor. The block that you will design will get no inputs from outside. You will have two memories: Data Memory and Instruction Memory. The instructions must be loaded to the instruction memory and the data must be put in data memory. You will support<strong> lw, sw, j, jal, jr, beq</strong>, <strong>bne</strong>, <strong>addn, subn, xorn, andn, orn,</strong> <strong>ori </strong>and<strong> lui </strong>instructions<strong>.</strong>

But the R-type instructions will execute different than the conventional MIPS we have seen. This is why they have ‘<strong>n</strong>’ at the end (representing <strong>n</strong>ew). The new instructions have the same opcode and function fields as the conventional R-type instructions. For instance the opcode and function field of <strong>orn</strong> is same as <strong>or</strong>. But the execution is different. For instance:

addn $rd, $rs, $rt <u>RTL Representation</u>

$rs &lt;= $rs + $rt if($rs + $rt == 0) $rd &lt;= 1

else if($rs + $rt &lt; 0)

$rd &lt;= 2 else $rd &lt;= 3 <strong> </strong>

In order to implement that, you must be able to write two different register addresses in one cycle Design your register accordingly.

You will write test bench and simulate your design for verification. You will write the register and memory contents before and after the execution of instructions using <strong>writememh</strong> in your test bench verilog code. You will initialize memory contents using <strong>readmemh</strong>.

The data memory size will be 256KB whereas the instruction memory size will be 16KB. Remember that addressing for a 256KB memory only requires 18 bits instead of 32 bits in regular MIPS. Update your design accordingly.




<strong> </strong>

<a href="https://www.youtube.com/watch?v=arj7oStGLkU">https://www.youtube.com/watch?v=arj7oStGLkU</a>

–