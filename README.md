/********************************************************************
 * README
 * Authors: Jack Burns (jburns08) & Ryan Ghayour (rghayo01)
 * calc40.ums callmain.ums printd.ums urt0.ums calc40.um compile
 * April 28, 2020
 ********************************************************************

Recieved some help from TAs (Ben, Adam and Jessica) with understanding of the
assignment as well as styling.

To the best of our knowledge, we have correctly implemented the RPN calculator.
urt0.ums allocates space for the call stack and initializes the stack pointer
to register 2 and r0 to 0. printd.ums outputs a single value from the value 
stack. calc40.ums allocates space for the value stack, sets up a jump table to
direct the program, and contains all of our operators. callmain.ums contains 
the initial call to main, and the final halt command.
There are no bugs, and all inputs work as expected.

No departures from recommended calling convention, we did use r3 to call the
value stack and we used r6 and r7 as our two permanent temp registers.

We implemented the print module by calling each number in calc40, and then 
parsing and printing the numbers in printd.ums.

We allocate space for the value stack in section data of calc40.ums, and call
it using register 3, which points to our value stack label.

Sections:
    section init: Initialize values and set registers to corresponding values
    section data: Allocate space and labels for various data structures
    section text: Write the functions used by the calculator
    section rodata: Allocates space for jumptable and sets labels.

Hours analyzing assignment: 5

Hours writing assembly code: 30

Hours debugging: 6
