# F83 (Forth 83 Model implementation, 16Bit)
## by Henry Laxen and Mike Perry, 1984  
## 8080, 8086, and 68000 distributions

This repository contains **F83**, a public domain implementation of 
FORTH-83 version 2.0 by Henry Laxen and Mike Perry for 

- CP/M-80 in directory `F83V2-80`
- CP/M 68000 in directory `F83V2-68`
- MSDOS: in directory `F83V2-MS`(run it in [a modern Browser](https://uho.github.io/F83/))

**F83** is a model implementation of the (now outdated) **Forth-83** standard. For your convenience you can find a copy of the Forth-83 standard document in the `Standard` directory.

The distributions also also contain source code in Forth block files (*.BLK, 1KB screens with 16 lines by 64 characters, no line breaks). You can best inspect these files from within a running F83 system.

The original Laxen/Perry distribution had these files squeezed with a program
that took hours (!) to run to unsqueeze at that time. See `HUFFMAN.BLK` and `EXPAND.BLK` for details. 

For further documentation please see the README files in the particular directories.

### Regenerating F83

F83 is self contained and can regenerate itself  without using other tools as it includes assemblers for the target processors (8080, 8086 and 68000) and its own meta compiler.

Sample regeneration run (here 68K version):

    C>f83 meta68.blk

    68000 Forth 83 Model 
    Version 2.1.0
    Modified 03Jun84
    ok
    
    OK ( your input )
    
          3 
          4 
    ...
         21 
    Meta Compiler Loaded
          1 
          2 
          3
    ...
         91 
     92 
    Unresolved references: 

        Statistics: 
    Last Host Address:           9596 
    First Target Code Address:   AD00 
    Last Target Code Address:    DC14 


    Now return to CP/M and type: 
    KERNEL EXTEND68.BLK <CR> 
    OK <CR>  ok
    
    BYE ( your input )
    150 Pages
    
    C> kernel extend68.blk
    
    OK ( your input )
    
    Loading system extensions.

    File Interface Loaded 
    MultiTasker Low Level Loaded 
    Machine Dependent IO Words Loaded 
    68000 Machine Dependent Code Loaded 
    Strings Loaded 
    Editor Loaded 
    Dumping Utility Loaded 
    Decompiler Loaded 
    Print Utility Loaded 
    Debugger Hi Level Loaded 
    MultiTasker Hi Level Loaded 
    Standard System Loaded 
    System has been loaded, Size = 28880 
    System saved as F83.68K  ok





