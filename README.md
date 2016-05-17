# Prog-6a
MASM - Program 6a - Computer Architecture and Assembly Language

This program requires the [Irvine Library] (http://kipirvine.com/asm/examples/index.htm)

### Objectives:
1. Designing, implementing, and calling low-level I/O procedures
2. Implementing and using a macro

### Problem Definition:
  - Implement and test your own *ReadVal* and *WriteVal* procedures for unsigned integers.
  - Implement macros *getString* and *displayString*. The macros may use Irvine’s *ReadString* to get input from the user, and *WriteString* to display output.
      * *getString* should display a prompt, then get the user’s keyboard input into a memory location
      * *displayString* should the string stored in a specified memory location.
      * *readVal* should invoke the *getString* macro to get the user’s string of digits. It should then convert the digit string to numeric, while validating the user’s input.
      * *writeVal* should convert a numeric value to a string of digits, and invoke the *displayString* macro to produce the output.
  - Write a small test program that gets 10 valid integers from the user and stores the numeric values in an array. The program then displays the integers, their sum, and their average.

### Requirements:
1.  User’s numeric input must be validated the hard way: Read the user's input as a string, and convert the string to numeric form. If the user enters non-digits or the number is too large for 32-bit registers, an error message should be displayed and the number should be discarded.
2. Conversion routines must appropriately use the **lodsb** and/or **stosb** operators.
3. All procedure parameters must be passed on the system stack.
4. Addresses of prompts, identifying strings, and other memory locations should be passed by address to the macros.
5. Used registers must be saved and restored by the called procedures and macros.
6. The stack must be “cleaned up” by the called procedure.
7. The usual requirements regarding documentation, readability, user-friendliness, etc., apply.

#### Notes:
1. For this assignment you are allowed to assume that the total sum of the numbers will fit inside a 32 bit register.
2. When displaying the average, you may round down to the nearest integer. For example if the sum of the 10 numbers is 3568 you may display the average as 356.
