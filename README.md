# y80e
Y80e - Z80/Z180 compatible processor extended by eZ80 instructions.

Z80/Z180 compatible processor softcore. Based on Y80 project described in the book 'Microprocessor Design Using Verilog HDL' of Monte Dalryple from Systemyde. If you want to understand internals of CPU then this book may greately help you to do it.

This CPU supports commonly used Z80 undocumented instructions: operations with halfs of index registers and SLI/SLL (Shift Left Logical). Optionally it supports emulation of R register.

Additionally CPU is Z180 compatible. Supported all IO, MLT (implemented via standard Verilog multiplication) and TST instructions.

Moreover, it has all non-ADL instructions from Zilog eZ80 CPU:

```
IND2, IND2R, INDM, INDMR, INDRX, 
INI2, INI2R, INIM, INIMR, INIRX, 
LD (HL),rr 
LD (ii+d),rr 
LD rr,(HL) 
LD rr,(ii+d) 
LEA rr,ii+d 
OUTD2, OTD2R, OTDRX 
OUTI2, OTI2R, OTIRX 
PEA ii+d 

	ii - IX, IY 
	rr - BC, DE, HL, IX, IY 
```

By Sergey Belyashov, based on the work of Monte Dalryple
