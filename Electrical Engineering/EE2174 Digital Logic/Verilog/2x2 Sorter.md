- Sort 2 numerical values
```
module Sort2x2v1 (A, B, Max, Min); // Parallel

	parameter N = 8 
	input [N-1:0] A, B; // 8 bit A and B inputs
	output [N-1:0] Max; // 8 bit placeholder max value
	output [N-1:0] Min; // 8 bit placeholder min value
	
	assign Max = A > B ? A : B; // Write max
	assign Min = A > B ? B : A; // Write min
	
endmodule

module Sort2x2v2 (A, B, Max, Min); // Sequential, Procedural

	parameter N = 8 
	input [N-1:0] A, B; // 8 bit A and B inputs
	output reg [N-1:0] Max; // 8 bit placeholder max value
	output reg [N-1:0] Min; // 8 bit placeholder min value
	
	always@ (A,B) // Procedural specification, go one line at a time
		Max = A > B ? A : B; // Write max
		Min = A > B ? B : A; // Write min
	
endmodule
```
