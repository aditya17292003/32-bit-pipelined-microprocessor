Implentation of a 32-bit pipelined microprocessor using verilog.
MIPS32 is a 32 bit processor.
Pipelined stages are - Instruction fetch,Instruction decode,EXecution,Memory Access,Register Write back.
It contain 32,32-bit registers (R0-R31).
R0 contains a constant 0.
It also contains a special purpose 32-bit program counter.
No	flag	registers	(zero,	carry,	sign,	etc.).	
Very	few	addressing	modes	(register,	immediate,	register	indexed,	etc.)	
Only	load	and	store	instruc>ons	can	access	memory.	
It is	assumed	memory	word	size	is	32	bits	(word	addressable).	
All	MIPS32	instructions	can	be	classified	into	three	groups	in	terms	of	instructon	encoding.
R-type	(Register),	I-type	(Immediate),	and	J-type	(Jump).	
In	an	instruction	encoding,	the	32	bits	of	the	instruction	are	divided	into	several	fields	of	fixed	widths.
I	divided	the	instruction	execution	cycle	into	five	steps:	
a) IF	 :	Instruction	Fetch	
b) ID	 :	Instruction	Decode	/	Register	Fetch	
c) EX	 :	Execution	/	Effective	Address	Calculation	
d) MEM	 :	Memory	Access	/	Branch	Completion	
e) WB	 :	Register	Write-back
Basic	requirements	for	pipelining	the	MIPS32	data	path	
A new instruction cycle should be started every clock cycle.	
Each	of	the	five	steps	mentioned	before	(IF,	ID,	EX,	MEM	and	WB)	becomes	a	pipeline	stage.	
Each	stage	must	finish	its	execution	within	one	clock	cycle.
