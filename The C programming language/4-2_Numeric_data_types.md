
1. On a 64-bit machine, the address space is 2^64 bytes. But most machines do not have that huge memory. A memory mapper,
 which is built in to the CPU, translates the address of CPU to actual RAM locations.
2. Inactive data may be swapped into disk, this is virtual memory.
3. Floating-point types consist of a fixed-size effective number X, and the exponent figure n, the final value is 
X * (2^n).
4. All other data is represented by converting it to either integer or floating-point numbers.
5. Char type
 * String is represented by integer, the value is ASCII code for each character. special character \n marks the 
end of the string.
 * Other characters are encoded by UTF-8.
 * color of a pixel is represented by three 8-bit integers, etc...
 
## Integers
* ints=longs = machine bits(32 or 64)
* char 8 bits
* long long, official in C99, twice the length of long type
* prefix, unsigned, signed. signed use 1 bit to indicate the postive/negativeness, so signed value's range is half the 
unsigned type.
* Negative value is -(2^n - acutal bit except first indication bit)
* addition/multiply is exactly same for binary bits for signed and unsigned, but the intepretation of result is different
* We can't avoid overflow in compiler, because int calculation needs truncate binary number to get correct answer.
* In C99, stdint.h provides clear size int, (u)int8(16/32/64)_t variable = value;
* INT_MIN, INT_MAX gives the smallest/largest value can be stored in int
