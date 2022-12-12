Building a custom printf function

printf is the C language function to do formatted printing
In the early days, computer programmers would write their own subroutines to read in and print out numbers.

They did this by:
allocate a character array to hold the result, 
divide the number by ten, keep the remainder, 
add x30 to it, and store it at the end of the array. 
Repeat the process until all the digits are found.

But even though it was easy (for Einstein), it still
took some effort. And what about error checking,
and negative numbers? So the computer program-
mers brought forth libraries of prerecorded func-
tions. And it was good. Eventually the most popular
of these functions were canonized into membership
in the “standard” libraries. Number printing was
popular enough to gain this hallowed honor.

programmers did not have to reinvent the number-printing subroutine again and again.

Thus printf was born
--------------------------------------------------------------------------------------
BUILDING A _PRINTF FUNCTION
--------------------------------------------------------------------------------------
For this specifc task, I will build a _printf function which can handle similar commands to the printf function
This _printf function conatins:
1) main.h (header file): which will store all the necessary function definitions, data type definitions, and macros necessary to operate thee _printf function
2) main.c : which will check the code and return a value upon successful execution off the program, and return a non-zero value upon failure of the program's execution

The subfunctions included in this _printf function include:
1) _print-hex: which will print an unsigned integer in hexadecimal (base 16)
		print_hex: prints unsigned integer in hexadecimal (base 16)
		print_x: prints hexadecimal number in lowercase
		print_X: prints hexadecimal number in uppercase
2) _print-binary: which will print an unsigned integer in binary (base 2)
		print_bin: prints unsigned integer in binary
3) _print-chars: which will contain format and conversion s,c,S,r specifiers
		print_c: prints character
		print-hex: prints a character's ASCII code in hexadecimal form
		print_S: prints string; non printable character
		print_r: prints string in reverse
4) _print_nums: which will print numbers d, i, u, 0 formats
		print_di: prints decimal number (base 10)
		print_u: prints unsigned integer in decimal (base 10)
		print_o: prints unsigned integer in octal (base 8)
5) _printf: which is a printf-like function
		get_func: will pick the correct fucntion
		printf: the printf-like function
