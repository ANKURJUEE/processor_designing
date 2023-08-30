# processor_designing
 ![Processor_design](https://github.com/ANKURJUEE/processor_designing/assets/143562100/e31000a6-5201-491e-86af-9e3d368f6708)


Let us try to understand the different subcomponents which will be present in our processor.

This helps us to easily understand the different section that we have in our code.

So our processor consists of following subsystems.

First one is a control unit.
The primary objective of a control unit is to read an instruction from an instruction resistor, and
then, depending on an operation that is specified in an instruction, we need to perform the respective
operation.

For example, if user want to perform an automatic operation control unit will execute an automatic
instruction.
It will also specify source and destination resistor.
Likewise, if user want to read the data from an external world, it will convey that message to an
input buffer from where we will be reading a data from an outside world.
It will also control logical operation, reading and writing to data memory as well as general purpose
resistor.

So control unit is our central part which will control operation of an entire processor.
Then we have an instruction resistor.

This will be a simple 32 bit resistor which will store type of an operation that user want to perform.

In a general terminology, we refer it as an opcode, then the source and destination addresses for
our data.

All the information that specific instruction required will be specified in an instruction resistor.
Now, series of instruction will form the operation of our system that is, programs or program consists
of series of an instruction to achieve something out of our processor.
All the instruction or a single program.
We will be storing it into a program memory.
Now we could have a multiple program.
Finally, we will be combining them together to get the single program or single operation that we want
to achieve out of our processor.

So the operation that we're going to perform will be embedded in a series of an instruction which will
be stored in a program memory.
The data from program memory will be read by an instruction resistor after control unit.
Send the read or write signal to an instruction resistor, and then, depending on an instruction that
we have read, we're going to perform the specific operation.
Then we have an input buffer.
This allow us to read the data from an external GPIO pin which are available on an FPGA board.
The data that we read from an external world cannot be directly read by a general purpose resistor.

Instead, we need to store it into a data memory.

This is how we designed our processor, and then from a data memory, you could store it into a general
purpose resistor.

Likewise, the data, if you want to write to an external GPIO opens, you need to first write or store
the data in a data memory and then you are allowed to write it on an GPIO pin.

All the automatic as well as logical operation will be done only on the general purpose resistor.

We plan to include 32 general purpose resistor in our processor.
All the automatic as well as logical operation will take both the source data from a general purpose
resistor, and the result of this operation will again be stored back to the general purpose resistor.

In this case, if you want to store it in an data memory, you have series of an instruction to do it.
These are subsystems which are present in our processor.

First one is a control unit which will control the flow of a program that we have added in the program.
Memory.

The seeds of an instruction to achieve the specific task will be stored in a program.
Memory.

Single instruction at a time will be read in an instruction resistor.
It will be processed by a control unit and then we read the next instruction Arithmetic Unit is used
to perform an arithmetic operation.

Logical Unit is used to perform a logical operation.
Both arithmetic and a logical operation will be done on a general purpose data.
And the result of this operation will again be stored in a general purpose resistor.
If you want to store it.
If you want to have a temporary storage for data, you have a data memory.
The other functionality that we get with the data memory is the data that we're going to read from an
external word or write to an external world will be happening from a data memory.
We do not have a direct access of this external data in a general purpose resistor, but we do have
an instruction that works between data, memory and general purpose resistor so that you could move
data back and forth between gpcr and data memory.

