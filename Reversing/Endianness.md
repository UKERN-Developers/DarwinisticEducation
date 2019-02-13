# Endianness
Left or Right, Little or Big memory. In other words, byte order.

## About
Endianness (Byte Order) is the way the memory is read.

ARM processors can switch between endianness which makes them highly efficient processors in my opinion.

Endianness can be seen just like the way arab and english reading differs.

We read english from left to right.

And arab should be read from right to left.

Little endian therefore should be read from right to left, and big endian from left to right.

## Big endian
Example: 0xABCDEF 

### Converting to little endian
take the first to 2 hex characters on the right end and move them to the left end.

take the next 2 hex characters on the right end and move them to the left end.

Repeat this until all charcters are moved.

Example: 0xABCDEF becomes 0xEFCDAB

## Little endian
Example: 0xEFCDAB

### Converting to big endian
take the first 2 hex characters on the left and move them to the right end.

take the next 2 hex charcters on the left end and move them the right end.

Repeat this until all charcters are moved.

Example: 0xEFCDAB becomes 0xABCDEF


## Programmatically swapping endianness
Snippets for swapping endianness in multiple programming languages can be found in the Sources folder of this repo under Endianness
