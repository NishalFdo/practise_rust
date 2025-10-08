# We learn Rust
### How programming languages work
#### How memory works in C/C++
##### How code turns into binary
- so when we compile the code, the compiler makes a object file which as .text(not .txt)
.bss and .data codes
.data is global vriables 
.bss are global variables that are not yet initalized
- The Os loader reads these and combine them to a exe that is loaded into the RAM
##### Whats stack n heap ?
- Its also part of the memory. just like .bss and data
- Those are 2 sections of ram that has been divided into by the OS to run the code.
- These are not pre defined in the binary like global variables n stuff, these are found while executing the code and it grows 
##### Stack 
- the memory is pre allocated to the stack by the OS. 
- The stack frame is the size of memeory in the stack allocated to a fucntion
- all the local varibales inside the function is stored in the stack
- if the stack frame grow to the point of; overflow youll get the stack overflow err
- after the function finishes running the memory is freed
- local vraiables and functions
- fast
##### Heap 
- This is used for dynamic memory allocation. like used to store stuff thatll grow as the code run.
- We can use this memory how ever we want
- But this is also limited so you gotta  manage it well
- C has mannual memory management where you have to use functions that will free the memory

- Mannual memory 
- slow
- Heap is used for dynamic memory allocation
- For stuff that doesnt have size in compile time
+--------------------------+
| Stack (top of memory)    |  ← grows downward
+--------------------------+
| Heap                     |  ← grows upward
+--------------------------+
| .bss                     |
| .data                    |
| .text                    |
+--------------------------+
.bass n stuff are for global variables
and the .text is the binary 
High memory addresses
---------------------
|       Stack       | <- grows downward
---------------------
|       Heap        | <- grows upward
---------------------
|       BSS         | uninitialized globals
|       Data        | initialized globals
---------------------
|       Text        | code / instructions
Low memory addresses


source code  →  compiler  →  object files  →  linker  →  executable  →  OS loads it to RAM
### Pointers and referances
- a Pointer is a variables that stores the memory address of another variable
- a Referance is the allias of the variables not a copy 
- &X means take the address of x
- *X means take there value of the address called x
## How rust works
- In rust there is a thing called Ownership, no 2 variables can own the same data at the same time
(Basically no copies n no variable can be in 2 scopes at once)
- If you really need copies there is a clone method you can use
- This ownership n borrowing only applies for non-primitive types
- Borrowing is using refercances n passing the values when you NEED copies
to be n 2 scopes at once
## How memory works in java
- 
### C does memory allocation mannually by there user while java does it at runtime with a garbage collector. Rust does it at runtime with ownership n borrowing  
